<template>
<div class="main_header">
    <div class="main_header_logo">
        <b style="color:red;">VN</b>REVOLUTION
    </div>

    <div class="main_header_links" :class="{ 'show_menu': isShow }">
        <ul class="main_header_links_items">
            <li class="main_header_links_items_item">Home</li>
            <li class="main_header_links_items_item sub_menu">Boss
                <ul class="main_header_links_items_item_sub_items">
                    <li class="main_header_links_items_item_sub_item "> Kanto</li>
                    <li class="main_header_links_items_item_sub_item ">Johto</li>
                    <li class="main_header_links_items_item_sub_item ">Hoen</li>
                    <li class="main_header_links_items_item_sub_item ">Sinnoh</li>
                </ul>
            </li>
            <li class="main_header_links_items_item">Tricks</li>
            <li class="main_header_links_items_item">Storys</li>
            <li class="main_header_links_items_item">Events</li>
            <li class="main_header_links_items_item sub_menu">Pokemons
                <ul style="width:210px" class="main_header_links_items_item_sub_items">
                    <li class="main_header_links_items_item_sub_item">Team Pro Build</li>
                    <li class="main_header_links_items_item_sub_item">Phân tích Pokemons</li>
                </ul>
            </li>
        </ul>
    </div>
    <div class="responsive_buger" @click="showMenu">

        <span class="iconify" data-icon="bx:bx-menu-alt-right" data-inline="false"></span>
    </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            isShow: false,
            width: '',

        }
    },
    methods: {
        showMenu() {
            this.isShow = !this.isShow
        },
        handleResize() {
            this.width = window.innerWidth;
        }
    },
    created() {
        window.addEventListener('resize', this.handleResize);
        this.handleResize();
    },
    destroyed() {
        window.removeEventListener('resize', this.handleResize);
    },
    watch: {
        width: {
            // This will let Vue know to look inside the array
            deep: true,

            // We have to move our method to a handler field
            handler(newValue) {

                // console.log(newValue);
                // newValue >= 900 ? this.isShow = true : this.isShow = false
                // console.log(this.isShow)
            }
        }
    }

}
</script>

<style lang="scss" scoped>
.main_header {
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
    width: 100vw;
    height: 80px;

    font-size: 18px;

    box-shadow: 0 4px 12px 0 rgba(0, 0, 0, 0.05);

    .main_header_logo {
        font-weight: bold;
        font-family: 'Overpass Mono', monospace;
    }

    .main_header_links {
        .main_header_links_items {

            display: flex;
            align-items: center;
            justify-content: space-between;
            list-style: none;
            cursor: pointer;

            .main_header_links_items_item {
                width: 80px;
                font-family: 'Overpass Mono', monospace;
                font-weight: 600;
                line-height: 24px;
                font-size: 16px;
                letter-spacing: 1px;

                &:hover {
                    .main_header_links_items_item_sub_items {
                        display: block;
                        transition: .5s ease-in all;

                    }
                }

                .main_header_links_items_item_sub_items {
                    cursor: pointer;
                    // background:white;
                    position: absolute;
                    left: 0;
                    top: 10;
                    display: flex;
                    flex-direction: column;
                    align-items: flex-start;
                    justify-content: flex-start;
                    list-style: none;
                    padding: 15px 10px;
                    padding-left: 0;
                    display: none;
                    z-index: 2;

                    .main_header_links_items_item_sub_item {
                        font-size: 15px;
                        &:hover {
                            background: rgba(0, 0, 0, .8);
                            color: rgba(255, 255, 255, .8);
                            transition: background .1s ease-out;
                        }
                    }
                }

            }

            .sub_menu {
                position: relative;
            }
        }
    }

    .responsive_buger {
        display: none;
        font-size: 25px;
        margin-bottom: 10px;
        z-index: 555;

    }

}
</style>
