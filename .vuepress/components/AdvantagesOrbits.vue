<template>
    <div class="orbits">
        <ul class="advantages"
            :style="{'background-image': 'url('+ $withBase('/img/Technical_Advantages_Section_Graphic2.svg') +')', 'background-size':'contain'}">
            <li v-for="advantage in advantages">
                <div :style="{'background-image': 'url('+ $withBase(advantage.image) +')'}"></div>
                <div>{{ advantage.text }}</div>
            </li>
        </ul>
    </div>
</template>
<script>
    export default {
        computed: {
            advantages() {
                return this.$page.frontmatter.advantages;
            }
        }
    }
</script>
