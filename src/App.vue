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

        <v-menu>
          <template #activator="{ props }">
            <v-avatar v-bind="props">
              <v-img
                src="https://images.bstatic.de/lNmMYb-xM7RSPJJYShCcOKUK2T8=/480x480/filters:focal(2651x1564:2671x1584):format(webp)/images/41b2dc71/b1af/408b/8e53/cfb1e49c0221.jpg" 
                alt="Sheldon" 
                cover
              ></v-img>          
            </v-avatar>
          </template>
          
          <v-card min-width="200px">
            <v-list :lines="false" density="compact" nav >
              <v-list-item prepend-icon="mdi-account-outline">
                <v-list-item-title>Meu Perfil</v-list-item-title>
              </v-list-item>
              <v-list-item prepend-icon="mdi-heart-outline">
                <v-list-item-title>Favoritos</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-card>
        </v-menu>
      </template>
    </v-app-bar>

    <v-main>
      <v-container>
        <h1 class="mb-6">Dashboard</h1>

        <v-card flat class="border mb-4">
          <div class="d-flex justify-space-between">
            <v-card-title>Útimos usuários</v-card-title>

            <v-card-title>
              <v-btn @click="isDialogOpen = true" variant="tonal" size="small">Adicionar usuários</v-btn>

              <v-dialog v-model="isDialogOpen" width="600px">          

                <v-card>
                  <v-card-title>Adicionar usuário</v-card-title>

                  <v-card-text>
                    <v-row>
                      <v-col>
                        <v-text-field label="Nome" variant="outlined"></v-text-field>
                      </v-col>
                      <v-col>
                        <v-text-field 
                          label="Email" 
                          variant="outlined"
                          :rules="emailRules"
                        ></v-text-field>
                      </v-col>                      
                    </v-row>
                    <v-select 
                      label="Cargo" 
                      variant="outlined"
                      :items="['Admin', 'Gerente', 'Convidado']"
                    ></v-select>
                  </v-card-text>
                  <v-card-actions>
                    <v-btn variant="text" @click="isDialogOpen  = fasle">Cancelar</v-btn>
                    <v-btn variant="tonal" color="success">Salvar</v-btn>
                  </v-card-actions>
                </v-card>
              </v-dialog>
            </v-card-title>
          </div>          

          <v-table>
            <thead>
              <tr>
                <th>Nome</th>
                <th>Email</th>
                <th>Cargo</th>
                <th>Açoes</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Tiago</td>
                <td>tiago@gmail.com</td>
                <td>Adim</td>
                <td>
                  <v-dialog>
                    <template #activator="{props}">
                      <v-btn v-bind="props" variant="tonal" color="pimary" >EDITAR</v-btn>
                    </template>

                    <v-card>
                      <v-card-text>
                        Editar
                      </v-card-text>
                    </v-card>
                  </v-dialog>
                </td>
              </tr>
              <tr>
                <td>Pamela</td>
                <td>pamela@gmail.com</td>
                <td>Usuário</td>
                <td>
                  <v-btn variant="tonal" color="pimary" >EDITAR</v-btn>
                </td>
              </tr>
              <tr>
                <td>Joao</td>
                <td>pamela@gmail.com</td>
                <td>Usuário</td>
                <td>
                  <v-btn variant="tonal" color="pimary" >EDITAR</v-btn>
                </td>
              </tr>
            </tbody>
          </v-table>
        </v-card>

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
  import { ref } from 'vue';

  const isDrawerOpen = ref(false)
  const isDialogOpen = ref(false)
  const emailRules = [
    value => {
      if (value) return true
      return 'O email é obrigatório'
    },
    value => {
      if(value.includes('@')) return true
      return 'Email inválido!'
    }
  ]
</script>
