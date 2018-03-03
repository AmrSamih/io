<template>
    <div class="row">
      <div class="col-md-12">
        <div class="card">
          <paper-table :title="table1.title" :sub-title="table1.subTitle" :data="table1.data" :columns="table1.columns">

          </paper-table>
        </div>
      </div>

    </div>
</template>
<script>
  import PaperTable from 'components/UIComponents/PaperTable.vue'
  const tableColumns = ['Id', 'Name', 'Price', 'CreatedAt', 'UpdatedAt', 'SellerName']
  const tableData = [{
    id: 1,
    name: 'Dakota Rice',
    price: '$36.738',
    createdat: '15/2/2018',
    updatedat: '16/2/2018',
    sellername: 'Mo'
  },
  {
    id: 2,
    name: 'Minerva Hooper',
    price: '$36.738',
    createdat: '15/2/2018',
    updatedat: '16/2/2018',
    sellername: 'Mo'
  }
  {
  id: 3,
  name: 'mug',
  price: '$50',
  createdat: '15/2/2018',
  updatedat: '16/2/2018',
  sellername: 'mo'
  }

  {
    id: 4,
    name: 'Batman Jacket',
    price: '$36.738',
    createdat: '15/2/2018',
    updatedat: '16/2/2018',
    sellername: 'mo'
  }

  ]

  export default {
    components: {
      PaperTable
    },
    data () {
      return {
        table1: {
          title: 'Stripped Table',
          subTitle: 'Here is a subtitle for this table',
          columns: [...tableColumns],
          data: [...tableData]
        },
        table2: {
          title: 'Table on Plain Background',
          subTitle: 'Here is a subtitle for this table',
          columns: [...tableColumns],
          data: [...tableData]
        }
      }
    }
  }

  <button class="Update">
          <slot>Update Product</slot>
          </button>
          <div id = "app">
          <v-header></v-header>
          <v-button></v-button>
          </div>

      <button class="Add">
      <slot>Add Product</slot>
      </button>
      <div id = "app">
      <v-header></v-header>
      <v-button></v-button>
      </div>

      <button class="Delete">
      <slot>Delete Product</slot>
      </button>
      <div id = "app">
      <v-header></v-header>
      <v-button></v-button>
      </div>

</script>
<style>

</style>
