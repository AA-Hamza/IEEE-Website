<template>
  <div class="ras">
    <carousel v-bind:carousel="data['carousel']"/>
    <about-us v-bind:data="data['about']" />
    <team v-bind:data="data['team']"/>
    <contact-us v-bind:contact="data['contact-us']"/>
    <committees-footer v-bind:data="data"/>
  </div>
</template>

<script>
import Database from '/database/database';
import Carousel from '@/components/committees/Carousel';
import AboutUs from '@/components/committees/AboutUs';
import Team from '@/components/committees/Team'
import ContactUs from '@/components/committees/ContactUs'
import CommitteesFooter from '@/components/committees/CommitteesFooter';


export default{

  components:{
    'carousel':Carousel,
    'about-us':AboutUs,
    'team':Team,
    'contact-us':ContactUs,
    'committees-footer':CommitteesFooter

  },

  data(){
    return{
      data: Database.committees.ras,
      
    }
  }
}

</script>
