<style type="text/css">
#topbar{
position:absolute;
padding-left:0%;padding-top:0%;
background-color: #999;
width: 340px;heigth:280px;
visibility: hidden;
z-index: 100;
}
</style> <script type="text/javascript">
var persistclose=0 //set to 0 or 1. 1 means once the bar is manually closed, it will remain closed for browser session
var startX = 30 //set x offset of bar in pixels
var startY = 5 //set y offset of bar in pixels
var verticalpos="fromtop" //enter "fromtop" or "frombottom"
function iecompattest(){
return (document.compatMode && document.compatMode!="BackCompat")? document.documentElement : document.body
}
function get_cookie(Name) {
var search = Name + "="
var returnvalue = "";
if (document.cookie.length > 0) {
offset = document.cookie.indexOf(search)
if (offset != -1) {
offset += search.length
end = document.cookie.indexOf(";", offset);
if (end == -1) end = document.cookie.length;
returnvalue=unescape(document.cookie.substring(offset, end))
}
}
return returnvalue;
}
function closebar(){
if (persistclose)
document.cookie="remainclosed=1"
document.getElementById("topbar").style.visibility="hidden"
}
function staticbar(){
barheight=document.getElementById("topbar").offsetHeight
var ns = (navigator.appName.indexOf("Netscape") != -1) || window.opera;
var d = document;
function ml(id){
var el=d.getElementById(id);
if (!persistclose || persistclose && get_cookie("remainclosed")=="")
el.style.visibility="visible"
if(d.layers)el.style=el;
el.sP=function(x,y){this.style.left=x+"px";this.style.top=y+"px";};
el.x = startX;
if (verticalpos=="fromtop")
el.y = startY;
else{
el.y = ns ? pageYOffset + innerHeight : iecompattest().scrollTop + iecompattest().clientHeight;
el.y -= startY;
}
return el;
}
window.stayTopLeft=function(){
if (verticalpos=="fromtop"){
var pY = ns ? pageYOffset : iecompattest().scrollTop;
ftlObj.y += (pY + startY - ftlObj.y)/8;
}
else{
var pY = ns ? pageYOffset + innerHeight - barheight: iecompattest().scrollTop + iecompattest().clientHeight - barheight;
ftlObj.y += (pY - startY - ftlObj.y)/8;
}
ftlObj.sP(ftlObj.x, ftlObj.y);
setTimeout("stayTopLeft()", 5);
}
ftlObj = ml("topbar");
stayTopLeft();
}
if (window.addEventListener)
window.addEventListener("load", staticbar, false)
else if (window.attachEvent)
window.attachEvent("onload", staticbar)
else if (document.getElementById)
window.onload=staticbar
</script>
<div class="clear">
</div>
<div id="topbar">
<div style="text-align: right;">
<a href="" onclick="closebar(); return false"><img src="https://1.bp.blogspot.com/-w8r2c9UH4V8/X86mH8GW2oI/AAAAAAAADlc/Da7xVb-k2XAkG70LqT5wduVROmxFjJQOQCLcBGAsYHQ/s640/tombolclose.png" width="25"/></a>
<br/><center><span style="color: white; font-size: small;">Klik (x) untuk menutup</span></center><center><b><span style="color: white;">Jangan lupa! Klo mo beli sandal ama admin aja ya, tersedia sandal Bandung kwalitas premium, 100% dijamin Ori</span></b><br/><center><a href="https://sandalbandung.web.id"><img border="0" data-original-height="648" data-original-width="2024" height="50" src="https://1.bp.blogspot.com/-Z0KOdrcCQsA/X890l3KItwI/AAAAAAAADl8/mJIwUzLlxr8OC0MshyPouEcPz7rw9cYgQCLcBGAsYHQ/w200-h64/AddText_12-08-07.13.23.png" width="150" /></a>
</center></center></div>
<div style="background: #999;">
</div></div> 
