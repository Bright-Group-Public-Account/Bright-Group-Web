<template>
    <div class="about-area ptb-100">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6 col-md-12">
                    <div class="about-image" data-tilt>
                        <img src="../../assets/images/about/about.png" alt="image" data-aos="fade-down" data-aos-delay="80" data-aos-duration="800" data-aos-once="true">
                    </div>
                </div>
                <div class="col-lg-6 col-md-12">
                    <div class="about-content" data-aos="fade-up" data-aos-delay="80" data-aos-duration="800" data-aos-once="true">
                        <span>WHO WE ARE</span>
                        <h3>Solution <b>&amp;</b> Technology Company</h3>
                        <p>Get the edge you need to propel your business forward with our cutting-edge IT <strong>Services</strong> and <strong>Technologies</strong>. Rest assured that you'll be working with a <strong>Reliable</strong> and <strong>Top Notch</strong> company.</p>
                        <div class="about-btn">
                            <router-link to="about" class="default-btn">
                                Know More About Us
                            </router-link>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="about-shape-1">
            <img src="../../assets/images/about/about-shape.png" alt="image">
        </div>
    </div>
</template>

<script>
export default {
    name: 'About'
}
</script>