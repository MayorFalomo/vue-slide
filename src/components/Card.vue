<template>
<div class="cardContainer" >
<div class="faqModal" > 
    <h1> Questions </h1>
    <div class="faqContainer" >
    <div class="faqSection" > 
        <div :style="flexTexts " >
        <p class="question" >Do I Have To Allow The Use Of Cookies? </p>
        <span v-if="numberZero == 0" @click="numberZero = 1 " :style="styleBtn " > + </span>
        <span v-if="numberZero == 1" @click="numberZero = 0" :style="styleBtn "  > - </span>
        </div>
        <p v-if="numberZero == 1" class="faqAnswer" >Unicorn vinyl poutine brooklyn, next level direct trade iceland. Shaman copper mug church-key coloring book, whatever poutine normcore fixie cred kickstarter post-ironic street art. </p>
    </div>
    <div class="faqSection" > 
        <div :style="flexTexts" >
        <p class="question" >How Do I Change My My Page Password? </p>
        <span v-if="numberOne == 1" @click="numberOne = 2 " :style="styleBtn "  > + </span>
        <span v-if="numberOne == 2" @click="numberOne = 1" :style="styleBtn "  > - </span>
        </div>
        <p v-if="numberOne == 2"  class="faqAnswer"  >Coloring book forage photo booth gentrify lumbersexual. Migas chillwave poutine synth shoreditch, enamel pin thundercats fashion axe roof party polaroid chartreuse. </p>
    </div>
    <div class="faqSection" > 
        <div :style="flexTexts" >
        <p class="question" >What is Bank Id? </p>
         <span v-if="numberTwo == 2" @click="numberTwo = 3 "  :style="styleBtn "  > + </span>
        <span v-if="numberTwo == 3" @click="numberTwo = 2"  :style="styleBtn "  > - </span>
        </div>
        <p v-if="numberTwo == 3"  class="faqAnswer"  >Enamel pin fam sustainable woke whatever venmo. Authentic asymmetrical put a bird on it, lumbersexual activated charcoal kinfolk banjo cred pickled sartorial. </p>
    </div>
    <div class="faqSection" > 
        <div :style="flexTexts" >
        <p class="question" >Whose Birth Number Can I Use? </p>
         <span v-if="numberThree == 3" @click="numberThree = 4" :style="styleBtn "  > + </span>
        <span v-if="numberThree == 4" @click="numberThree = 3" :style="styleBtn "  > - </span>
        </div>
        <p  v-if="numberThree == 4"  class="faqAnswer"  >Unicorn vinyl poutine brooklyn, next level direct trade iceland. Shaman copper mug church-key coloring book, whatever poutine normcore fixie cred kickstarter post-ironic street art. </p>
    </div>
    <div class="faqSection" > 
        <div :style="flexTexts" >
        <p class="question" >When Do I Recieve A Password Ordered By Letter? </p>
         <span  v-if="numberFour == 4" @click="numberFour = 5" :style="styleBtn "  > + </span>
        <span  v-if="numberFour == 5" @click="numberFour = 4" :style="styleBtn "  > - </span>
        </div>
        <p  v-if="numberFour == 5"  class="faqAnswer"  >Locavore franzen fashion axe live-edge neutra irony synth af tilde shabby chic man braid chillwave waistcoat copper mug messenger bag. Banjo snackwave blog, microdosing thundercats migas vaporware viral lo-fi seitan </p>
    </div>
    <div class="faqSection" > 
        <div :style="flexTexts" >
        <p class="question" >Do I Have To Allow The Use Of Cookies? </p>
         <span  v-if="numberFive == 5" @click="numberFive = 6" :style="styleBtn "  > + </span>
        <span  v-if="numberFive == 6" @click="numberFive = 5" :style="styleBtn " > - </span>
        </div>
        <p  v-if="numberFive == 6"  class="faqAnswer"  >Unicorn vinyl poutine brooklyn, next level direct trade iceland. Shaman copper mug church-key coloring book, whatever poutine normcore fixie cred kickstarter post-ironic street art. </p>
    </div>
    </div>
</div>
</div>
</template>

<script>
export default {
props: {
    carousel: Object
},
data() {
    return {
        numberZero: 0,
        numberOne: 1,
        numberTwo: 2,
        numberThree: 3,
        numberFour: 4,
        numberFive: 5,
        styleBtn : {
 fontSize: '22px',
    minWidth: '30px',
    minHeight: '30px',
    backgroundColor: '#164E63',
    color: 'white',
    borderRadius: '50%',
    display: 'grid',
    placeContent: 'center',
    cursor: 'pointer',
        },
        flexTexts : {
             display: 'flex',
    justifyContent: 'space-between',
    alignItems: 'center',
    padding: '15px',
    width: '100%',
        }
    }
},
}
</script>

<style>
.cardContainer{
   width: 100vw;
   min-height: 100vh;
   overflow: hidden;
   display: flex;
   justify-content: center;
   align-items: center;
   margin: 0 auto;
   background-color: #CFFAFE;
   font-family: "Inclusive Sans";
}
.faqModal {
    width: 60%;
    height: fit-content;
    /* max-height: 700px; */
     border-radius: 20px;
  padding: 20px;
  background-color: white;
box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
}
.faqModal h1{
    text-align: center;
   font-size: 30px;
}
.faqContainer{
    display: flex;
    flex-direction: column;
    gap: 20px;
    align-items: center;
    margin: 30px auto;
    width: 90%;
}
.faqSection{
    width: 100%;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;

}

.faqSection .question{
    font-size: 20px;
    font-weight: 700;
    line-height: 40px;
   padding: 10px;
   color: #334155;
}
.faqSection .faqAnswer{
    font-size: 18px;
    line-height: 30px;
   width: 95%;
   margin: 0 auto;
   color: #000;
   opacity: 0.8;
}

@media (max-width: 1200px) {
    .faqModal{
        width: 80%;
    }
}
@media (max-width: 850px) {
    .faqModal{
        width: 95%;
    }
}
@media (max-width: 500px) {
    .faqModal{
        width: 100%;
        border-radius: 0;
    }
    .faqContainer{
        width: 100%;
    }
}
</style>