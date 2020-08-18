<template>
  <div class="pop-content">
    <h1 class="m-b-20 common-title"><img src="../../../images/title32.png" alt="" />综合网址</h1>
    <ul class="common-ul dev-ul flex flex-start flex-wrap">
        <li v-for="(item, index) in baseWeb" :key="index+'base'">
            <a href="#" id="tapd" @click="toUrl(item)">
                <img :src="item.src" />
                <p class="colour-text">{{ item.webName }}</p>
            </a>
        </li>
    </ul>
    <br />
    <h1 class="m-b-20 common-title"><img src="../../../images/title32.png" alt="" />3.0开发环境</h1>
    <ul class="common-ul dev-ul flex flex-start flex-wrap">
      <li v-for="(item, index) in threeDevWeb" :key="index+'three'">
          <a href="#" id="tapd" @click="toUrl(item)">
              <img :src="item.src" />
              <p class="colour-text">{{ item.webName }}</p>
          </a>
      </li>
    </ul>
    <br />
    <h1 class="m-b-20 common-title "><img src="../../../images/title32.png" alt="" />3.0生产环境</h1>
    <ul class="common-ul pro-ul flex flex-start flex-wrap">
      <li v-for="(item, index) in threeProWeb" :key="index+'threep'">
          <a href="#" id="tapd" @click="toUrl(item)">
              <img :src="item.src" />
              <p class="colour-text">{{ item.webName }}</p>
          </a>
      </li>
    </ul>
    <h1 class="m-b-20 common-title "><img src="../../../images/title32.png" alt="" />4.0开发环境</h1>
    <ul class="common-ul pro-ul flex flex-start flex-wrap">
      <li v-for="(item, index) in fourDevWeb" :key="index+'four'">
          <a href="#" id="tapd" @click="toUrl(item)">
              <img :src="item.src" />
              <p class="colour-text">{{ item.webName }}</p>
          </a>
      </li>
    </ul>
    <h1 class="m-b-20 common-title "><img src="../../../images/title32.png" alt="" />4.0生产环境</h1>
    <ul class="common-ul pro-ul flex flex-start flex-wrap">
      <li v-for="(item, index) in fourProWeb" :key="index+'fourp'">
          <a href="#" id="tapd" @click="toUrl(item)">
              <img :src="item.src" />
              <p class="colour-text">{{ item.webName }}</p>
          </a>
      </li>
    </ul>
  </div>
</template>
<script>
import { baseWeb } from './base-web.js';
import { threeDevWeb } from './three-dev-web.js';
import { threeProWeb } from './three-pro-web.js';
import { fourDevWeb } from './four-dev-web.js';
import { fourProWeb } from './four-pro-web.js';
export default {
    data() {
        return {
          baseWeb: baseWeb,
          threeDevWeb: threeDevWeb,
          threeProWeb: threeProWeb,
          fourDevWeb: fourDevWeb,
          fourProWeb: fourProWeb,
        };
    },
    methods: {
      /**
       * 跳转网址
       * @param {Object} item
       */
      toUrl(item) {
        window.open(item.url)
      }
    }
};
</script>
<style lang="scss" scoped>
p {
    font-size: 20px;
}
</style>