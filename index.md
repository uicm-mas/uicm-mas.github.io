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
    
repo: 'https://github.com/uicm-mas/uicm-mas.github.io.git',
    
oauth: {
        client_id: 'e7c23936abdea2108b8c',
        
client_secret: 'f18edfb1aad0f67001855682e19fa4535026e2c5',
   
 },

});

gitment.render('gitmentContainer');

</script>

