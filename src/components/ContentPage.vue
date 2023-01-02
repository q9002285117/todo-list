<template>
    <div class="header">
        <img class= "delete" src="../assets/delete.png">
    </div>
    <div class= "page">
        <input class = "input">
        <input class = "content">

        <img class= "image" :src="image"/>
        <input type="file" @change="fileSelected">
    </div>
</template>
<script>
import { ref } from 'vue'
export default {
  name: 'ContentPage',
  props: {
  },
  setup(){
    const image = ref('')
    const list = [
        {
            id:0,
            name:'item title',
            content:'text',
            dateFrom:'',
            dateEnd:'',
            image:''
        }]

    const fileSelected = (e) => {
      const file = e.target.files.item(0);
      const reader = new FileReader();
      reader.addEventListener('load', imageLoaded);
      reader.readAsDataURL(file);
    }
    const imageLoaded = (e) => {
      image.value = e.target.result;
    }

    return{
        list,
        image,
        fileSelected,
        imageLoaded
    }
  }

}
</script>
<style lang="scss" scoped>
.header{
    height: 40px;
    .delete{
        float: right;
        width: 20px;
        margin: 20px;
    }
}
.page {
    margin-left: 16%;
    .input {
        width: 97%;
        height: 30px;
        border-radius: 10px;
        margin: 10px;
        background: #EBEBEB;
        border: #EBEBEB;
    }
    .content {
        width: 50%;
        height: 90px;
        margin: 10px;
        border-radius: 10px;
        background: #EBEBEB;
        border: #EBEBEB;
    }
    .image {
        background: #EBEBEB;
        width: 30%;
    }
}
</style>