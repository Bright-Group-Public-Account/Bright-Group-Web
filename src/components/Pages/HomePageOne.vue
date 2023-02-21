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

<script type="application/ld+json">
import Navbar from '../Layouts/Navbar'
import MainBanner from '../HomeOne/MainBanner'
import Partner from '../Common/Partner'
import About from '../HomeOne/About'
import Services from '../HomeOne/Services'
import ChooseUs from '../AboutOne/ChooseUs'
import Video from '../HomeOne/Video'
import Projects from '../HomeOne/Projects'
// import Testimonials from '../HomeOne/Testimonials'
// import Pricing from '../Common/Pricing'
import Blog from '../Common/Blog'
import Footer from '../Layouts/Footer'

export default {
    // name: 'HomePageOne',
    components: {
        Navbar,
        MainBanner,
        Partner,
        About,
        Services,
        ChooseUs,
        Video,
        Projects,
        // Testimonials,
        // Pricing,
        Blog,
        Footer,
    },
    "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Bright Group Ltd",
  "image": "https://www.brightgroupltd.com/img/android-chrome-192x192.c3d2e03b.png",
  "@id": "",
  "url": "https://www.brightgroupltd.com",
  "telephone": "",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Century City",
    "addressLocality": "CapeTown",
    "postalCode": "7550",
    "addressCountry": ""
  },
  "openingHoursSpecification": {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": [
      "Monday",
      "Tuesday",
      "Wednesday",
      "Thursday",
      "Friday",
      "Saturday"
    ],
    "opens": "08:00",
    "closes": "16:00"
  },
}
</script>