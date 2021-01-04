<template>
<div class="main_header">
    <div class="main_header_logo">
        <!-- with star -->
        <!-- <b style="color:red;">VN</b>REVOLUTION <span style="background:red; padding:2px 3px"> ⭐ </span> -->
        <!-- aaa123 -->
        <b style="color:red;">VN</b>REVOLUTION
    </div>
    <div class="main_header_links">
        <ul class="main_header_links_items">
            <li class="main_header_links_items_item">Home</li>
            <li class="main_header_links_items_item">Boss</li>
            <li class="main_header_links_items_item">Tricks</li>
            <li class="main_header_links_items_item">Storys</li>
            <li class="main_header_links_items_item">Events</li>
        </ul>
    </div>
</div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.main_header {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100vw;
    height: 100px;
    background: #FFFFFF;
    font-size: 18px;
    border-bottom: 1px solid #DDDDDD;
    -webkit-box-shadow: 0 10px 6px -6px #777;
    -moz-box-shadow: 0 10px 6px -6px #777;
    box-shadow: 0 5px 6px -6px #777;

    .main_header_logo {
        font-weight: bold;
        font-family: 'Overpass Mono', monospace;
    }

    .main_header_links {
        margin-left: 315px;

        .main_header_links_items {
            display: flex;
            align-items: center;
            justify-content: space-between;
            list-style: none;

            .main_header_links_items_item {
                width: 80px;
                font-family: 'Overpass Mono', monospace;
                font-weight: 600;
                line-height: 24px;
                font-size: 16px;
                letter-spacing: 1px;

            }
        }
    }
}
</style>
