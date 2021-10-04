<template>
  <div class="market">
    <div class="notification">
        10
    </div>      
  </div>
</template>

<script>
export default {

}
</script>

<style>
    .market{
        width: 80px;
        height: 80px;
        border-radius: 50%;
        background-image: url("../assets/carrito-de-compras.png");
        background-repeat: no-repeat;
        background-position:50% 50%;
        background-size: 60px;                
        background-color: rgba(28, 62, 172, 0.555);
        position: sticky;
        top: 8%;
        left: 92%;
    }

    .notification{                
        width: 25%;
        height: 25%;
        border-radius: 50%;
        background-color: red;
        color: aliceblue;        
    }
</style>