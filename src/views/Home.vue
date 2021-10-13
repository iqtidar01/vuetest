<template>

<div class="w-full max-w-xs">
  <form class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
    <div class="mb-4">
      <label class="block text-gray-700 text-sm font-bold mb-2" for="username">
        A
      </label>
      <input v-model="a" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"  type="number" placeholder="Enter any number">
    </div>
    <div class="mb-6">
      <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
        B
      </label>
      <input v-model="b" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"  type="number" placeholder="Enter any number">

     
    </div>
     <div class="mb-6">
      <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
        Sum
      </label>
      <input v-model="sumval" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"  type="number" placeholder="">

     
    </div>
    <div class="flex items-center justify-between">
      <button @click="add"  class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="button">
        Click
      </button>
      
    </div>
  </form>


</div>



</template>

<script lang="ts">



export default ({
   data: () => ({
    a:'',
      b:'',
      sumval:'',
  }),

  methods: {
  add: function () {
    if(this.a==""){
    alert('Input Value in A');
    }
    else if(this.b==""){
    alert('Input Value in B');
    }else{
    let result=parseFloat(this.a)+parseFloat(this.b);
    this.sumval=result;
    }
}
  },
})
</script>


