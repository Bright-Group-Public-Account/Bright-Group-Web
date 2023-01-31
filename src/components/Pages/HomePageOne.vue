<template>
    <div>
        <Navbar />
        <MainBanner />
        <Partner />
        <About />
        <Services />
        <ChooseUs />
        <Video />
        <Projects />
        <Testimonials />
        <Pricing />
        <Blog />
        <Footer />
    </div>
</template>

<script>
import Navbar from '../Layouts/Navbar'
import MainBanner from '../HomeOne/MainBanner'
import Partner from '../Common/Partner'
import About from '../HomeOne/About'
import Services from '../HomeOne/Services'
import ChooseUs from '../HomeOne/ChooseUs'
import Video from '../HomeOne/Video'
import Projects from '../HomeOne/Projects'
import Testimonials from '../HomeOne/Testimonials'
import Pricing from '../Common/Pricing'
import Blog from '../Common/Blog'
import Footer from '../Layouts/Footer'

export default {
    name: 'HomePageOne',
    components: {
        Navbar,
        MainBanner,
        Partner,
        About,
        Services,
        ChooseUs,
        Video,
        Projects,
        Testimonials,
        Pricing,
        Blog,
        Footer,
    }
}

window.alert("Thank you for visiting us. Please note that we are busy updating this site. Alot of function wont be displayed well. We apologise for that.");
</script>