<template>
        <nav id="sidebar" :class="{active:active}">
            <div class="sidebar-header">
                <h3>Sidebar Titile</h3>
            </div>
            <ul class="list-unstyled components">
                <p>Dummy Heading</p>
                <li>
                    <a href="#">About</a>
                </li>
                <li>
                    <a href="#">Portfolio</a>
                </li>
                <li>
                    <a href="#">Contact</a>
                </li>
            </ul>

        </nav>
</template>

<script>
export default {
    name:'sidebar',
    data(){
        return{
            active:true
        }
    },
    mounted(){
        this.$parent.$on('toggleNav',this.toggleNav)
    },
    methods:{
        toggleNav(){
            console.log('toggleNav')
            this.active=!this.active
        }
    }

}
</script>
