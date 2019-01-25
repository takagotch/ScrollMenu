### ScrollMenu
---
https://github.com/s-yadav/ScrollMenu

```js
var myScrollMenu = ScrollMenu([wrapper] [,options]);

var setupOption = {
  template: ''
  anchorSetup: [
    {
      backgroundColor: "#dc767d",
      label: "ScrollMenu",
      className: "test"
      },
    {
      backgroundColor: "",
      label: ""
    },
    {
      backgroundColor: "",
      label: "",
      template : '<%= label %>'
    }]
};
var scrollMenu = ScrollMenu(setupOption);

var myScrollMenu = ScrollMenu({
  menuType : 'horizontal',
  anchorSetup : [\*setup object*/]
});

var myScrollMenu = ScrollMenu({
  onhover : function(e,data){
    //
  }
});
var myScrollMenu = ScrollMenu({
  anchorSetup : [{
    onhover : function(e,data){
    }
  },
  ]
});

var currentTop = myScrollMenu.scrollTop();

myScrollMenu.scrollTop(300,true, function(){
  console.log('Scroll is done');
});

myScrollMenu.scrollToSection(3,true,function(){
  console.log('Scroll is done');
});

var data = myScrollMenu.getIndexData(2);

myScrollMenu.destroy();
myScrollMenu = null;

setTimeout(funciton(){
  myScrollMenu.refresh();
}, 0);

var scrollElm = myScrollMenu.scrollElm;
scrollElm.on('scroll',function(){
});
var scrollTop = scrollElm.scrollTop();

function IScrollMenu(container, scrollMenuOptions, iScrollOption){
  scrollMenuOptions = scrollMenuOptions || {}; oScrollOptions || {}; scrollMenuOptions.nativeScroll = false; iScrollOptions.probeType = 3;
  var iScrollInst = new IScroll(container, iScrollOptions),
    scrollMenuInst = ScrollMenu(container, scrollMenuOptions);
  scrollMenuInst._scrollTo = function(top, duration,callback){
    iScrollInst.scrollTo(0, -top, duration);
    setTimeout(callback,duration);
  }
  scrollMenuInst.scrollTop = funciton(){
    return -iScrollInst.y;
  }
  scrollMenInst._scrollHeight = funciton(){
    return this.container.children().height();
  }
  iScrollInst.on('scroll', function(){
    scrollMenuInst.onScroll();
  });
  scrollMenuInst.onScroll();
  return {
    scrollMenu: scrollMenuInst,
    iScroll: iScrollInst
  }
  
}

```

```
```

```
```

