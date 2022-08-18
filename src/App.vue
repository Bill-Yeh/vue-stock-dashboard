<template>
  <div id="app">
    <input type="checkbox" id="rwd-switch" />
    <header class="rwd-header">
      <div class="header-wrap">
        <label for="rwd-switch" class="header_hb">
          <span></span>
          <span></span>
          <span></span>
        </label>
        <div class="header-logo">
          <router-link to="/">
            <img src="@/assets/money.png" alt="Investment" />
          </router-link>
        </div>
        <div class="header-bell">
          <i class="bi bi-bell-fill"></i>
        </div>
      </div>
      <nav class="rwd-main-nav">
        <div class="rwd-main-nav-wrap">
          <div class="search-function">
            <input type="text" placeholder="Search for stock or more" />
            <i class="bi bi-search"></i>
          </div>
          <div class="rwd-nav-item">
            <ul class="item-list">
              <li class="rwd-home">
                <i class="bi bi-house-door-fill"></i>
                <span>Home</span>
              </li>
              <li class="rwd-exchange">
                <i class="bi bi-currency-exchange"></i>
                <span>Exchange</span>
                <div class="rwd-item-arrow-down">
                  <i class="bi bi-chevron-down"></i>
                </div>
              </li>
              <li class="rwd-stock">
                <i class="bi bi-graph-up"></i>
                <span>Stock</span>
              </li>
              <li class="rwd-crypto">
                <i class="bi bi-currency-bitcoin"></i>
                <span>Crypto</span>
              </li>
              <li class="rwd-member">
                <i class="bi bi-person-fill"></i>
                <span>Member</span>
                <div class="rwd-item-arrow-down">
                  <i class="bi bi-chevron-down"></i>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
    <!-- <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav> -->
    <router-view />
  </div>
</template>

<style lang="scss">
@import "assets/scss/main.scss";
</style>
