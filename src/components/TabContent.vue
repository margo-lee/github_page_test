<script>
import { reactive } from '@vue/reactivity'
import { computed, onMounted,ref } from '@vue/runtime-core';
import $ from 'jquery';
export default {
    setup(){
    const PostArr=reactive([
        {name:'1. 本申請只適用於進出入烏來鄉桶后林道，進入山地特定管制區請另外向烏玉入山檢查所現場辦理入山手續。',
        time:'(2021/4/27 3:07:38 AM)'},
        {name:'2.[緊急封閉]2010/02/19 ~ 2010/02/26 豪大雨道路中斷',
        time:'(2021/4/27 3:07:38 AM)'},
        {name:'3. 本申請只適用於進出入烏來鄉桶后林道，進入山地特定管制區請另外向烏玉入山檢查所現場辦理入山手續。',
        time:'(2021/4/27 3:07:38 AM)'}
    ]);
    const NewsArr=reactive([
        {name:'2-1. 本申請只適用於進出入烏來鄉桶后林道，進入山地特定管制區請另外向烏玉入山檢查所現場辦理入山手續。',
        time:'(2021/4/27 3:07:38 AM)'},
        {name:'2-2.[緊急封閉]2010/02/19 ~ 2010/02/26 豪大雨道路中斷',
        time:'(2021/4/27 3:07:38 AM)'},
        {name:'2-3. 本申請只適用於進出入烏來鄉桶后林道，進入山地特定管制區請另外向烏玉入山檢查所現場辦理入山手續。',
        time:'(2021/4/27 3:07:38 AM)'}
    ])
    const tagStatus=ref('post')
    
    const filterArr =computed(()=>{
    if(tagStatus.value == "post"){
        listH(PostArr)
        tabContentH(PostArr)
        return PostArr
    
    }
    if(tagStatus.value == "news"){
        listH(NewsArr)
        tabContentH(NewsArr)
        return NewsArr
    }
    })

    const listH = (filterArr)=>{
        return `${filterArr.length * 48 }px`
    }
    const tabContent=ref('0px')
    const tabContentH = (filterArr)=>{
        let arrH = filterArr.length * 48
        let tabItemH = 60
        let all=arrH + tabItemH +150
        tabContent.value=`${all}px`
    }
    
    
    onMounted(()=>{     
    /*-----------------------------------*/
    ///////////////// 變數 ////////////////
    /*-----------------------------------*/
    
    var _window = $(window),
    ww = _window.outerWidth(),
    wh = _window.height(),
    wwNormal = 1400,
    wwMedium = 992,
    wwSmall = 768,
    wwxs = 576;

    /*-----------------------------------*/
    ////////////////多組Tab////////////////
    /*-----------------------------------*/
    var tab_headerHeight = Math.floor($(".header").outerHeight(true));
    var resizeTimer1;

    const resizeFn = ()=>{
        _window.resize(function () {
            clearTimeout(resizeTimer1);
            resizeTimer1 = setTimeout(function () {
                ww = _window.outerWidth();
                tabSet();
            }, 50);
        });
    }

    function tabSet() {
    $(".tabs").each(function () {
        var _tab = $(this),
        _tabItem = _tab.find(".tabItem"),
        _tabContent = _tab.find(".tabContent"),
        tabwidth = _tab.width(),
        tabItemHeight = _tabItem.outerHeight(),
        tabContentHeight = _tab.find(".active").next().innerHeight(),
        tiGap = 0,
        tabItemLength = _tabItem.length,
        tabItemWidth;
        _tab.find(".active").next(".tabContent").show();
        if (ww >= wwSmall) {
            _tabContent.css("top", tabItemHeight);
            _tab.height(tabContentHeight + tabItemHeight);
            tabItemWidth = (tabwidth - (tabItemLength - 1) * tiGap) / tabItemLength;
        } else {
            _tab.css("height", "auto");
            _tabItem.css("margin-left", 0).last().css("position", "relative");
        }
        _tabItem.focus(tabs); //改button後，前面改_tabItem
        _tabItem.click(tabs); //改button後，前面改_tabItem
        function tabs(e) {
            var _tabItemNow = $(this), //改button後，原來$(this).parent(),改$(this)
            tvp = _tab.offset().top,
            tabIndex = _tabItemNow.index() / 2,
            scollDistance = tvp + tabItemHeight * tabIndex - tab_headerHeight;
            _tabItem.removeClass("active");
            _tabItemNow.addClass("active");
            if (ww <= wwSmall) {
                _tabItem.not(".active").next().slideUp();
                _tabItemNow.next().slideDown();
            $("html,body")
                .stop(true, false)
                .animate({ scrollTop: scollDistance });
                } else {
                _tabItem.not(".active").next().hide();
                _tabItemNow.next().show();
                tabContentHeight = _tabItemNow.next().innerHeight();
                _tab.height(tabContentHeight + tabItemHeight);
            }
        e.preventDefault();
      }
    });
   
    }
    $(".tabs>.tabItem:first-child>a").trigger("click");
     tabSet();  
})
    
        return{
            NewsArr,PostArr,tagStatus,filterArr,listH,tabContentH,tabContent
        }
    }

}
</script>
<template>
    <div class="tabSet">
        <section class="tabs" :style="{height:tabContent}" >
            <h2 :class="['tabItem',{'active': tagStatus=='post'} ]" @click.prevent="tagStatus='post'"><a href="#">緊急公告</a></h2>
                <!--選到的頁籤項目-->
                <div class="tabContent" :style="{height:listH}">
                <ul>
                     <li v-for="item in filterArr" :key="item.name" ><a href="#">{{item.name}}</a><time>(2021/4/27 3:07:38 AM)</time></li>
                </ul>    
                </div>    
            <h2 :class="['tabItem',{'active': tagStatus=='news'}]" @click.prevent="tagStatus='news'"><a href="#">最新消息</a></h2>
                <div class="tabContent" :style="{height:listH}">
                    <ul>
                        <li v-for="item in filterArr" :key="item.name" ><a href="#">{{item.name}}</a><time>(2021/4/27 3:07:38 AM)</time></li>
                    </ul>
                </div>        
        </section>
    </div>
</template>
<style ></style>