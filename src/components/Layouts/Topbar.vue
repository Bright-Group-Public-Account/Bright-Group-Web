<template>
    <div class="topbar-area">
        <div class="container-fluid">
            <div class="row align-items-center">
                <div class="col-lg-9 col-md-9">
                    <ul class="topbar-information">
                        <li>
                            <i class="ri-phone-line"></i>
                            <span>Phone: <a href="tel:9901234567">+27 65 813 0434</a></span>
                        </li>
                        <li>
                            <i class="ri-mail-line"></i>
                            <span>Mail: <a href="mailto:info@brightgroupltd.com">info@brightgroupltd.com</a></span>
                        </li>
                        <li>
                            <i class="ri-map-pin-line"></i>
                            <span>Address:</span> Century City, Cape Town
                        </li>
                    </ul>
                </div>

                <div class="col-lg-3 col-md-3">
                    <ul class="topbar-action">
                        <li class="dropdown language-option">
                            <button 
                                class="dropdown-toggle"
                                @click="show = !show"
                                :aria-pressed="show ? 'true' : 'false'"
                                v-bind:class="{ show: button_show_state }"
                                v-on:click="button_show_state = !button_show_state"
                            >
                                <img
                                    :src="image"
                                    alt="image"
                                />
                                {{name}}
                            </button>
                            <div 
                                class="dropdown-menu language-dropdown-menu" 
                                :class="{ toggler: show }"
                            >
                                <div v-if="newData.length > 0">
                                    <a 
                                        class="dropdown-item" 
                                        href="#"
                                        v-for="data in newData" 
                                        :key="data.id"
                                    >
                                        <div 
                                            v-on:click="toggleSelected(data), 
                                            show = !show"
                                        >
                                            <img
                                                :src="data.image"
                                                alt="image"
                                            />
                                            {{data.name}}
                                        </div>
                                    </a>
                                </div>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Topbar',
	data: () => ({
		show: false,
		active: false,
        button_show_state: false,
		newData: [
            {
                id: '',
                image: require('../../assets/images/uk.png'),
                name: 'ENG',
            },
            {
                id: '',
                image: require('../../assets/images/china.png'),
                name: '????????????',
            },
            {
                id: '',
                image: require('../../assets/images/uae.png'),
                name: '????????????????',
            }
        ],
		name: "ENG",
		image: require("../../assets/images/uk.png"),
        clicked: false
	}),

    methods: {
        toggleSelected(select, index){
            if(this.clicked === index){
                this.clicked = null
            }

            this.clicked = index 
            this.name = select.name 
            this.image = select.image
        }
    }
}
</script>