<template>
  <div class="ui secondary menu">
    <div class="ui container">
      <div class="left menu">
        <router-link class="item" to="/">
          <img class="ui large image" src="../assets/nuevoLogo.png" alt="Ecomerce" />          
        </router-link>
        <router-link class="item" to="/">
          INICIO
        </router-link>
        <router-link class="item" to="/service">
          SERVICIOS
        </router-link>
        <router-link class="item" to="/store">
          TIENDA
        </router-link>
        <router-link class="item" to="/contact">
          CONTACTENOS
        </router-link>
      </div>
      <!-- Iniciar sesion -->
      <div class="right menu">
        <router-link class="item btn" to="/login" v-if="!token">
          Iniciar sesión
        </router-link>

        <template v-if="token">
          <router-link class="item" to="/orders">Pedidos</router-link>
          <span class="ui item cart">
            <i class="shopping cart icon"></i>
          </span>
          <span class="ui item logout">
            <i class="sign-out icon"></i>
          </span>
        </template>
      </div>
    </div>
  </div>
</template>

<script>
import { getTokenApi } from '../api/token';
export default {
  name: 'Menu',

  setup() {
    const token = getTokenApi();

    return {
      token,
    };
  },
};
</script>

<style lang="scss" scoped>
.ui.menu.secondary {
  background-color: #e2e2e2;

  .item {
    color: #14679b;
    font-size: 18px;    
    &:hover {
      color: #1fa1f1;
    }
  }

  .item.btn{
    background-color: #1fa1f1;
  }

  .menu.left {
    width: 50%;
    .ui.image {
      width: 180px;
    }
  }

  .menu.right {
    width: 50%;
    justify-content: flex-end;

    .logout,
    .cart {
      &:hover {
        cursor: pointer;
      }
    }
  }
}
</style>
