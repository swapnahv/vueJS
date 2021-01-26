<template>
<div>
  <div class="cards" id="cards">
      <div id="question">
        <h3>How do you feel about these quotes?</h3>
      </div>
      <div>
        <div id="cardList">
          <div>
            <div v-if="visibleSlide === 0">
        <img src="../assets/img_statement_1.png" alt="" >
      </div>
      <div v-if="visibleSlide === 1">
        <img src="../assets/img_statement_2.png" alt="" >
      </div>
      <div v-if="visibleSlide === 2">
        <img src="../assets/img_statement_3.png" alt="" >
      </div >
      <div v-if="visibleSlide === 3">
        <img src="../assets/img_statement_4.png" alt="" >
      </div>
      <div v-if="visibleSlide === 4">
        <img src="../assets/img_statement_5.png" alt="" >
      </div>
      <div v-if="visibleSlide === 5">
        <img src="../assets/img_statement_6.png" alt="" >
      </div>
          </div>
      
        </div>
        <div class="smilies">
          <a @click="feedback('happy');">
            <img src="../assets/img_cat_happy.png" alt="" style="width:100px;height:100px"/>
          </a>
          <a @click="feedback('neutral');">
            <img src="../assets/img_cat_neutral.png" alt="" style="width:100px;height:100px">
          </a>
          <a @click="feedback('supersad');">
            <img src="../assets/img_cat_supersad.png" alt="" style="width:100px;height:100px">
          </a>
        </div>
      </div>
      
  </div>
  <div class="nextDiv">
        <a class="next" @click="nextCard();">&#10095;</a>
      </div>
      </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      cards: [],
      visibleSlide: 0,
      feedbackValue: null
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
    },
    feedback(value){
      this.feedbackValue = value;
      this.nextCard();
    }
  }
}
</script>

<style lang="scss" scoped>
  #cardList img {
    width:90%;
    margin: 20px;
  }
  .smilies img{
    background-color: white;
    border-radius: 4px;
    margin: 10px;
  }
  .nextDiv{
        font-size: 20px;
    background-color: lightgrey;
    color: white;
    width:30px;
    height:30px;
    text-align: center;
    position: absolute;
    top:25%;
    display:inline-block;
    margin-left: 20px;
  }
  a:hover{
    cursor: pointer;
  }
  #cards{
    text-align: center;
    width:50%;
    background-color:yellowgreen;
    display:inline-block;
  }
  #question {
    border-bottom:0.5px solid white;
    color:white;
  }
</style>


