<template>
    <ion-page>
      <ion-header :translucent="true">
        <ion-toolbar>
          <ion-title>Carrito de compra</ion-title>
        </ion-toolbar>
      </ion-header>
  
      <ion-content :fullscreen="true">
        <ion-header collapse="condense">
          <ion-toolbar>
            <ion-title size="large">Login</ion-title>
          </ion-toolbar>
        </ion-header>
        <div id="login-container">
          <img src="\resources\icon.png" alt="Imagen de carrito de compra" id="cart-image" />
        
          <div id="description">
            <p>Bienvenido al carrito de compra. Por favor, inicia sesión para continuar.</p>
          </div>
        
         
  
          <div>
            <InputComponent id="user" name="Nombre" label="Nombre: " />
            <InputComponent id="user" name="apellido" label="apellido: " />
            <InputComponent type="number" id="tel" name="Celular" label="Celular: " />
            <InputComponent type="email" id="email" name="correo" label="Email: " />
            <InputComponent type="date" id="date" name="FechadeNacimiento" />
            <br>
            <ButtonComponent id="login" value="Consultar" fill="outline" />
            <ButtonComponent id="save" value="Guardar" fill="outline" color="success"/>
            <ButtonComponent id="update" value="Modificar" fill="outline" color="warning"/>
            <ButtonComponent id="delete" value="Borrar" fill="outline" color="danger"/>
          </div>
          <ion-button id="present-alert">ToKaMe</ion-button>
    <ion-alert
      trigger="present-alert"
      header="peligro"
      sub-header="Registro completado"
      message="toda tu informacion quedo registrada."
      :buttons="alertButtons"
    ></ion-alert>
      
        </div>
      </ion-content>
    </ion-page>
  </template>
  
  
  <script setup lang="ts">
  import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar,IonAlert, IonButton } from '@ionic/vue';
  import ButtonComponent from '@/components/ButtonComponent.vue';
  import InputComponent from '@/components/InputComponent.vue';
  const alertButtons = ['Action'];
  
  </script>
  
  <style scoped>
  #login-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
  }
  
  #cart-image {
    margin-bottom: 20px;
    width: 100px;
  }
  
  #description {
    margin-bottom: 20px;
    text-align: center;
  }
  
  #description p {
    margin: 0;
    padding: 10px; 
  }
  
  #login-form {
    max-width: 300px;
    width: 100%;
  }
  </style>