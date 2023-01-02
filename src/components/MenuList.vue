<template>
    <div class = "menu">
        <div class = "title">Demo Todo List</div>
        
        <div v-for="(item,index) in list" :key="item.id">
            <div class="item">{{index+1}}.{{item.name}}</div>
        </div>
        
        <div class="button">
            <button class="addBtn">Add Item</button>
        </div>
    </div>
</template>
<script>
export default {
  name: 'MenuList',
  props: {
  },
  setup(){
    const list = [
        {
            id:0,
            name:'item title',
            content:'text',
            dateFrom:'',
            dateEnd:'',
            image:''
        }]
    return{
        list
    }
  }

}
</script>
<style lang="scss" scoped>
.menu {
    background: #A1FFC7;
    width: 15%;
    height: 100vh;
    float: left;
    .title {
        padding: 20px;
        font-family: sans-serif;
        font-weight: bold;
    }
}
.item {
    background: #81F8B1;
    height: 20px;
    padding: 10px;
    display: flex;
    align-items: center;
    font-family: sans-serif;
}
.button{
    display: flex;
    justify-content: center; 
    align-items: center; 
}
.addBtn{
    background: #E7FFE9;
    border: #E7FFE9;
    border-radius: 10px;
    width: 180px;
    height: 30px;
    margin: 10px
}
</style>