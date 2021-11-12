<template>
    <v-row justify="center" align="center"> 
      <v-col cols="12">      
        <v-simple-table>
          <thead>
            <tr>
              <th>No.</th>
              <th>Employee Number</th>
              <th>First Name</th>
              <th>Last Name</th>
              <th>Email</th>
              <th>Gender</th>              
              <th>Phone Number</th>
              <th>Action</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(item,index) in employees" :key="item.id" >
              <td>{{ index + 1 }}</td>
              <td>{{ item.employee_number }}</td>
              <td>{{ item.first_name }}</td>
              <td>{{ item.last_name }}</td>
              <td>{{ item.email }}</td>
              <td>{{ item.gender }}</td>              
              <td>{{ item.phone_number }}</td>

              <td>
                <v-btn class="mx-2" fab dark small color="blue" >
                  <v-icon dark>
                    mdi-pencil
                  </v-icon>
                </v-btn>
                <v-btn class="mx-2" fab dark small color="red" >
                  <v-icon dark>
                    mdi-delete
                  </v-icon>
                </v-btn>
              </td>
            </tr>
          </tbody>
        </v-simple-table>
      </v-col>
    </v-row>
</template>
<script>
  export default {
    data() {
      return {
        employees: [
          {
            id: 1,
            employee_number: 'E0100',
            first_name: 'Test',
            last_name: 'Name',
            gender: 'Female',
            email: 'test@gmail.com',
            phone_number: '09999777',
          },
          {
            id: 2,
            employee_number: 'E0102',
            first_name: 'Test 2',
            last_name: 'Name 2',
            gender: 'Male',
            email: 'test2@gmail.com',
            phone_number: '09999777',
          },
          {
            id: 3,
            employee_number: 'E0103',
            first_name: 'Test',
            last_name: 'Name',
            gender: 'Female',
            email: 'test@gmail.com',
            phone_number: '09999777',
          },
          {
            id: 4,
            employee_number: 'E0104',
            first_name: 'Test 4',
            last_name: 'Name 4',
            gender: 'Male',
            email: 'test4@gmail.com',
            phone_number: '09999777',
          },
        ]
      }
    }
  }
</script>
<style scoped>
.v-data-table tr:hover {
  background: none!important;
}
</style>