<template>
  <v-app theme="dark">
    <v-app-bar flat class="border-b">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-app-bar-title>Meu app</v-app-bar-title>

      <template #append>
        <v-btn icon class="mr-2">
          <v-badge dot color="info">
            <v-icon icon="mdi-bell-outline"></v-icon>
          </v-badge>
        </v-btn>
        
        <v-avatar>
          <v-img
            src="https://images.bstatic.de/lNmMYb-xM7RSPJJYShCcOKUK2T8=/480x480/filters:focal(2651x1564:2671x1584):format(webp)/images/41b2dc71/b1af/408b/8e53/cfb1e49c0221.jpg" 
            alt="Sheldon" 
            cover
          ></v-img>          
        </v-avatar>
      </template>
    </v-app-bar>

    <v-main>
      <v-container>
        <h1>Dashboard</h1>

        <v-row>
          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card>
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/3384815/pexels-photo-3384815.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"                
              >
                <v-card-title>Best Norway beaches</v-card-title>
              </v-img>
              
              <v-card-subtitle class="pt-3">Norway</v-card-subtitle>
              <v-card-text>                
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nobis sequi.</p>
              </v-card-text>

              <v-card-actions>
                <v-btn variant="outlined" color="primary">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" variant="tonal" color="primary">Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>     
          
          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card>
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/3384815/pexels-photo-3384815.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"                
              >
                <v-card-title>Best Norway beaches</v-card-title>
              </v-img>
              
              <v-card-subtitle class="pt-3">Norway</v-card-subtitle>
              <v-card-text>                
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nobis sequi.</p>
              </v-card-text>

              <v-card-actions>
                <v-btn variant="outlined" color="primary">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" variant="tonal" color="primary">Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>

          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card>
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/3384815/pexels-photo-3384815.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"                
              >
                <v-card-title>Best Norway beaches</v-card-title>
              </v-img>
              
              <v-card-subtitle class="pt-3">Norway</v-card-subtitle>
              <v-card-text>                
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nobis sequi.</p>
              </v-card-text>

              <v-card-actions>
                <v-btn variant="outlined" color="primary">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" variant="tonal" color="primary">Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>

          <v-col cols="12" sm="6" md="4" lg="3">
            <v-card>
              <v-img
                class="align-end text-white"
                src="https://images.pexels.com/photos/3384815/pexels-photo-3384815.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"                
              >
                <v-card-title>Best Norway beaches</v-card-title>
              </v-img>
              
              <v-card-subtitle class="pt-3">Norway</v-card-subtitle>
              <v-card-text>                
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nobis sequi.</p>
              </v-card-text>

              <v-card-actions>
                <v-btn variant="outlined" color="primary">Ver mais</v-btn>
                <v-btn prepend-icon="mdi-cart" variant="tonal" color="primary">Comprar</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
          
        </v-row>
      </v-container>
    </v-main>    
  </v-app>
</template>

<script setup>
  //
</script>
