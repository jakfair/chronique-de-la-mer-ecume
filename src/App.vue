<template>
    <router-view id="app" v-slot="{ Component, route }">
        <transition name="route" mode="out-in"
                    @after-leave="onLeave">
            <div :key="route.name">
                <component :is="Component" @scrollHandle="handleScroll">
                    <template #nav>
                        <nav>
                            <router-link to="/">Home</router-link>
                            |
                            <router-link to="/about">About</router-link>
                        </nav>
                    </template>
                    <template #content></template>
                    <template #background>
                    </template>
                </component>
            </div>
        </transition>
    </router-view>
</template>

<script>
    export default {
        methods: {
            onLeave() {
                this.handleScroll()
            },
            handleScroll() {
                var scrollContent = document.getElementById('content').scrollTop;
                Array.from( document.getElementById('content').children).forEach(
                function (element) {
                    console.log(document.getElementById('content').children[0].getBoundingClientRect().y)
                    console.log(document.getElementById('content').children[0].className)
                    if(element.getBoundingClientRect().y < 500 && element.getBoundingClientRect().y > 140 && getComputedStyle(element).opacity  === '0') {
                        if(element.className === 'notshow') {
                            element.classList.replace('notshow','show')
                        } else {
                            element.classList.toggle('show')
                        }
                    }
                    if((element.getBoundingClientRect().y < 140 || element.getBoundingClientRect().y > 500) && element.className === 'show'){
                        element.classList.replace('show','notshow')
                    }
                });
                var iter = 0.1;
                Array.from(document.getElementsByClassName("background_image")).forEach(
                    function (element, index) {
                        element.style.transform = "translate(0," + ((iter*1000) - scrollContent * iter) + "px)";
                        if(index%2 === 0) {
                            iter = iter + 0.1;
                        }
                    });
            }
        },
        watch: {
            '$route': function (to, from) {
                if (from.name && document.getElementsByClassName("background_image")) {
                    Array.from(document.getElementsByClassName("background_image")).forEach(
                        function (element) {
                            var transformStyle = element.style.transform
                            const translateX = transformStyle.replace(/[^\d.]/g, '');
                            const translateX_Val = +translateX;

                            element.animate([
                                {transform: 'scale(1, 1) translate(0,' + translateX_Val + 'px)', opacity: 1},
                                {transform: 'scale(2, 2)', opacity: 0}
                            ], {
                                duration: 3000,
                                iterations: 1
                            });
                        }
                    );
                }
            }
        }
    }
</script>
<style>
    #app {
        position: relative;
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin: 0;
        overflow: hidden;
        height: 100vh;
    }

    #content {
        position: absolute;
        z-index: 2;
        height: 60vh;
        margin-left: 20vw;
        margin-right: 20vw;
        padding-top: 15vh;
        overflow-y: scroll;
        width: 60vw;
    }
    #content>* {
        opacity: 0;
        background-color: rgba(255, 255, 128, .5);
    }
    .show {
        opacity: 1 !important;
        transition: all 1s;
    }
    .notshow {
        opacity: 0 !important;
        transition: all 1s;
    }

    .background {
        position: absolute;
        z-index: 1;
    }

    .background_wrapper {
        width: 100vw;
        height: 100vh;
        position: relative;
        overflow: hidden;
    }

    .background_image, .background_image_fond {
        position: absolute;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
    }

    #bg_2, #bg_3, #bg_4, #bg_5, #bg_6, #bg_7 {
        transform: translate(0, 400px);
    }

    nav {
        padding: 30px;
        position: absolute;
        z-index: 2;
    }

    nav a {
        font-weight: bold;
        color: #2c3e50;
    }

    nav a.router-link-exact-active {
        color: #42b983;
    }

    .route-enter-from {
      opacity: 0;
    }

    .route-enter-active {
        transition: all 3s ease-out;
    }

    .route-leave-to {
      opacity: 0;
    }

    .route-leave-active {
        transition: all 3s ease-in;
    }

    /* Hide scrollbar for Chrome, Safari and Opera */
    .hidden-scrollbar::-webkit-scrollbar {
        display: none;
    }

    /* Hide scrollbar for IE, Edge and Firefox */
    .hidden-scrollbar {
        -ms-overflow-style: none; /* IE and Edge */
        scrollbar-width: none; /* Firefox */
    }
</style>
