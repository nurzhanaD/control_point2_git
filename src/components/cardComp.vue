<template>
        <div class="card border-info mb-3" style="width:60rem;min-height:30rem;">
            <div class="card-header" style="text-align:center;font-size:2rem;">{{title}}</div>
            <div class="card-body">
                <h4 class="card-title" style="text-align:center;">Info card theme</h4>
                <p class="card-text">Lorem ipsum, dolor sit amet consectetur adipisicing elit. 
                    Eveniet corrupti fuga iure fugiat nulla perspiciatis architecto beatae 
                    asperiores enim, voluptatem temporibus quae vero praesentium minus culpa 
                    iste eaque, quia pariatur officia explicabo facilis, aliquid vel voluptatum 
                    tenetur! Libero, ut! Voluptate expedita vitae sapiente animi blanditiis 
                    consequuntur id omnis cumque assumenda.</p>
            </div>
        </div>
</template>

<script>

export default {
    props:['title'],
    setup(props) {
        console.log(props.title)
    }
}
</script>

<style scoped>

</style>

