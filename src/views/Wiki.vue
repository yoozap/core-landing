<template>
  <div class="wiki-container">
      <div class="header" data-aos="fade-up">
        <router-link
          class="logo" to="/">
          <svg width="64" height="88" viewBox="0 0 64 88" fill="none" xmlns="http://www.w3.org/2000/svg">
            <g clip-path="url(#clip0)">
              <path d="M8.99963 88C6.05963 88 3.81963 87.2467 2.27963 85.74C1.48874 84.9059 0.878133 83.9178 0.485866 82.8374C0.0935993 81.7569 -0.0719185 80.6072 -0.000370834 79.46C-0.0708249 78.2872 0.0927039 77.112 0.480698 76.003C0.868692 74.8939 1.4734 73.8731 2.25963 73C3.75963 71.4467 6.0063 70.6667 8.99963 70.66C9.92191 70.6506 10.8429 70.731 11.7496 70.9C12.5441 71.0475 13.3263 71.2548 14.0896 71.52V75.21C12.5748 74.5814 10.9497 74.2618 9.30963 74.27C8.62302 74.2095 7.93128 74.2891 7.27635 74.504C6.62143 74.7189 6.01697 75.0645 5.49963 75.52C4.59538 76.6243 4.15767 78.0379 4.27963 79.46C4.22118 80.1412 4.30476 80.8271 4.52509 81.4743C4.74542 82.1215 5.0977 82.716 5.55963 83.22C6.62907 84.0932 7.99281 84.5227 9.36963 84.42C10.1847 84.4221 10.9982 84.3485 11.7996 84.2C12.598 84.051 13.3788 83.8198 14.1296 83.51V87.22C13.3678 87.4662 12.5891 87.6567 11.7996 87.79C10.8739 87.9393 9.93723 88.0095 8.99963 88V88Z" fill="#00050F"/>
              <path d="M23.8695 88C21.1295 88 19.0495 87.3033 17.6295 85.91C16.2095 84.5167 15.4928 82.35 15.4795 79.41C15.4795 76.29 16.1995 74.06 17.6295 72.7C19.0595 71.34 21.1295 70.7 23.8695 70.7C26.6095 70.7 28.6795 71.38 30.1095 72.7C31.5395 74.02 32.2495 76.29 32.2495 79.41C32.2495 82.35 31.5295 84.52 30.1095 85.91C28.6895 87.3 26.5995 88 23.8695 88ZM23.8695 84.42C24.4495 84.4776 25.035 84.3982 25.5787 84.188C26.1224 83.9778 26.6091 83.6428 26.9995 83.21C27.7499 82.0915 28.1021 80.753 27.9995 79.41C28.1282 78.0019 27.7757 76.5918 26.9995 75.41C26.6048 74.9968 26.122 74.6778 25.587 74.477C25.052 74.2762 24.4786 74.1986 23.9095 74.25C23.3357 74.1969 22.7574 74.2736 22.2173 74.4744C21.6772 74.6752 21.1892 74.995 20.7895 75.41C20.0081 76.5896 19.6551 78.0015 19.7895 79.41C19.6869 80.753 20.0391 82.0915 20.7895 83.21C21.1766 83.6332 21.6554 83.9623 22.1892 84.1721C22.7231 84.3818 23.2978 84.4666 23.8695 84.42V84.42Z" fill="#00050F"/>
              <path d="M34.3896 87.74V70.92H42.7996C43.5995 70.8538 44.4042 70.9596 45.1598 71.2304C45.9153 71.5012 46.604 71.9307 47.1796 72.49C48.1682 73.6589 48.6727 75.1614 48.5896 76.69C48.6208 77.755 48.3203 78.8033 47.7296 79.69C47.1523 80.5449 46.3345 81.2095 45.3797 81.6C45.6117 81.7778 45.8113 81.9943 45.9697 82.24C46.1602 82.5578 46.3209 82.8926 46.4496 83.24L48.4496 87.78H44.0496L42.1696 83.5C42.0478 83.1828 41.84 82.9058 41.5696 82.7C41.2655 82.5266 40.9196 82.4401 40.5696 82.45H38.5896V87.78L34.3896 87.74ZM38.5896 79.17H41.6996C42.3934 79.2139 43.0784 78.9962 43.6196 78.56C43.8636 78.3171 44.0516 78.024 44.1708 77.7011C44.29 77.3781 44.3373 77.0331 44.3097 76.69C44.3097 75.01 43.4997 74.16 41.8797 74.16H38.5896V79.17Z" fill="#00050F"/>
              <path d="M50.7295 87.74V70.92H63.1395V74.16H54.9395V77.69H62.1695V81H54.9395V84.5H63.1395V87.74H50.7295Z" fill="#00050F"/>
              <path fill-rule="evenodd" clip-rule="evenodd" d="M11.74 15.39C14.1961 12.1394 17.4138 9.54246 21.1098 7.82801C24.8057 6.11355 28.8665 5.33413 32.9345 5.55838C37.0026 5.78262 40.9531 7.00366 44.4382 9.11396C47.9233 11.2243 50.836 14.1591 52.92 17.66L54.72 16.66L57.72 14.9C55.0286 10.372 51.2061 6.62165 46.6278 4.01691C42.0494 1.41218 36.8725 0.0426025 31.605 0.0426025C26.3375 0.0426025 21.1606 1.41218 16.5822 4.01691C12.0039 6.62165 8.1814 10.372 5.49 14.9L4 17.24L6.38 18.65L15.59 24.12C14.0836 27.9087 13.9787 32.1106 15.2943 35.9696C16.6098 39.8287 19.2595 43.0916 22.7664 45.1712C26.2734 47.2508 30.4074 48.0105 34.4245 47.3137C38.4417 46.6168 42.0783 44.5092 44.68 41.37L51.39 45.37C48.9333 48.6235 45.7135 51.2223 42.0148 52.9372C38.3162 54.652 34.2523 55.4301 30.1817 55.2028C26.1112 54.9755 22.1592 53.7498 18.6744 51.6339C15.1896 49.5179 12.2792 46.5768 10.2 43.07L5.45 45.88C8.1414 50.408 11.9639 54.1584 16.5422 56.7631C21.1206 59.3678 26.2975 60.7374 31.565 60.7374C36.8325 60.7374 42.0094 59.3678 46.5878 56.7631C51.1661 54.1584 54.9886 50.408 57.68 45.88L59.1 43.5L56.72 42.09L49.16 37.6L42.64 33.84C41.8463 36.3666 40.2119 38.5456 38.0084 40.0148C35.805 41.484 33.1651 42.155 30.5275 41.9163C27.8899 41.6775 25.4134 40.5434 23.5096 38.7025C21.6058 36.8615 20.3892 34.4245 20.062 31.7964C19.7349 29.1683 20.3169 26.5074 21.7113 24.2558C23.1058 22.0043 25.2286 20.2977 27.7272 19.4196C30.2258 18.5416 32.9496 18.5449 35.446 19.4291C37.9424 20.3133 40.0611 22.0251 41.45 24.28L46.24 21.52C44.8328 19.1861 42.8888 17.2219 40.5696 15.7906C38.2503 14.3594 35.6229 13.5025 32.9058 13.2912C30.1887 13.08 27.4605 13.5204 24.9479 14.576C22.4353 15.6315 20.211 17.2717 18.46 19.36L11.74 15.39Z" fill="#FF7152"/>
            </g>
            <defs>
              <clipPath id="clip0">
              <rect width="63.14" height="88" fill="white"/>
              </clipPath>
            </defs>
          </svg>
          <h1>wiki</h1>
        </router-link>
        <div class="header__head">
          <span>Welcome to the CORE Wiki</span>
          <div class="header__social">
            <a href="#" class="header__social-link">
              <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M9.23896 16V8.70218H11.6875L12.0549 5.85725H9.23896V4.04118C9.23896 3.21776 9.46667 2.65661 10.6488 2.65661L12.154 2.65599V0.111384C11.8937 0.0775563 11.0002 0 9.96017 0C7.78849 0 6.30172 1.32557 6.30172 3.75942V5.85725H3.8457V8.70218H6.30172V16H9.23896Z" fill="#00050F"/>
              </svg>
            </a>
            <a href="#" class="header__social-link">
              <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0)">
                <path d="M16 3.039C15.405 3.3 14.771 3.473 14.11 3.557C14.79 3.151 15.309 2.513 15.553 1.744C14.919 2.122 14.219 2.389 13.473 2.538C12.871 1.897 12.013 1.5 11.077 1.5C9.261 1.5 7.799 2.974 7.799 4.781C7.799 5.041 7.821 5.291 7.875 5.529C5.148 5.396 2.735 4.089 1.114 2.098C0.831 2.589 0.665 3.151 0.665 3.756C0.665 4.892 1.25 5.899 2.122 6.482C1.595 6.472 1.078 6.319 0.64 6.078C0.64 6.088 0.64 6.101 0.64 6.114C0.64 7.708 1.777 9.032 3.268 9.337C3.001 9.41 2.71 9.445 2.408 9.445C2.198 9.445 1.986 9.433 1.787 9.389C2.212 10.688 3.418 11.643 4.852 11.674C3.736 12.547 2.319 13.073 0.785 13.073C0.516 13.073 0.258 13.061 0 13.028C1.453 13.965 3.175 14.5 5.032 14.5C11.068 14.5 14.368 9.5 14.368 5.166C14.368 5.021 14.363 4.881 14.356 4.742C15.007 4.28 15.554 3.703 16 3.039Z" fill="#00050F"/>
                </g>
                <defs>
                <clipPath id="clip0">
                <rect width="16" height="16" fill="white"/>
                </clipPath>
                </defs>
              </svg>
            </a>
            <a href="#" class="header__social-link">
              <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0)">
                <path d="M6.27812 10.1207L6.01345 13.8433C6.39212 13.8433 6.55612 13.6807 6.75279 13.4853L8.52812 11.7887L12.2068 14.4827C12.8815 14.8587 13.3568 14.6607 13.5388 13.862L15.9535 2.54732L15.9541 2.54666C16.1681 1.54932 15.5935 1.15932 14.9361 1.40399L0.742785 6.83799C-0.225881 7.21399 -0.211215 7.75399 0.578119 7.99866L4.20679 9.12732L12.6355 3.85332C13.0321 3.59066 13.3928 3.73599 13.0961 3.99866L6.27812 10.1207Z" fill="#00050F"/>
                </g>
                <defs>
                <clipPath id="clip0">
                <rect width="16" height="16" fill="white"/>
                </clipPath>
                </defs>
              </svg>
            </a>
            <a href="#" class="header__social-link">
              <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0)">
                <path d="M7.999 0.000205994C3.582 0.000205994 0 3.67265 0 8.20296C0 11.8264 2.292 14.9004 5.472 15.986C5.872 16.0616 6.018 15.8083 6.018 15.5908C6.018 15.3957 6.011 14.88 6.007 14.1957C3.782 14.691 3.312 13.0958 3.312 13.0958C2.949 12.1481 2.424 11.8958 2.424 11.8958C1.697 11.3872 2.478 11.3975 2.478 11.3975C3.281 11.4557 3.703 12.2431 3.703 12.2431C4.417 13.4961 5.576 13.1346 6.032 12.9242C6.104 12.3942 6.311 12.0327 6.54 11.8274C4.764 11.6201 2.896 10.9164 2.896 7.77403C2.896 6.87839 3.208 6.14614 3.72 5.5722C3.637 5.36488 3.363 4.53051 3.798 3.40202C3.798 3.40202 4.47 3.18143 5.998 4.24252C6.636 4.06073 7.32 3.96984 8.001 3.96678C8.68 3.97086 9.365 4.06073 10.004 4.24354C11.531 3.18245 12.202 3.40304 12.202 3.40304C12.638 4.53255 12.364 5.3659 12.282 5.57322C12.795 6.14717 13.104 6.87941 13.104 7.77505C13.104 10.9256 11.234 11.6191 9.452 11.8223C9.739 12.0756 9.995 12.576 9.995 13.3409C9.995 14.4377 9.985 15.3222 9.985 15.5908C9.985 15.8103 10.129 16.0656 10.535 15.985C13.71 14.8983 16 11.8254 16 8.20296C16 3.67265 12.418 0.000205994 7.999 0.000205994Z" fill="#00050F"/>
                </g>
                <defs>
                <clipPath id="clip0">
                <rect width="16" height="16" fill="white"/>
                </clipPath>
                </defs>
              </svg>
            </a>
          </div>
        </div>
      </div>
      <div class="wiki" data-aos="fade">
        <div class="wiki__menu" v-click-outside="closeMenu">
          <div class="wiki__menu-top">
            <div class="wiki__menu-burger" 
              @click="burgerActive = !burgerActive"
              :class="{active:burgerActive}">
              <span class="line1"></span>
              <span class="line2"></span>
              <span class="line3"></span>
            </div>
            <div class="wiki__menu-title" key="title">{{itemData[chousenCategory].category}}</div>
          </div>
          <slide-up-down :active="burgerActive" :duration="1000">
            <div class="wiki__menu-item-list">
              <div class="wiki__menu-item" v-for="(category, index) in itemData" 
                :class="{active: activeCategory == index}">

                <div class="wiki__menu-head" @click="toggleActive(index)">
                  <h3 :class="{active: chousenCategory == index}">{{category.category}}</h3>
                  <svg :class="{active: chousenCategory == index}" width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M11 3L6 8L1 3" stroke="#00050F" stroke-width="2"/>
                  </svg>

                </div>
                <slide-up-down class="wiki__menu-list" 
                  :active="activeCategory == index" :duration="1000">
                  <div>
                    <template v-for="(tab , tabIndex) in category.tabList">

                      <router-link class="wiki__menu-list-item"
                        v-if="tab.tabGroupTitle == '' "
                        :to="{ name: 'wiki', params: { sectionName:tab.url } }" 
                        :key = "tab.id"
                        @click.native.prevent="
                        text = tab.content; 
                        chousenCategory = index;
                        findTab(); 
                        animate()">
                        {{tab.title}}
                      </router-link>

                      <div v-else class="wiki__menu-list-subItems">
                        <span 
                          v-if="tab.tabGroupTitle != category.tabList[tabIndex - 1].tabGroupTitle">
                          {{tab.tabGroupTitle}}
                        </span>
                        <router-link class="wiki__menu-list-item"
                          :to="{ name: 'wiki', params: { sectionName:tab.url } }" 
                          :key = "tab.id"
                          @click.native.prevent="
                          text = tab.content; 
                          chousenCategory = index; 
                          findTab();
                          animate()">
                          {{tab.title}}
                        </router-link>
                      </div>
                    </template>
                  </div>
                </slide-up-down>
              </div>
            </div>
          </slide-up-down>
        </div>

        <transition name="fade">
          <div class="text" v-if="animateText" ref="text">
            <template v-for="content in text">
              <div class="head" v-if="content.navUrl != '' " :id="content.navUrl"
                @click="copyUrl(content.navUrl)">
                <h3>{{content.title}}</h3>
                <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <g clip-path="url(#clip0)">
                  <path d="M14.6112 5.02658L12.7332 5.02641C12.3603 5.02656 12.0582 5.32867 12.058 5.7016C12.058 6.07469 12.3604 6.37712 12.7334 6.37695L14.6114 6.37712C16.5954 6.37728 18.2203 8.00411 18.2337 9.99943C18.2337 11.983 16.607 13.6081 14.6114 13.6217L12.7333 13.6219C12.3604 13.6218 12.058 13.9242 12.058 14.2973C12.058 14.6704 12.3602 14.9726 12.7332 14.9725L14.6158 14.9725C15.984 14.9632 17.2252 14.402 18.1245 13.5027C19.0256 12.6015 19.5838 11.3605 19.5842 9.99486C19.5656 7.25506 17.335 5.02643 14.6112 5.02658Z" fill="#FF7152"/>
                  <path d="M7.8946 5.02696L6.01183 5.02678C3.27259 5.04524 1.04393 7.2761 1.04362 10.0042C1.0621 12.7438 3.29279 14.9723 6.01645 14.9723L7.89462 14.9723C8.08102 14.9724 8.24988 14.8968 8.37212 14.7746C8.49419 14.6525 8.56981 14.4836 8.56966 14.2969C8.56981 13.924 8.2674 13.6216 7.89447 13.6217L6.01629 13.6217C4.03244 13.6217 2.40751 11.9949 2.39414 9.99958C2.39445 8.01573 4.0213 6.39082 6.01644 6.37728H7.89462C8.26773 6.37728 8.56981 6.07519 8.56981 5.70209C8.56995 5.3292 8.26753 5.02678 7.8946 5.02696Z" fill="#FF7152"/>
                  <path d="M12.7331 9.32476L7.89446 9.32476C7.52153 9.32459 7.21911 9.627 7.21927 9.99996C7.21911 10.3729 7.52153 10.6753 7.89446 10.6751L12.7331 10.6751C12.9196 10.6751 13.0883 10.5997 13.2106 10.4775C13.3328 10.3552 13.4083 10.1865 13.4083 9.99995C13.4084 9.62702 13.106 9.32461 12.7331 9.32476Z" fill="#FF7152"/>
                  </g>
                  <defs>
                  <clipPath id="clip0">
                  <rect width="20" height="20" fill="white"/>
                  </clipPath>
                  </defs>
                </svg>
              </div>
              <div v-html="content.html" v-if="content.html != ''"></div>

            </template>
            <div class="text__bottom">
              <span>Explore next</span>
              <button @click="openNext()">
                <span v-if="nextTab">{{nextTab.title}}</span>
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M13.8706 20.2576L11.8871 18.2534L16.35 13.7905L2.11426 13.7905L2.11426 10.9806L16.35 10.9806L11.8871 6.51771L13.8706 4.51355L21.7426 12.3856L13.8706 20.2576Z" fill="#00050F"/>
                </svg>
              </button>
            </div>
          </div>
        </transition>
        <div class="wiki_nav">
          <transition name="fade">             
            <scrollactive active-class="active"  
              class="wiki_nav-list" v-if="animateText" data-aos="fade-in">
              <template v-for="(nav, index) in text">
                <span class="head" v-if="nav.navGroupTitle != '' 
                  && nav.navGroupTitle != text[index - 1].navGroupTitle">
                    {{nav.navGroupTitle}}
                </span>
                <a class="scrollactive-item wiki_nav-link" 
                  :class="{pLeft: nav.navGroupTitle != ''}"
                  :href="'#' + nav.navUrl">{{nav.title}}</a>
              </template>
            </scrollactive >
          </transition>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Wiki',
  data () {
    return {
      activeCategory:0,
      chousenCategory: 0,
      text: null,
      animateText: true,
      burgerActive: false,
      nextTab: null
    }
  },
  mounted () {
    /*open selected tab content or set default(first)*/
    let sectionName = this.$route.params.sectionName;
    let _this = this;
    if(sectionName === undefined){
      this.text = this.itemData[0].tabList[0].content;
      this.activeCategory = 0;
      this.$router.push({ name: 'wiki', params: { sectionName: this.itemData[0].tabList[0].url } })
    }else{
      this.itemData.forEach(function(item, index){
        item.tabList.find(function(tab){
          if(tab.url == sectionName){
            _this.activeCategory = index;
            _this.text = tab.content;
            return false;
          }
        })
      })
    }
    
    if(this.$mq == "tablet" || this.$mq == "phone"){
      this.burgerActive = false;
    }else{
      this.burgerActive = true;
    }

    /*change page layout*/
    this.$store.commit('setSideMenuState', false)
    document.body.style.backgroundColor= "#F5F5F5";

    this.findTab()
  },
  watch:{
    $mq:function(){
      if(this.$mq == "tablet" || this.$mq == "phone"){
        this.burgerActive = false;
      }else{
        this.burgerActive = true;
      }
    },
    activeTab(){
      this.findTab()
    }
  },
  computed:{
    itemData(){
      return this.$store.state.wiki;
    },
    
  },
  beforeDestroy() {
    /*return page layout*/
    this.$store.commit('setSideMenuState', true)
    document.body.style.backgroundColor= "#00050F";
  },
  methods: {
    toggleActive(index){
      if(this.activeCategory == index){
        this.activeCategory = null;
      }else{
        this.activeCategory = index;
      }
    },
    animate(){
      this.animateText = false;
      setTimeout(()=> this.animateText = true,100)
    },
    copyUrl(path){
      let value =this.$route.fullPath + '#' + path;
      this.$clipboard(value)
    },
    openNext(){
      this.animateText = false;
      setTimeout(()=> this.animateText = true,100)
      this.text = this.nextTab.content;
      this.$router.push({ name: 'wiki', params: { sectionName: this.nextTab.url } })
      this.findTab();
    },
    findTab(){
      let _this = this;
      let result;
      let current = this.$route.params.sectionName;
      let chousenCategory;
      let activeTab;

      this.itemData.forEach(function(item, index){
        item.tabList.find(function(tab, index2){
          if(tab.url == current){
            chousenCategory = index;
            _this.chousenCategory = index;
            activeTab = index2;
            return false;
          }
        })
      })


      result = this.itemData[chousenCategory].tabList.find(function(tab, index){
        if(index == [activeTab + 1]){
          return tab;
        }
      })

      if(result == undefined && this.itemData.length > chousenCategory + 1){
        result = this.itemData[chousenCategory + 1].tabList[0]
      }else if(result === undefined && this.itemData.length <= chousenCategory + 1){
        result = this.itemData[0].tabList[0];
      }

      this.nextTab = result;
    },
    closeMenu(){
      if(this.$mq == "tablet" || this.$mq == "phone"){
        this.burgerActive = false;
      }
      
    }
    
  }
}
</script>
<style scoped>
  .fade-enter-active, .fade-leave-active {
    transition: opacity 1s;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }

  .wiki-container{
    max-width: 1920px;
    margin: 0 auto;
    padding-right: 80px;
  }
  .header{
    display: flex;
    align-items: center;
  }
  .logo{
    width: 230px;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 40px;
  }
  .logo h1{
    color: #000;
    font-size: 16px;
    line-height: 22px;
  }
  .header__head{
    flex: 1;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .header__head span{
    font-size: 15px;
    color: #00050F;
    line-height: 24px;
  }
  .header__social{
    display: flex;
    align-items: center;
  }
  .header__social-link{
    display: flex;
    align-items: center;
    margin-right: 16px;
    cursor: pointer;
  }
  .header__social-link:last-child{
    margin-right: 0;
  }
  .header__social-link path{
    transition: 0.6s;
  }
  @media(min-width: 1024px){
    .header__social-link:hover path{
      fill: #FF7152;
    }
  }


  .wiki{
    display: flex;
    justify-content: space-between;
    width: 100%;
    padding: 56px 100px 100px 0;
  }
  .wiki__menu{
    width: 230px;
    flex: none;
    padding: 20px 20px 0 0;
    max-height: 485px;
    overflow: auto;
  }
  .wiki__menu::-webkit-scrollbar {
    width: 4px;
  }
  .wiki__menu::-webkit-scrollbar-track {
    background: transparent;
  }
  .wiki__menu::-webkit-scrollbar-thumb {
    background: rgba(0,5,15,0.1);
  }
  .wiki__menu-top{
    display: none;
    justify-content: space-between;
    background-color: #010918;
    height: 60px;
    align-items: center;
    padding: 0 34px;
  }
  .wiki__menu-burger{
    position: relative;
    width: 18px;
    height: 16px;
    cursor: pointer;
  }
  .wiki__menu-burger .line1, 
  .wiki__menu-burger .line2, 
  .wiki__menu-burger .line3 {
    display: flex;
    width: 100%;
    height: 3px;
    background-color: #fff;
    margin: 3px 0;
    transition: .4s;
    border-radius: 10px;
  }
  .wiki__menu-burger.active .line1{
    position: absolute;
    top: 50%;
    transform: rotate(-45deg);
    background-color: #FF7152;
  }
  .wiki__menu-burger.active .line2 {
    display: none;
  }
  .wiki__menu-burger.active .line3 {
    position: absolute;
    top: 50%;
    transform: rotate(45deg);
    background-color: #FF7152;
  }

  .wiki__menu-item{
    border-bottom: 1px solid rgba(0,5,15,0.05);
  }
  .wiki__menu-item:last-child{
    border-bottom: none;
  }
  .wiki__menu-head{
    position: relative;
    display: flex;
    align-items: center;
    padding: 16px 0 16px 56px;
    cursor: pointer;
  }
  .wiki__menu-head h3{
    font-size: 13px;
    line-height: 22px;
    text-transform: uppercase;
    margin-right: 30px;
    color: #00050F;
    transition: 0.6s;
  }
  .wiki__menu-item.active h3{
    color: #FF7152;
  }
  .wiki__menu-head svg{
    position: absolute;
    right: 0px;
    top: 20px;
    transition: 0.6s;
  }
  .wiki__menu-head path{
    transition: 0.6s;
  }
  .wiki__menu-item.active svg{
    transform: rotate(180deg);
  }
  .wiki__menu-item.active path{
    stroke: #FF7152;
  }
  .wiki__menu-list > div{
    padding: 0 0 16px 56px;
  }
  .wiki__menu-list-item{
    display: flex;
    font-size: 13px;
    color: #00050F;
    margin-bottom: 8px;
    transition: 0.6s;
    cursor: pointer;
  }
  .wiki__menu-list-subItems > span{
    display: flex;
    font-size: 13px;
    color: #00050F;
    margin-bottom: 8px;
  }
  .wiki__menu-list-subItems > .wiki__menu-list-item{
    padding-left: 10px;
  }
  .wiki__menu-list-item.router-link-active{
    color: rgba(0,5,15,0.3);
  }


  @media(min-width: 1024px){
    .wiki__menu-head:hover h3{
      color: #FF7152;
    }
    .wiki__menu-head:hover path{
      stroke: #FF7152;
    }
    .wiki__menu-list-item:hover{
      color: rgba(0,5,15,0.3);
    }
  }


  .wiki_nav{
    align-self: flex-start;
    width: 195px;
    position: -webkit-sticky;
    position: sticky;
    top: 0;
    padding-left: 24px;
    height: 210px;
    overflow: auto;
  }
  .wiki_nav::-webkit-scrollbar {
    width: 4px;
  }
  .wiki_nav::-webkit-scrollbar-track {
    background: transparent;
  }
  .wiki_nav::-webkit-scrollbar-thumb {
    background: rgba(0,5,15,0.1);
  }
  .wiki_nav:before{
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 1px;
    height: 100%;
    min-height: 210px;
    background-color: rgba(0,5,15,0.05);
  }
  .wiki_nav .head{
    display: flex;
    font-size: 15px;
    color: #00050F;
    line-height: 24px;
    margin-bottom: 6px;
  }
  .wiki_nav-link{
    font-size: 12px;
    color: #00050F;
    line-height: 20px;
    display: flex;
    margin-bottom: 6px;
    cursor: pointer;
    transition: 0.6s;
  }
  .wiki_nav-link.pLeft{
    padding-left: 10px;
  }
  .wiki_nav-link:last-child{
    margin-bottom: 0;
  }
  .scrollactive-item{
    transition: 0.6s;
  }
  .scrollactive-item.active{
    color: rgba(0,5,15,0.3);
  }
  @media(min-width: 1024px){
    .scrollactive-item:hover{
      color: rgba(0,5,15,0.3);
    }
  }



  .wiki .text{
    flex: 1;
    padding: 0 56px;
  }
  .text > div{
    margin-bottom: 56px;
  }
  .text > div.head{
    margin-bottom: 16px;
  }
  .text .head{
    position: relative;
  }
  .text .head svg{
    position: absolute;
    top: 5px;
    left: -12px;
    transform: translateX(-100%);
    transition: 0.6s;
    opacity: 0;
  }
  .text .head:hover svg{
    opacity: 1;
  }
  .text > div:last-child{
    margin-bottom: 0;
  }
  .text ::v-deep mark{
    display: block;
    width: 100%;
    padding: 26px 32px;
    background-color: #fff;
    color: #00050F;
    font-size: 15px;
    line-height: 24px;
    border-left: 5px solid #FF7152;
    margin: 32px 0;
  }
  .text ::v-deep img{
    display: block;
    width: 100%;
    height: auto;
    margin: 0 32px;
  }
  .text ::v-deep a{
    display: inline-flex;
    font-size: inherit;
    line-height: inherit;
    color: #FF7152;
    transition: .6s cubic-bezier(0.79, 0.01, 0.15, 0.99);
    cursor: pointer;
    margin-bottom: 15px;
  }
  .text ::v-deep a:hover{
    color: #0500FF;
  }
  .text ::v-deep li:after{
    content: '';
    background: #0500FF;
    height: 6px;
    width: 6px;
    border-radius: 50%;
    display: flex;
    position: absolute;
    left: 0px;
    top: 10px;
  }
  .text ::v-deep li{
    position: relative;
    padding-left: 20px;
    margin-bottom: 5px;
    font-size: 15px;
    line-height: 24px;
    color: rgba(0,5,15,0.5);
  }
  .text ::v-deep ul{
    margin-bottom: 30px;
  }
  .text ::v-deep h3{
    font-size: 20px;
    line-height: 30px;
    margin-bottom: 16px;
    color: #00050F;
  }
  .text ::v-deep h2{
    font-size: 51px;
    line-height: 66px;
    margin-bottom: 16px;
    color: #00050F;
  }
  .text ::v-deep h2 span, .text ::v-deep h3 span{
    line-height: inherit;
    font-size: inherit;
    color: #FF7152;
    margin-right: 10px;
  }
  .text ::v-deep h1{
    font-size: 100px;
    line-height: 110px;
    margin-top: 210px;
    display: flex;
    flex-direction: column;
    margin-bottom: 100px;
  }
  .text ::v-deep h1 span{
    font-size: inherit;
    line-height: inherit;
  }
  .text ::v-deep h1 span:last-child{
    padding-left: 100px;
  }
  .text ::v-deep p{
    font-size: 15px;
    line-height: 24px;
    color: rgba(0,5,15,0.5);
    margin-bottom: 30px;
  }


  .text__bottom{
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
  }
  .text__bottom > span{
    flex: none;
    font-size: 20px;
    line-height: 30px;
    padding-right: 34px;
    color: rgba(0,5,15,0.2)
  }
  .text__bottom button{
    display: flex;
    align-items: flex-start;
  }
  .text__bottom button span{
    text-align: left;
    font-size: 20px;
    line-height: 30px;
    color: rgba(0,5,15,1);
    transition:0.6s;
  }
  .text__bottom button svg{
    flex: none;
    display: flex;
    margin-left: 25px;
    margin-top: 6px;
    transition: 0.6s;
  }
  @media(min-width: 1024px){
    .text__bottom button:hover svg{
      transform: translateX(10px);
    }
  }

  /*responsive*/


  @media (max-width: 1365px){
    .wiki-container{
      padding-right: 40px;
    }
    .wiki{
      padding: 56px 0 100px 0;
    }
    .wiki .text{
      padding: 0 34px;
    }
    .text__bottom button span,
    .text__bottom > span{
      font-size: 15px;
    }
  }

  @media (max-width: 1023px){
    .logo{
      width: unset;
      margin-right: 34px;
    }
    .header{
      padding-left: 34px;
    }
    .wiki{
      position: relative;
      padding: 200px 0 100px 0;
    }
    .wiki_nav{
      display: none;
    }
    .wiki__menu{
      position: absolute;
      top: 54px;
      left: 0;
      padding-right: 0;
      width: 100%;
      z-index: 10;
      padding: 0;
      overflow: unset;
    }
    .wiki__menu-top{
      display: flex;
    }
    .wiki__menu-item-list{
      background-color: #fff;
      max-height: 350px;
      padding: 0 40px 40px 0;
      overflow: auto;
    }
    .wiki__menu > div:nth-child(2){
      -webkit-box-shadow: 0px 10px 15px 1px rgba(1,9,24,0.2);
      -moz-box-shadow: 0px 10px 15px 1px rgba(1,9,24,0.2);
      box-shadow: 0px 10px 15px 1px rgba(1,9,24,0.2);
    }
    .wiki__menu-item:first-child{
      padding-top: 40px;
    }
    .wiki__menu-item{
      border-bottom: 1px solid rgba(0,5,15,0.2);
    }
    .text__bottom{
      margin-top: 2px;
    }
    .text ::v-deep h1{
      font-size: 60px;
      line-height: 70px;
      margin-bottom: 50px;
    }
    .text ::v-deep h2{
      font-size: 28px;
      line-height: 40px;
    }
    .text ::v-deep p{
      width: 100%;
      padding-left: 0px;
    }
    .text ::v-deep ul{
      margin-left: 20px;
    }
  }
  /*Mobile 320*/
  @media (max-width: 767px){
    .wiki-container{
      padding-right: 16px;
    }
    .header{
      padding-left: 16px;
    }
    .logo{
      padding-top: 21px;
    }
    .header__head{
      flex-direction: column;
      align-items: flex-end;
    }
    .header__social{
      margin-top: 21px;
    }
    .wiki{
      padding: 156px 0 80px 0;
    }
    .wiki__menu-head{
      padding: 16px 0 16px 16px;
    }
    .wiki__menu-list > div {
      padding: 0 0 16px 21px;
    }
    .wiki__menu-top{
      padding: 0 16px;
    }
    .wiki__menu-item-list{
      padding: 0 20px 20px 0;
    }
    .wiki .text{
      padding: 0 0 0 16px;
    }
    .text ::v-deep ul{
      margin-left: 10px;
    }
    .text ::v-deep h1 {
      font-size: 50px;
      line-height: 60px;
      margin-bottom: 30px;
      margin-top: 100px;
    }
    .text ::v-deep mark {
      padding: 16px 21px;
    }
    .text__bottom > span{
      padding-right: 21px;
    }
    .text__bottom button svg{
      margin-left: 10px;
    }
   
  }
</style>
