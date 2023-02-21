<template>
    <Preloader v-if="isLoading" />
    <router-view />
    <BackToTop />
</template>

<script type="application/ld+json">
import Preloader from './components/Layouts/Preloader'
import BackToTop from './components/Layouts/BackToTop'

export default {
    name: 'App',
    components: {
        Preloader,
        BackToTop,
    },
    data() {
        return {
            isLoading: true
        }
    },
    mounted() {
        setTimeout(() => {
            this.isLoading = false
        }, 2000)
    },
"@context": "https://schema.org",
  "@type": "BreadcrumbList", 
  "itemListElement": [{
    "@type": "ListItem", 
    "position": 1, 
    "name": "Home",
    "item": "https://www.brightgroupltd.com/"  
  },{
    "@type": "ListItem", 
    "position": 2, 
    "name": "About",
    "item": "https://www.brightgroupltd.com/about"  
  },{
    "@type": "ListItem", 
    "position": 3, 
    "name": "Service",
    "item": "https://www.brightgroupltd.com/service"  
  },{
    "@type": "ListItem", 
    "position": 4, 
    "name": "Contact",
    "item": "https://www.brightgroupltd.com/"  
  }]
}
</script>