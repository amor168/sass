<template>
  <div id="main-background">
    <BackPicture id="lt" class="rotating_around"  :items="lt"></BackPicture>
    <BackPicture id="rt"  :items="rt"></BackPicture>
    <BackPicture id="rb" :items="rb"></BackPicture>
    <BackPicture id="lb" :items="lb"></BackPicture>
  </div>
</template>
<script>
  import Vue from 'vue'
  Vue.component("BackPicture",{
    render: function(createElement){
      return createElement("div", this.items.map(function(item){
        return createElement("div",{
          "class": item.class,
           attrs: {id: item.id}
        })
      }))
    },
    props:{
      items:{}
    }
  });
export default {
  name: "background",
  data(){
    return{
      lt:[
        {id: 'lt__element_left'},
        {id: 'lt__bond_left-right'},
        {id: 'lt__element_right'},
        {id: 'lt__element_right__point-1', class: 'dot tiny'},
        {id: 'lt__element_right__point-2', class: 'dot tiny'},
        {id: 'lt__element_right__point-3', class: 'dot tiny'}
      ],
      rt: [
        {id: 'rt__point-center', class: 'rotating_around'},
        {id: 'rt__point-outer-1', class: 'dot tiny'},
        {id: 'rt__point-outer-2', class: 'dot tiny'},
        {id: 'rt__bond_center-outer-1'},
        {id: 'rt__bond_center-outer-2'}
      ],
      rb: [
        {id: "rb__point-center", class: "rotating_around"},
        {id: "rb__point-outer-1"},
        {id: "rb__point-outer-2"},
        {id: "rb__point-outer-3"},
        {id: "rb__point-outer-4"},
        {id: "rb__point-outer-5"},
        {id: "rb__bond_center-outer-1"},
        {id: "rb__bond_center-outer-2"},
        {id: "rb__bond_center-outer-3"},
        {id: "rb__bond_center-outer-4"},
        {id: "rb__bond_center-outer-5"},
        {id: "rb__bond_outer-3-4"},
        {id: "rb__bond_outer-2-A"},
        {id: "rb__bond_outer-2-B"}
      ],
      lb: [
        {id: 'lb__point-center', 'class': 'dot'},
        {id: 'lb__point-outer-1'},
        {id: 'lb__point-outer-2', 'class': 'dot'},
        {id: 'lb__point-outer-3', 'class': 'dot'},
        {id: 'lb__bond_center-outer-1'},
        {id: 'lb__bond_center-outer-2'},
        {id: 'lb__bond_center-outer-3'}
      ]
    }
  }
}
</script>
 <style src="./BackgroundReview.scss" lang="scss"></style>




