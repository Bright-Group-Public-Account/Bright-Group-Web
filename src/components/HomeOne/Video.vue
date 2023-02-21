<template>
    <div>
        <div class="video-area">
            <div class="container">
                <div class="video-view-content" data-aos="fade-up" data-aos-delay="80" data-aos-duration="800" data-aos-once="true">
                    <div class="video-image">
                        <img src="../../assets/images/video/video.jpg" alt="image">
                    </div>

                    <a 
                        href="javascript:void(0)" 
                        v-on:click="isPopupMethod(isPopup)" 
                        class="video-btn popup-youtube"
                    >
                        <i class="ri-play-fill"></i>
                    </a>
                </div>
            </div>
        </div>

        <div 
            class="popup-video" 
            v-if="isPopup"
        >
            <div class="d-table">
                <div class="d-table-cell">
                    <div 
                        class="popup-overlay-close"
                        v-on:click="isPopupMethod(isPopup)"
                    >
                        <div class="popup-overlay-close-line"></div>
                        <div class="popup-overlay-close-line"></div>
                    </div>
                    <div class="play-video">
                        <iframe src="https://www.facebook.com/plugins/video.php?height=452&href=https%3A%2F%2Fwww.facebook.com%2Fbrightgroupfb%2Fvideos%2F2844999089089155%2F&show_text=false&width=560&t=0"
                        width="560" height="452" style="border:none;overflow:hidden" scrolling="no" 
                        allow="autoplay; clipboard-write;encrypted-media; picture-in-picture; web-share" allowFullScreen="true"></iframe>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Video',
    data (){
        return {
            isPopup: false,
        }
    },
    methods: {
        isPopupMethod(isPopup){
            return this.isPopup = !isPopup
        },
    },
}
</script>