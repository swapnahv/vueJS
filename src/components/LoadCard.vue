<template>
  <div class="cards" >
      <div >
        <div>
          <div>
            <div v-if="visibleSlide === 0">
        <img src="../assets/img_statement_1.png" alt="" style="width:50%">
      </div>
      <div v-if="visibleSlide === 1">
        <img src="../assets/img_statement_2.png" alt="" style="width:50%">
      </div>
      <div v-if="visibleSlide === 2">
        <img src="../assets/img_statement_3.png" alt="" style="width:50%">
      </div >
      <div v-if="visibleSlide === 3">
        <img src="../assets/img_statement_4.png" alt="" style="width:50%">
      </div>
      <div v-if="visibleSlide === 4">
        <img src="../assets/img_statement_5.png" alt="" style="width:50%">
      </div>
      <div v-if="visibleSlide === 5">
        <img src="../assets/img_statement_6.png" alt="" style="width:50%">
      </div>
          </div>
      <div class="nextDiv">
        <a class="next" @click="nextCard();">&#10095;</a>
      </div>
        </div>
        <div class="smilies">
          <a >
            <img src="../assets/img_cat_happy.png" alt="" style="width:100px;height:100px">
          </a>
          <a>
            <img src="../assets/img_cat_neutral.png" alt="" style="width:100px;height:100px">
          </a>
          <a>
            <img src="../assets/img_cat_supersad.png" alt="" style="width:100px;height:100px">
          </a>
        </div>
      </div>
      
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      cards: [],
      visibleSlide: 0
    }
  },
  props: {
    msg: String
  },
  methods: {
    nextCard(){
      if(this.visibleSlide<5) {
        this.visibleSlide++;
      }
    }
  }
}
</script>

<style lang="scss" scoped>
  .smilies img{
    background-color: white;
    border-radius: 4px;
    margin-right: 10px;
  }
  .nextDiv{
        font-size: 20px;
    background-color: lightgrey;
    color: white;
    width:30px;
    height:30px;
    text-align: center;
  }
  a:hover{
    cursor: pointer;
  }
</style>


