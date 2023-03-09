<template>
    <div class="navbar">
      <div class="navbar__brand" @click="$router.push('/')">{{ getTitle() }}</div>

      <dropdown ref="dropdown">
        <btn type="primary" class="dropdown-toggle"
          >Dropdown <span class="caret"></span
        ></btn>
        <template slot="dropdown">
          <li><a role="button">Action</a></li>
          <li><a role="button">Another action</a></li>
          <li><a role="button">Something else here</a></li>
          <li role="separator" class="divider"></li>
          <li><a role="button">Separated link</a></li>
        </template>
      </dropdown>

      <!-- <div  class="navbar__user-settings">
        <a class="dropdown-toggle" @click="openUserSettingsDrop">
          Тестовый Администратор , Ленинградская область
          <span class="caret hidden-xs"></span>
        </a>
        <div class="navbar-dropdown__menu" v-if="onOpen">
          <li class="menu-list-item">Тестовый Администратор , Ленинградская область</li>
          <li class="menu-list-item">Справка</li>
          <li class="menu-list-item">Версия 1.503.2</li>
          <li class="menu-list-item">Написать администратору</li>
          <li class="menu-list-item">Выйти</li>
        </div>
      </div> -->
    </div>
  </template>
  
  <script>
  
  
  export default {
    data() {
      return {
        title: 'Фонд пространственных данных ЛО',
        onOpen: false,
      }
    },
    methods: {
      getTitle() {
        return this.title
      },
      openUserSettingsDrop() {
        if (this.onOpen === false) {
          this.onOpen = true
        } else {
          this.onOpen = false
        }
      }
    }
  }
  
  
  
  </script>
  
  
<style>

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #0766A6;
  padding-left: 10px;
  padding-right: 10px;
  overflow: visible;
}

.navbar__brand {
  padding: 10px 10px;
  font-size: 14px;
  line-height: 20px;
  height: 40px;
  color: #fff;
  cursor: pointer;
}

.navbar__user-settings {
  color: #fff;
  font-size: 14px;
  line-height: 20px;
  cursor: pointer;
  position: relative;
}

.navbar-dropdown__menu {
  position: absolute;
  min-width: 180px;
  padding: 5px 0;
  color: #333333;
  box-shadow: 0 1px 3px rgb(0 0 0 / 10%);
}

.menu-list-item {
  list-style: none;
}

</style>
  