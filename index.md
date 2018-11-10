---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<script>
var _hmt = _hmt || [];
(function() {
  var hm = document.createElement("script");
  hm.src = "https://hm.baidu.com/hm.js?9351512b626de5011fb5fb1143ce1721";
  var s = document.getElementsByTagName("script")[0]; 
  s.parentNode.insertBefore(hm, s);
})();
</script>

<div id="gitmentContainer">
</div>
<link rel="stylesheet" href="https://imsun.github.io/gitment/style/default.css">

<script src="https://imsun.github.io/gitment/dist/gitment.browser.js"></script>
<script>

var gitment = new Gitment({
    
owner: 'uicm-mas',
    
repo: 'https://github.com/uicm-mas/uicm-mas.github.io',
    
oauth: {
        client_id: '4d4c182500b44b523097',
        
client_secret: 'b74fcc3d903bc43ea35e5a803182ae4c65070185',
   
 },

});

gitment.render('gitmentContainer');

</script>

