<script>
/*import BenefitCard from './benefitCard.vue'*/
export default {
  /*components: {
    BenefitCard
  },*/
  data() {
  	return {
    	items: [
            { image:'1.png',
            title: 'Performant',
            text: 'Truly reactive, compiler-optimized rendering system that rarely requires manual optimization.'}, 
            { image:'2.png',
            title: 'Approachable',
            text: 'Builds on top of standard HTML, CSS and JavaScript with intuitive API and world-class documentation.'}, 
            { image:'3.png',
            title: 'Versatile',
            text: 'A rich, incrementally adoptable ecosystem that scales between a library and a full-featured framework.'}, 
        ]
  	}
  }
}
</script>

<template>
    <div id="bodyBenefits">
        <div 
            v-for="item in items"
            :key="item.image">
            <img v-bind:src="'/src/assets/USP-' + item.image">
            <h3>{{ item.title }}</h3> 
            <p>{{ item.text }}</p>
        </div>
    </div>
    
</template>

<style scoped>
#bodyBenefits {
    background-color: #39B983;
    display: flex;
    justify-content: space-around;
}

div {
    text-align: center;
}
</style>