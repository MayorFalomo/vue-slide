<script>
import CardVue from './components/Card.vue'
import { Icon } from '@iconify/vue';
export default {
  name: "App",
  components: {
    CardVue,
    Icon,
  },
  data() {
    return{
  carousels : [
    {
    id: 1,
    image: "https://res.cloudinary.com/diqqf3eq2/image/upload/v1586883334/person-1_rfzshl.jpg",
    name: "Susan Smith",
    position: "WEB DEVELOPER",
    comment: "I'm baby meggings twee health goth +1. Bicycle rights tumeric chartreuse before they sold out chambray pop-up. Shaman humblebrag pickled coloring book salvia hoodie, cold-pressed four dollar toast everyday carry"
          },
    {
    id: 2,
    image: "https://res.cloudinary.com/diqqf3eq2/image/upload/v1586883409/person-2_np9x5l.jpg",
    name: "Anna Johnson",
    position: "WEB DESIGNER",
    comment: "Helvetica artisan kinfolk thundercats lumbersexual blue bottle. Disrupt glossier gastropub deep v vice franzen hell of brooklyn twee enamel pin fashion axe.photo booth jean shorts artisan narwhal."
          },
    
    {
    id: 3,
    image: "https://res.cloudinary.com/diqqf3eq2/image/upload/v1586883417/person-3_ipa0mj.jpg",
    name: "Peter Jones",
    position: "INTERN",
    comment: "Sriracha literally flexitarian irony, vape marfa unicorn. Glossier tattooed 8-bit, fixie waistcoat offal activated charcoal slow-carb marfa hell of pabst raclette post-ironic jianbing swag."
          },
    {
    id: 4,
    image: "https://res.cloudinary.com/diqqf3eq2/image/upload/v1586883423/person-4_t9nxjt.jpg",
    name: "Bill Anderson",
    position: "THE BOSS",
    comment: "Edison bulb put a bird on it humblebrag, marfa pok pok heirloom fashion axe cray stumptown venmo actually seitan. VHS farm-to-table schlitz, edison bulb pop-up 3 wolf moon tote bag street art shabby chic."
    },
    ],
    carouselIndex: 0,
    }
    
  },
  methods: {
    handleNext() {
      this.carouselIndex = (this.carouselIndex + 1) % this.carousels.length;
    },
    handlePrevious() {
      this.carouselIndex = (this.carouselIndex - 1 + this.carousels.length) % this.carousels.length;
    },
    pickRandomIndex() {
      this.carouselIndex = Math.floor(Math.random() * this.carousels.length);
    },
  }
}
</script>

<template>
 <div class="wrapper" >
<div  class="wrappedModal" >
 <div class="infoContainer" >
<div class="carouselImg" >
  <img :src="carousels[carouselIndex].image "  class="carouselImage"  alt="img" />
</div>
<h1> {{carousels[carouselIndex].name}} </h1>
<span> {{carousels[carouselIndex].position}} </span>
<p> {{carousels[carouselIndex].comment}} </p>
</div>
<div class="controlBtn" >
<span @click="handleNext " ><Icon icon="uim:angle-left" width="50px" height="50px" /></span>
<span @click="handlePrevious " ><Icon icon="uim:angle-right"  width="50px" height="50px" /> </span>
</div>
<button @click="pickRandomIndex " class="surpriseBtn" > Surprise Me </button>
</div>
 </div>
 <CardVue/>
</template>

<style scoped>
.wrapper{
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #F8FAFC;
}
.wrappedModal{
   height: fit-content;
   max-height: 800px;
   width: 60%;
   max-width: 900px;
   min-width: 350px;
    background-color: white;
  border-radius: 20px;
  padding: 20px;
box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
}
.infoContainer{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 10px;
}
.carouselImg{
    position: relative;
    width: 230px;
    height: 230px;
    background-color: #645CFF;
    border-radius: 50%;
}
.carouselImg span{
  background: #645CFF;
  color: white;
  position: absolute;
  left: 0;
  top: 20px ;
  z-index: 2;
  font-size: 35px;
}

.carouselImage{
    width: 100%;
    height: 100%;
    object-fit: cover;
    position: absolute;
    left: -15px;
    top: 0;
    z-index: 1;
    background-color: #645CFF;
    border-radius: 50%;
}

.infoContainer h1{
  font-size: 30px;
  font-weight: 500;
  margin-top: 10px;
}
.infoContainer span{
  font-size: 20px;
  color: #735CFF;
}
.infoContainer p{
  font-size: 20px;
  line-height: 35px;
  width: 95%;
  text-align: center;
}
.controlBtn{
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
}
.controlBtn span{
  cursor: pointer;
}
.surpriseBtn{
  display: flex;
  justify-content: center;
  font-size: 18px;
  border: none;
  outline: none;
  padding: 10px 20px;
  border-radius: 8px;
  margin: 20px auto;
  background-color: #C1BEFF;
  color: #735CFF;
  cursor: pointer;
}

@media (max-width: 600px) {
  .wrappedModal{
    width: 95%;
  }
  .carouselImg{
    width: 150px;
    height: 150px;
   
}
}
</style>
645CFF