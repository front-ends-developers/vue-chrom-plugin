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
    <h1 class="m-b-20 common-title"><img src="../../../images/title32.png" alt="" />开发环境</h1>
    <ul class="common-ul dev-ul flex flex-start flex-wrap">
      <li v-for="(item, index) in threeDevWeb" :key="index+'three'">
          <a href="#" id="tapd" @click="toUrl(item)">
              <img :src="item.src" />
              <p class="colour-text">{{ item.webName }}</p>
          </a>
      </li>
    </ul>
    <br />
    <h1 class="m-b-20 common-title "><img src="../../../images/title32.png" alt="" />生产环境</h1>
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
export default {
    data() {
        return {
          baseWeb:[
            {
              src: require('../../../images/tapd.png'),
              webName: 'Tapd',
              url: 'https://www.tapd.cn/my_worktable/#&filter_close=true'
            },
            {
              src: require('../../../images/jenkins.png'),
              webName: 'Jenkins',
              url: 'http://123.207.187.158:8888/jenkins/'
            },
            {
              src: require('../../../images/gitlab.png'),
              webName: 'Gitlab',
              url: 'http://115.159.76.241/dashboard/groups'
            },
            {
              src: require('../../../images/api.png'),
              webName: 'Yapi',
              url: 'http://yapi.gicdev.com'
            },
            {
              src: require('../../../images/yuque.png'),
              webName: '语雀',
              url: 'https://www.yuque.com/kgrc1y'
            },
            {
              src: require('../../../images/lanhu.png'),
              webName: '蓝湖',
              url: 'https://next.lanhuapp.com/web/#/item?fid=9af0d2e6-82bf-44b2-9f01-8c142a3fc99c&commonly=all'
            },
          ],
          threeDevWeb: [],
          threeProWeb: [],
          fourDevWeb: [],
          fourProWeb: [],
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