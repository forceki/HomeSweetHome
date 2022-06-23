<template>
<section id="navbar">
    <v-container fluid class="ma-0 pa-0">
      <v-app-bar elevation="0" color="white">
        <v-container class="d-flex align-center px-0 px-sm-3">
         <a href=""> logo </a>

          <v-spacer></v-spacer>

          <v-toolbars>
            <v-toolbar-items class="text-decoration-none hidden-xs-only d-sm-flex">
              <a class="d-flex pl-10 justify-center align-center text-decoration-none black--text" v-for="(toolbar , i) in linkbar" :key="i">
                {{ toolbar.title }}
              </a>
            </v-toolbar-items>

      
               <v-btn
                  class="hidden-sm-and-up pl-4"
                  icon
                  @click="Clicklist = !Clicklist"
                >
                   <v-icon color="black"> mdi-menu</v-icon>
             </v-btn>
          </v-toolbars>
          
        </v-container>
      </v-app-bar>    

    </v-container>
        <v-navigation-drawer
          v-model="Clicklist"
          temporary
          fixed    
          width="185px"
        >
      

          <v-list-item class="d-flex justify-center mt-5">
         
           <v-avatar size="70" tile><v-img max-width="120px" src="img/Asset/logo.png"></v-img></v-avatar>
        
          </v-list-item>
           <v-list-item-title class="d-flex justify-center mt-1 mb-3 text-h6"><p class="mb-0 font-weight-bold"> Savikindo</p></v-list-item-title>

   
          <v-divider></v-divider>

          <v-list dense class="mt-4">
            <v-list-item link>
                <v-icon  color="black" small> mdi-home</v-icon>
                <v-items class="pl-3" @click="scrollToHome() ; CloseNavbar()"><p class="mb-0"> Home</p></v-items>
            </v-list-item>
            <!-- <v-list-item link>
                <v-icon color="black" small> mdi-cog</v-icon>
                <v-items class="pl-3" @click="scrollToServices() ; CloseNavbar()"><p class="mb-0">Services</p></v-items>
            </v-list-item>
            <v-list-item link>
                <v-icon color="black" small> mdi-account-group</v-icon>
                <v-items class="pl-3" @click="scrollToClients() ; CloseNavbar()"><p class="mb-0">Clients</p></v-items>
            </v-list-item>
            <v-list-item link>
                <v-icon color="black" small> mdi-phone</v-icon>
                <v-items class="pl-3" @click="scrollToContactUs() ; CloseNavbar()"> <p class="mb-0">Contact Us</p></v-items>
            </v-list-item> -->
          </v-list>
        </v-navigation-drawer>
</section>
</template>

<script>

export default {
    
    name:"avbarVue",
    data() {
      return {
      drawer:null,
      Clicklist:false,
      linkbar: [
        { title: "Home", icon: "mdi-home", link: "/" },
        { title: "About", icon: "mdi-cog", link: "/about" },
        { title: "Member", icon: "mdi-account-group", link: "/member" },
        { title: "Moments", icon: "mdi-phone", link: "/moments" },
      ],
    };
  },
  methods: {
    
    scrollToHome() {document.getElementById("home").scrollIntoView({ behavior: "smooth" });
    this.Clicklist = false;
    },
    scrollToServices() {document.getElementById("service").scrollIntoView({ behavior: "smooth" });
    this.Clicklist = false;
    },
    scrollToClients() {document.getElementById("ourclient").scrollIntoView({ behavior: "smooth" });
     this.Clicklist = false;
    },
    scrollToContactUs() {document.getElementById("contactus").scrollIntoView({ behavior: "smooth" });
    this.Clicklist = false;
    },
     CloseNavbar () {
      this.Clicklist = false;
    },
  },
};
</script>

<style>
v-items {
  font-family: PoppinsSemiBold;

}
v-div{
  font-family: PoppinsBold;
}

.v-toolbar__content {
  padding: 4px 12px 4px 12px !important;
}
v-items {
  color: black;
  transition: 0.5s;
  width: 90px;
  font-size: 14px;
}
v-items:hover{
  font-size: 16px;
  transition: 0.5s;
}
@media (max-width:600px) {
  v-items p {
  color: black;
  transition: 0.5s;
  width: 90px;
  font-size: 13px;
}
v-items p:hover{
  font-size: 13px;
}
}
</style>