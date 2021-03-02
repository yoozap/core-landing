<template>
  	<div class="body-container">
	    <div class="container" :class="firstAnimation ? 'animHead' : ''" v-view="visibilityChanged">
	      	<TopHead/>
	      	<div class="wiki">
	      		<div class="wiki__menu">
              <div class="wiki__menu-top">
                <div class="wiki__menu-burger"
                  @click="burgerActive = !burgerActive"
                  :class="{active:burgerActive}">
                  <span class="line1"></span>
                  <span class="line2"></span>
                  <span class="line3"></span>
                </div>
                <div class="wiki__menu-title">{{itemData[chousenCategory].category}}</div>
              </div>
              <slide-up-down :active="burgerActive" :duration="1000">
                <div class="wiki__menu-item-list">
    	      			<div class="wiki__menu-item" v-for="(tab, index) in itemData"
                    :class="{active: active == index}">
    	      				<div class="wiki__menu-head" @click="toggleActive(index)">
    	      					<h3 :class="{active: chousenCategory == index}">{{tab.category}}</h3>
                      <svg :class="{active: chousenCategory == index}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <line x1="12" y1="4.37115e-08" x2="12" y2="24" stroke="white" stroke-width="2"/>
                        <line x1="24" y1="12" x2="-8.74228e-08" y2="12" stroke="white" stroke-width="2"/>
                      </svg>
    	      				</div>
    	      				<slide-up-down class="wiki__menu-list"
                      :active="active == index" :duration="1000">
                      <div>

      	      					<router-link v-for="(link , linkIndex) in tab.list" :key="linkIndex"
                           :to="{ name: 'wiki', params: { sectionName:link.url } }"
                           class="wiki__menu-list-item"
                          @click.native.prevent="text = link.list; chousenCategory = index; animate()">{{link.navItem}}
                        </router-link>
                      </div>
    	      				</slide-up-down>
    	      			</div>
                </div>
              </slide-up-down>
	      		</div>
            <transition name="fade">
              <div class="text" v-if="animateText" ref="text" data-aos="fade-up">
                <template v-for="item in text">
                  <div  v-html="item.html" :id="item.url"></div>
                  <div  v-for="secondaryItems in item.list"
                        v-html="secondaryItems.html" :id="secondaryItems.url">
                  </div>
                </template>
              </div>
            </transition>
            <div class="wiki_nav">
              <transition name="fade">
                <scrollactive active-class="active"
                  class="wiki_nav-list" v-if="animateText" data-aos="fade-in">
                  <template v-for="item in text">
                    <a class="scrollactive-item wiki_nav-link-main"
                      :href="'#' + item.url" >{{item.title}}</a>
                    <a class="scrollactive-item wiki_nav-link-secondary"
                      v-for="secondaryItems in item.list"
                        :href="'#' + secondaryItems.url" >
                      {{secondaryItems.title}}
                    </a>
                  </template>
                </scrollactive >
              </transition>
            </div>
	  		  </div>
	    </div>
  	</div>
</template>

<script>
import TopHead from '../components/TopHead'
export default {
  name: 'Wiki',
  components: {
    TopHead
  },
  data () {
    return {
      firstAnimation: false,
      active:0,
      activeCategory: 0,
      chousenCategory: 0,
      linkActive: '0_0',
      text: null,
      animateText: true,
      burgerActive: false,
    }
  },
  mounted () {
    setTimeout(() => {
      this.firstAnimation = true
    }, 100)
    let sectionName = this.$route.params.sectionName;
    let _this = this;

    if(sectionName != undefined){
      this.itemData.forEach(function(item, index){
        for(let i = 0; i < item.list.length; i++){
          if(item.list[i].url === sectionName){
            _this.text = item.list[i].list;
            _this.active = index;
            return false;
          }
        }
      })
    }else{
      this.text = this.itemData[0].list[0].list;
      this.active = 0;
      this.$router.push({ name: 'wiki', params: { sectionName: this.itemData[0].list[0].url } })
    }

    if(this.$mq == "tablet" || this.$mq == "phone"){
      this.burgerActive = false;
    }else{
      this.burgerActive = true;
    }
  },
  watch:{
    $mq:function(){
      if(this.$mq == "tablet" || this.$mq == "phone"){
        this.burgerActive = false;
      }else{
        this.burgerActive = true;
      }
    }
  },
  computed:{
    itemData(){
      return this.$store.state.wiki;
    }
  },
  methods: {
    visibilityChanged () {
      this.$store.commit('setMenuStatus', 0)
    },
    toggleActive(index){
      if(this.active == index){
        this.active = null;
      }else{
        this.active = index;
        this.activeCategory = index;
      }
    },
    animate(){
      this.animateText = false;
      setTimeout(()=> this.animateText = true,100)
    }

  }
}
</script>
<style scoped>
  .fade-enter-active, .fade-leave-active {
    transition: opacity 1s;
  }
  .fade-enter, .fade-leave-to /* .fade-leave-active до версии 2.1.8 */ {
    opacity: 0;
  }

	.wiki{
		display: flex;
    justify-content: space-between;
    width: 100%;
		padding: 210px 0px 100px;
	}
	.wiki__menu{
		width: 260px;
		flex: none;
    padding-right: 80px;
	}
  .wiki__menu-top{
    display: none;
    justify-content: space-between;
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
    margin-bottom: 15px;
  }
  .wiki__menu-item:last-child{
    margin-bottom: 0;
  }
  .wiki__menu-head{
    position: relative;
    display: flex;
    align-items: center;
    padding-right: 50px;
    cursor: pointer;
  }
  .wiki__menu-head h3{
    font-size: 20px;
    margin-right: 30px;
    transition: 0.6s;
  }
  .wiki__menu-head h3.active{
    color: #FF7152;
  }
  .wiki__menu-head svg{
    position: absolute;
    right: 0px;
    top: 0px;
  }
  .wiki__menu-head line{
    transition: 0.6s;
  }
  .wiki__menu-head svg.active line{
    stroke: #FF7152;
  }
  .wiki__menu-item.active .wiki__menu-head line:first-child{
    opacity: 0;
  }
  .wiki__menu-list > div{
    padding: 10px 0 20px;
  }
	.wiki__menu-list-item{
    display: flex;
		font-size: 15px;
    margin-bottom: 5px;
    transition: 0.6s;
    cursor: pointer;
	}
  .wiki__menu-list-item.router-link-active{
    color: #FF7152;
  }
  .wiki__menu-list-item:last-child{
    margin-bottom: 0;
  }

  @media(min-width: 1024px){
    .wiki__menu-item:hover .wiki__menu-head h3{
      color: #FF7152;
    }
    .wiki__menu-item:hover .wiki__menu-head line{
      stroke: #FF7152;
    }
    .wiki__menu-list-item:hover{
      color:  #FF7152;
    }
  }

  .wiki .text{
    flex: 1;
    padding-right: 20px;
  }

  .wiki_nav{
    align-self: flex-start;
    width: 240px;
    position: -webkit-sticky;
    position: sticky;
    top: 0;
    padding: 40px 0 40px 20px;
    margin-right: 20px;
    border-left: 1px solid #FF7152;
  }
  .wiki_nav-list > div{
    margin-bottom: 20px;
  }
  .wiki_nav-list > div:last-child{
    margin-bottom: 0;
  }
  .wiki_nav-link-main{
    font-size: 18px;
    display: flex;
    margin-top: 20px;
  }
  .wiki_nav-link-main:first-child{
    margin-top: 0;
  }
  .wiki_nav-link-secondary{
    display: flex;
    padding-left: 20px;
    margin-top: 10px;
    cursor: pointer;
  }
  .scrollactive-item{
    transition: 0.6s;
  }
  .scrollactive-item.active{
    color: #FF7152;
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
  }
  .text ::v-deep ul{
    margin-bottom: 30px;
  }
  .text ::v-deep h3{
    font-size: 20px;
    line-height: 30px;
    margin-bottom: 30px;
  }
  .text ::v-deep h2{
    font-size: 51px;
    line-height: 66px;
    margin-bottom: 30px;
  }
  .text ::v-deep h2 span, .text ::v-deep h3 span{
    line-height: inherit;
    font-size: inherit;
    color: #FF7152;
    margin-right: 10px;
  }
  .terms{
    flex-direction: column;
    position: relative;
  }
  .body-container{
    padding-left: 210px;
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
    color: rgba(255,255,255,.5);
    margin-bottom: 30px;
    width: 70%;
  }

  /*responsive*/

  @media (max-width: 1439px){
    .text ::v-deep p{
      width: 100%;
    }
  }

  @media (max-width: 1365px){
    .wiki__menu{
      width: 240px;
      padding-right: 60px;
    }
    .wiki_nav{
      display: none;
    }
  }

  @media (max-width: 1023px){
    .body-container{
      padding-left: 180px;
    }
    .wiki{
      position: relative;
    }
    .wiki__menu{
      position: absolute;
      top: 150px;
      left: 0;
      padding-right: 0;
      height: 60px;
      width: 100%;
      z-index: 10;
    }
    .wiki__menu-top{
      display: flex;
    }
    .wiki__menu-item-list{
      background-color: #00050F;
      height: 350px;
      padding: 0 40px 40px 0;
      overflow: auto;
      -webkit-box-shadow: 0px 10px 45px 16px rgba(0,5,15,1);
      -moz-box-shadow: 0px 10px 45px 16px rgba(0,5,15,1);
      box-shadow: 0px 10px 45px 16px rgba(0,5,15,1);
    }
    .wiki__menu-item:first-child{
      padding-top: 60px;
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
    .wiki__menu-item-list{
      padding: 0 20px 20px 0;
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
    .body-container{
      padding-left: 0px;
    }
  }
</style>
