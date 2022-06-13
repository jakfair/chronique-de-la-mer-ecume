<template>
    <slot name="summary"></slot>
    <slot name="nav"></slot>
    <slot name="content">
        <div class="home hidden-scrollbar text-center" id="content" @scroll="$emit('scrollHandle')">
            <h1 class="h1" id="titre">Les chroniques de la mer d'Écume</h1>
            <p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent nunc diam, facilisis nec blandit quis,
                scelerisque ut erat. Praesent quam libero, aliquam non metus et, hendrerit sodales justo. Maecenas vel
                mattis ex, at pellentesque erat. Etiam maximus velit sem, eu viverra massa hendrerit quis. In lobortis
                faucibus pretium. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed et rhoncus ipsum.
                Curabitur eget pellentesque urna, at suscipit risus. Pellentesque luctus rutrum scelerisque. Mauris
                tristique gravida dolor, sed faucibus nunc luctus ac. Maecenas aliquam lacus odio, a molestie mi
                scelerisque vel. Proin tristique leo eget diam dapibus, et egestas erat dapibus. Suspendisse in
                scelerisque ligula. Sed fermentum tincidunt ipsum. In in leo id leo tempus laoreet.
            </p>
            <p> Nulla tincidunt mattis tellus. Donec ut neque lacinia, rhoncus lectus in, mollis tortor. Sed turpis
                nisl, sagittis id fermentum eu, eleifend vitae nisl. Vestibulum egestas mattis elementum. Integer
                volutpat velit nibh, eu porta lorem commodo vitae. Vivamus rutrum sagittis nisl. In porta tincidunt sem
                non euismod. Duis volutpat posuere neque, in suscipit enim pulvinar in. Vivamus leo orci, lobortis
                vehicula odio quis, suscipit auctor justo. Suspendisse potenti. Vivamus eget metus eget dui varius
                posuere pharetra nec diam. Curabitur tincidunt varius urna at feugiat. Praesent fermentum leo sit amet
                metus pellentesque, nec egestas massa pharetra. In et orci purus. Vivamus id nisi consequat urna posuere
                ullamcorper et non magna. Etiam feugiat varius varius.
            </p>
            <p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent nunc diam, facilisis nec blandit quis,
                scelerisque ut erat. Praesent quam libero, aliquam non metus et, hendrerit sodales justo. Maecenas vel
                mattis ex, at pellentesque erat. Etiam maximus velit sem, eu viverra massa hendrerit quis. In lobortis
                faucibus pretium. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed et rhoncus ipsum.
                Curabitur eget pellentesque urna, at suscipit risus. Pellentesque luctus rutrum scelerisque. Mauris
                tristique gravida dolor, sed faucibus nunc luctus ac. Maecenas aliquam lacus odio, a molestie mi
                scelerisque vel. Proin tristique leo eget diam dapibus, et egestas erat dapibus. Suspendisse in
                scelerisque ligula. Sed fermentum tincidunt ipsum. In in leo id leo tempus laoreet.
            </p>
            <p> Nulla tincidunt mattis tellus. Donec ut neque lacinia, rhoncus lectus in, mollis tortor. Sed turpis
                nisl, sagittis id fermentum eu, eleifend vitae nisl. Vestibulum egestas mattis elementum. Integer
                volutpat velit nibh, eu porta lorem commodo vitae. Vivamus rutrum sagittis nisl. In porta tincidunt sem
                non euismod. Duis volutpat posuere neque, in suscipit enim pulvinar in. Vivamus leo orci, lobortis
                vehicula odio quis, suscipit auctor justo. Suspendisse potenti. Vivamus eget metus eget dui varius
                posuere pharetra nec diam. Curabitur tincidunt varius urna at feugiat. Praesent fermentum leo sit amet
                metus pellentesque, nec egestas massa pharetra. In et orci purus. Vivamus id nisi consequat urna posuere
                ullamcorper et non magna. Etiam feugiat varius varius.
            </p>
            <p> Donec sed nulla dolor. Vivamus hendrerit, nulla sed placerat feugiat, erat risus tristique sapien, ac
                venenatis erat ipsum a erat. Morbi volutpat ullamcorper augue eget posuere. Proin nec luctus orci, ac
                pellentesque leo. Fusce tincidunt dapibus quam vitae efficitur. Suspendisse eget accumsan urna, vel
                posuere metus. Integer vel mollis dolor, et euismod ipsum. Praesent eu ullamcorper odio. Ut at dui arcu.
                Sed in eros id urna semper efficitur. Pellentesque posuere risus mi. Cras pulvinar sagittis dictum.
                Integer a nunc nec ipsum vulputate facilisis et nec lacus. Ut ultrices porttitor dapibus. Proin
                consequat ex at purus interdum feugiat.
            </p>
          <h1 class="h1" id="titre2">Deuxième Partie</h1>
            <p> Aliquam faucibus pulvinar magna quis commodo. Sed vel lacinia quam. Morbi faucibus congue sapien id
                imperdiet. Suspendisse sapien turpis, ultrices non imperdiet vel, rutrum ut lacus. Phasellus sit amet
                dapibus velit, et pretium eros. Suspendisse purus felis, sodales eu auctor non, luctus faucibus justo.
                Vestibulum tempor sit amet elit ac tincidunt. Etiam libero lorem, gravida nec velit non, maximus ornare
                mauris. Pellentesque scelerisque mi et magna interdum tempus. Nulla condimentum nulla in urna vestibulum
                lacinia. Praesent sit amet sagittis nibh, in tincidunt arcu.
            </p>
            <p> Integer porta consequat turpis, nec ultrices ex sodales ac. Nam non eros elementum, vehicula tellus
                eget, pulvinar eros. Nullam metus nisl, lobortis sed diam nec, mollis tempus leo. Donec tempus volutpat
                nisi. Nullam non felis eu eros eleifend pretium at id tortor. Donec vitae eros felis. In sapien felis,
                dictum id lacinia id, sollicitudin eget mi. Donec dapibus sed nibh sit amet sollicitudin. Vivamus a
                turpis purus. Suspendisse sollicitudin tristique dolor ac semper. Aliquam at molestie justo. Aliquam
                ullamcorper elit tortor, nec varius lacus volutpat a. Sed commodo tellus lacus, luctus ullamcorper metus
                elementum quis. Aenean semper semper tellus.
            </p>
            <p> Nam eget eros odio. Fusce in ex augue. Proin placerat eros sed consequat semper. Curabitur orci erat,
                fermentum vitae rhoncus nec, laoreet sed nunc. Pellentesque non semper sapien, non laoreet turpis. Morbi
                non pretium mi. Mauris blandit ipsum dictum ex faucibus convallis. Vestibulum vel diam ex. Aliquam
                luctus pellentesque suscipit.
            </p>
          <h1 class="h1" id="titre3">Troisième Partie</h1>
          <p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent nunc diam, facilisis nec blandit quis,
            scelerisque ut erat. Praesent quam libero, aliquam non metus et, hendrerit sodales justo. Maecenas vel
            mattis ex, at pellentesque erat. Etiam maximus velit sem, eu viverra massa hendrerit quis. In lobortis
            faucibus pretium. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed et rhoncus ipsum.
            Curabitur eget pellentesque urna, at suscipit risus. Pellentesque luctus rutrum scelerisque. Mauris
            tristique gravida dolor, sed faucibus nunc luctus ac. Maecenas aliquam lacus odio, a molestie mi
            scelerisque vel. Proin tristique leo eget diam dapibus, et egestas erat dapibus. Suspendisse in
            scelerisque ligula. Sed fermentum tincidunt ipsum. In in leo id leo tempus laoreet.
          </p>
          <p> Nulla tincidunt mattis tellus. Donec ut neque lacinia, rhoncus lectus in, mollis tortor. Sed turpis
            nisl, sagittis id fermentum eu, eleifend vitae nisl. Vestibulum egestas mattis elementum. Integer
            volutpat velit nibh, eu porta lorem commodo vitae. Vivamus rutrum sagittis nisl. In porta tincidunt sem
            non euismod. Duis volutpat posuere neque, in suscipit enim pulvinar in. Vivamus leo orci, lobortis
            vehicula odio quis, suscipit auctor justo. Suspendisse potenti. Vivamus eget metus eget dui varius
            posuere pharetra nec diam. Curabitur tincidunt varius urna at feugiat. Praesent fermentum leo sit amet
            metus pellentesque, nec egestas massa pharetra. In et orci purus. Vivamus id nisi consequat urna posuere
            ullamcorper et non magna. Etiam feugiat varius varius.
          </p>
          <p> Donec sed nulla dolor. Vivamus hendrerit, nulla sed placerat feugiat, erat risus tristique sapien, ac
            venenatis erat ipsum a erat. Morbi volutpat ullamcorper augue eget posuere. Proin nec luctus orci, ac
            pellentesque leo. Fusce tincidunt dapibus quam vitae efficitur. Suspendisse eget accumsan urna, vel
            posuere metus. Integer vel mollis dolor, et euismod ipsum. Praesent eu ullamcorper odio. Ut at dui arcu.
            Sed in eros id urna semper efficitur. Pellentesque posuere risus mi. Cras pulvinar sagittis dictum.
            Integer a nunc nec ipsum vulputate facilisis et nec lacus. Ut ultrices porttitor dapibus. Proin
            consequat ex at purus interdum feugiat.
          </p>
          <p> Donec sed nulla dolor. Vivamus hendrerit, nulla sed placerat feugiat, erat risus tristique sapien, ac
            venenatis erat ipsum a erat. Morbi volutpat ullamcorper augue eget posuere. Proin nec luctus orci, ac
            pellentesque leo. Fusce tincidunt dapibus quam vitae efficitur. Suspendisse eget accumsan urna, vel
            posuere metus. Integer vel mollis dolor, et euismod ipsum. Praesent eu ullamcorper odio. Ut at dui arcu.
            Sed in eros id urna semper efficitur. Pellentesque posuere risus mi. Cras pulvinar sagittis dictum.
            Integer a nunc nec ipsum vulputate facilisis et nec lacus. Ut ultrices porttitor dapibus. Proin
            consequat ex at purus interdum feugiat.
          </p>
        </div>
    </slot>
    <slot name="background">
        <div class="background" v-bind="$attrs">
            <div class="background_wrapper">
                <img class="background_image_fond" src="~@/assets/fond_montagne/sky.png"/>
                <img class="background_image" src="~@/assets/fond_montagne/cloud_lonely.png"/>
                <img class="background_image" src="~@/assets/fond_montagne/clouds_bg.png"/>
                <img class="background_image" src="~@/assets/fond_montagne/glacial_mountains.png"/>
                <img class="background_image" src="~@/assets/fond_montagne/clouds_mg_3.png"/>
                <img class="background_image" src="~@/assets/fond_montagne/clouds_mg_2.png"/>
                <img class="background_image" src="~@/assets/fond_montagne/clouds_mg_1.png"/>
            </div>
        </div>
    </slot>
</template>

<script>

    export default {
        name: 'HomeView',
    }
</script>
