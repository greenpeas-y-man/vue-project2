<template>
    <header class="p-Header--common">
      <h1 class="logo"><img src="./assets/logo.png"></h1>
        <nav id="wrap_gNav">
          <ul id="gNav" class="menu">
            <li class="menu-item-247"><router-link to="/">トップ</router-link></li>
            <li class="menu-item-248"><router-link to="page2">ページ２</router-link></li>
          </ul>
      </nav>
    </header>
</template>

<script>
export default {
  name: 'HeaderCommon'
}
</script>

<style>

</style>
