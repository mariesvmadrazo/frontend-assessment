<template>
  <div id="wrapper" class="w-100">
    <div id="hello-developer" class="w-100 d-flex flex-column justify-content-center text-white mb-5">
        <h1 class="text-bold">Hello Developer!</h1>
        <h3>Lorem ipsum dolor, sit amet consectetur adipisicing elit</h3>
    </div>
    <div id="cards-wrapper" class="px-5 d-flex flex-column flex-sm-row justify-content-center">
        <div class="card mx-4 mb-3" style="width: 18rem;" v-for="(c, i) in cards" :key="`card-${i+1}`">
            <img class="card-img-top" :src="require(`@/assets/${c.src}`)" alt="Card image cap">
            <div class="card-body">
                <p class="card-text">{{ c.text }}</p>
                <div role="button" class="text-bold rounded border border-dark cursor-pointer">READ MORE</div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            cards: [
                {
                    name: 'card 1',
                    src: '400x300.png',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum nisi illo dolor quia libero sapiente ex facere dolorum velit non magnam, quae quo beatae nemo quis voluptate molestiae perspiciatis ad provident voluptatibus, ullam exercitationem magni voluptates nihil. Nostrum, illum possimus eos a perferendis ea quod vel, corrupti ad fuga totam.'
                },
                {
                    name: 'card 2',
                    src: '400x300.png',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt quo eaque optio in voluptatem cumque error. Quia quaerat qui quis.'
                },
                {
                    name: 'card 3',
                    src: '400x300.png',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. A incidunt autem non nulla dignissimos harum laborum corporis magni eos officia, eligendi maiores cum nemo obcaecati nobis. Dignissimos optio aut eum?'
                }
            ]
        }
    }
}
</script>

<style scoped>
#hello-developer {
    background-repeat: no-repeat;
}

@media only screen and (max-width: 1920px) {
    #hello-developer {
        height: 650px;
        background-image: url('../assets/1920x650.png')
    }
}

@media only screen and (max-width: 600px) {
    #hello-developer {
        height: 600px;
        background-image: url('../assets/600x600.png')
    }
}
</style>