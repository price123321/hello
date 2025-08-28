
        <template>
          <table>
            <thead>
              <tr>
                <th>ID</th>
                <th>Name</th>
                <th>Value</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="item in tableData" :key="item.id">
                <td>{{ item.id }}</td>
                <td>{{ item.name }}</td>
                <td>{{ item.value }}</td>
              </tr>
            </tbody>
          </table>
        </template>

        <script>
        import axios from 'axios'; // Or use fetch

        export default {
          data() {
            return {
              tableData: [],
            };
          },
          async created() {
            try {
              const response = await axios.get('http://localhost:3000/api/table-data');
              this.tableData = response.data;
            } catch (error) {
              console.error('Error fetching data:', error);
            }
          },
        };
        </script>