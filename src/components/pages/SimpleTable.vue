<template>
  <div>
    <md-table v-model="users" :table-header-color="tableHeaderColor">
      <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="Name">{{ item.name }}</md-table-cell>
        <md-table-cell md-label="Username">{{ item.name }}</md-table-cell>
        <md-table-cell md-label="Password">{{ item.name }}</md-table-cell>
        <md-table-cell md-label="Contact">{{ item.name }}</md-table-cell>
        <md-table-cell md-label="Country">{{ item.country }}</md-table-cell>
        <md-table-cell md-label="City">{{ item.city }}</md-table-cell>
        <md-table-cell md-label="Role">{{ item.role }}</md-table-cell>
         <md-table-cell md-label="Action">
           <md-button class="md-just-icon md-simple md-primary">
            <md-icon>edit</md-icon>
            <md-tooltip md-direction="top">Edit</md-tooltip>
          </md-button>
          <md-button class="md-just-icon md-simple md-danger">
            <md-icon>delete</md-icon>
            <md-tooltip md-direction="top">Delete</md-tooltip>
          </md-button>
         </md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
export default {
  name: "simple-table",
  props: {
    tableHeaderColor: {
      type: String,
      default: "green"
    }
  },
  data() {
    return {
      selected: [],
      users: [
        {
          name: "Dakota Rice",
          role: "Chef",
          country: "Niger",
          city: "Oud-Turnhout"
        },
        {
          name: "Minerva Hooper",
          role: "Chef",
          country: "Curaçao",
          city: "Sinaai-Waas"
        },
        {
          name: "Sage Rodriguez",
          role: "Chef",
          country: "Netherlands",
          city: "Overland Park"
        },
        {
          name: "Philip Chaney",
          role: "Chef",
          country: "Korea, South",
          city: "Gloucester"
        },
        {
          name: "Doris Greene",
          role: "Waiter",
          country: "Malawi",
          city: "Feldkirchen in Kārnten"
        },
        {
          name: "Mason Porter",
          role: "Waiter",
          country: "Chile",
          city: "Gloucester"
        }
      ]
    };
  }
};
</script>
