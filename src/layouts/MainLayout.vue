<template>
  <q-layout view="LHh Lpr lFf" class="bg-white">
    <div>
      <q-header elevated
        style="height: 150.0">
        <q-toolbar class="justify-between">      
          <div class="col-4">
            <q-btn
            flat
            dense
            round
            @click="leftDrawerOpen = !leftDrawerOpen"
            aria-label="Menu"
            icon="menu"
          />   
          </div>     
          <div class="col-md-4 offset-md-4 q-mr-xs">
            <q-btn 
            type="a"
            href="http://wa.link/8phs9s"
            target="_blank"
            round 
            color="positive" 
            icon="chat" 
            />    
            <q-btn 
            type="a"
            href="https://www.facebook.com/groups/2739741569616794/?ref=share"
            target="_blank"
            round 
            color="blue-8" 
            icon="facebook" 
            />    
            <q-btn 
            type="a"
            href="https://youtube.com/user/merry1669"
            target="_blank"
            round 
            color="negative" 
            icon="subscriptions" 
            />    
            <q-btn 
            type="a"
            href="http://www.twitch.tv/dantemex91?sr=a"
            target="_blank"
            round 
            color="indigo" 
            icon="format_quote" 
            />    
            <q-btn 
            type="a"
            href="https://joelge08.wixsite.com/gamer360zone"
            target="_blank"
            round 
            color="white" 
            text-color="blue-10"
            icon="public" 
            />    
            <q-btn 
            type="a"
            href="https://www.paypal.me/joel1891"
            target="_blank"
            round 
            color="indigo" 
            icon="redeem" 
            />
          </div>      
        </q-toolbar>
        <div class="q-px-lg q-pt-xl q-mb-md">
          <div>
            <q-toolbar-title class="title">
              Gamers<span class="x360">360</span>Zone
            </q-toolbar-title>
          </div>
          <div>
            <q-toolbar-subtitle class="subtitle">
              Todo el contenido en la palma de tu mano.
            </q-toolbar-subtitle>
          </div>
        </div>
        <q-img
          src="../statics/bg-wall.jpg"
          class="header-image absolute-top">
        </q-img>
      </q-header>
    </div>

    <q-drawer
        v-model="leftDrawerOpen"
        :width="300"
        :breakpoint="600"
        elevated
        content-class="bg-teal-4"
      >
        <q-scroll-area style="height: calc(100% - 150px); margin-top: 150px">
          <q-list padding>
            <div v-for="section in menuSections">
              <q-item 
                clickable 
                tag="a" 
                target="_blank" 
                rel="noopener" 
                :href="section.link">
                <q-item-section avatar>
                  <q-icon :name="section.icon"/>
                </q-item-section>
                <q-item-section>
                  <q-item-label>{{section.name}}</q-item-label>
                  <q-item-label caption>{{section.caption}}</q-item-label>
                </q-item-section>
              </q-item>
            </div>            
          </q-list>
        </q-scroll-area>

        <q-img 
          class="absolute-top" 
          src="../statics/bg-wall.jpg" 
          style="height: 150px">
          <div class="absolute-bottom bg-transparent">
            <q-avatar size="56px" class="q-mb-sm">
              <img src="../statics/avatar.jpeg">
            </q-avatar>
            <div class="text-weight-bold subtitle">¡Bienvenidos Gamers!</div>
            <!-- <div>@rstoenescu</div> -->
          </div>
        </q-img>
      </q-drawer>

    <q-page-container style="background-color: black">
      <!-- <div style="background-color: black">
        <!-- <q-parallax src="../statics/bg-gamer.jpg" class="bg-page">
          <router-view />
        </q-parallax> -->
        
          <router-view />
      <!-- </div> -->
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MyLayout',
  data () {
    return {
      leftDrawerOpen: false,
      menuSections: [
        // {name: 'Inicio', link: '', caption: "", icon: "home"},
        {name: 'Apps Xbox 360', link: 'https://joelge08.wixsite.com/gamer360zone/app-xbox-360', caption: "Administra tu consola", icon: "build"},
        {name: 'Juegos Xbox 360 RGH', link: 'https://joelge08.wixsite.com/gamer360zone/juegos-xbox-rgh', caption: "Los mejores juegos", icon: "sports_esports"},
        {name: "DLC's Xbox 360 RGH", link: 'https://joelge08.wixsite.com/gamer360zone/dlc-xbox-360', caption: "Contenido extra descargable", icon: "extension"},
        {name: 'Apps Android', link: 'https://joelge08.wixsite.com/gamer360zone/actualizacion-17599', caption: "Aplicaciones para tu móvil", icon: "android"},
        {name: 'Servers', link: 'https://joelge08.wixsite.com/gamer360zone/servers', caption: "Juega on-line!", icon: "dns"},
        {name: 'Emuladores', link: 'https://joelge08.wixsite.com/gamer360zone/emuladores', caption: "Los mejores emuladores para Xbox", icon: "videogame_asset"},
        // {name: 'Play Station 3', link: '', caption: "Apartado en construcción...", icon: "play_arrow"},
        {name: 'Programas de PC', link: 'https://joelge08.wixsite.com/gamer360zone/programas-pc', caption: "Aplicaciones útiles", icon: "desktop_windows"},
        {name: 'Tutoriales', link: 'https://joelge08.wixsite.com/gamer360zone/tutoreales', caption: "Aprende con nosotros", icon: "school"},
      ],
    }
  }
}
</script>

<style lang="scss">
  .header-image {
    height: 100%;
    z-index: -1;
    opacity: 0.7;
  }

  .bg-page {
    opacity: 0.5;
    filter: grayscale(50%);
  }
  .title{
    text-shadow: 3px 3px 5px rgb(255, 0, 0);
    font-weight: bold;
  }

  .subtitle{
    text-shadow: 3px 3px 8px white;
  }

  .x360 {
    color: rgb(18, 219, 18);
    text-shadow: 3px 3px 2px rgb(12, 148, 12);
    font-size: 1.5em;
  }

</style>