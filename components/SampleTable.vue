<script setup lang="ts">
interface DataProps {
  firstName: String;
  lastName: String;
  userId: string;
  accountCreationDate: String;
  accountStatus: String;
  activeSales: Number;
  completedSales: Number;
  dealerName: String;
  eamil: String;
}
interface Props {
  data: DataProps[];
}
const props = withDefaults(defineProps<Props>(), {});
</script>

<template>
  <div>
    <v-table>
      <thead>
        <tr>
          <th class="text-left">First Name</th>
          <th class="text-left">Last Name</th>
          <th class="text-left">User ID</th>
          <th class="text-left">Acct Creation Date</th>
          <th class="text-left">Acct Status</th>
          <th class="text-left">Active Sales</th>
          <th class="text-left">Completed Sales</th>
          <th class="text-left">Dealer Name</th>
          <th class="text-left">Email</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in data" :key="item.userId">
          <td>{{ item.firstName }}</td>
          <td>{{ item.lastName }}</td>
          <td>{{ item.userId }}</td>
          <td>{{ item.accountCreationDate }}</td>
          <td>{{ item.accountStatus }}</td>
          <td>{{ item.activeSales }}</td>
          <td>{{ item.completedSales }}</td>
          <td>{{ item.dealerName }}</td>
          <td>{{ item.eamil }}</td>
        </tr>
      </tbody></v-table
    >
  </div>
</template>
