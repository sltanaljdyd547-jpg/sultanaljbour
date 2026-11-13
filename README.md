# sultanaljbour
<html lang="ar" dir="rtl"><style>* { -webkit-text-size-adjust: 109.00000000000001% !important; }</style><head><style>
@font-face {
  font-family: "Optimistic";
  font-style: normal;
  font-weight: 400 600;
  font-display: swap;
  src: url("/fonts/OptimisticAI_VF_Optimized.woff2") format("woff2");
}
@font-face {
  font-family: "Optimistic Mono";
  font-style: normal;
  font-weight: 400;
  font-display: swap;
  src: url("/fonts/OptimisticMono_W_TextRegular.woff2") format("woff2");
}
:where(html) {
  font-family: "Optimistic", system-ui, sans-serif;
}
:where(code, pre, kbd, samp) {
  font-family: "Optimistic Mono", ui-monospace, monospace;
}
</style><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<title>بطاقات حفظ - سلطان الجبور</title>
<style>
*{box-sizing:border-box}body{margin:0;background:#0f1220;color:#fff;font-family:-apple-system,BlinkMacSystemFont,sans-serif;padding:12px}
.header{text-align:center;padding:10px 0} .header h1{font-size:20px;margin:0} .header p{color:#aab;margin:4px 0;font-size:14px}
.card{background:#1e2340;border-radius:18px;padding:28px 18px;text-align:center;margin:14px 0;min-height:260px;display:flex;flex-direction:column;justify-content:center}
.en{font-size:20px;font-weight:800;line-height:1.4;direction:ltr} .ar{font-size:18px;line-height:1.8;margin-top:16px;color:#e8eaf6}
.btns{display:flex;gap:8px} button{flex:1;padding:14px;border:0;border-radius:12px;font-size:16px;font-weight:700;cursor:pointer}
.prev,.next{background:#2a2f55;color:#fff} .known{background:#10b981;color:#fff} .not{background:#f59e0b;color:#111}
.row{display:flex;gap:8px;margin-top:8px} .prog{height:8px;background:#2a2f55;border-radius:99px;overflow:hidden} .prog div{height:100%;background:#6366f1}
.footer{text-align:center;color:#889;font-size:12px;margin-top:14px}
</style></head><body>
<div class="header"><h1>بطاقات حفظ • سلطان الجبور</h1><p>Software Costs</p><p id="counter">بطاقة 1 من 5</p><div class="prog"><div id="bar" style="width:20%"></div></div></div>
<div class="card" onclick="flip()"><div id="front" style="display: block;"><div class="en" id="en">Software costs often dominate computer system costs.</div><div class="ar" id="ar">تكاليف البرمجيات غالباً بتسيطر على تكاليف نظام الكمبيوتر كله.</div></div><div id="back" style="display:none"><div class="ar" id="exp">السوفتوير هو أكبر تكلفة في النظام كله، مش الهاردوير.</div></div></div>
<div class="btns"><button class="next" onclick="prev()">السابق →</button><button class="next" onclick="next()">← التالي</button></div>
<div class="row"><button class="not" onclick="next()">لسا</button><button class="known" onclick="next()">✓ عرفت؟</button></div>
<p class="footer">من عمل سلطان الجبور • للدراسة والمراجعة</p>
<script>
const data=[
{en:"Software costs often dominate computer system costs.",ar:"تكاليف البرمجيات غالباً بتسيطر على تكاليف نظام الكمبيوتر كله.",exp:"السوفتوير هو أكبر تكلفة في النظام كله، مش الهاردوير."},
{en:"The costs of software on a PC are often greater than the hardware cost.",ar:"تكلفة السوفتوير على الـ PC غالباً أكبر من تكلفة الهاردوير.",exp:"جهازك نفسه أرخص من البرامج اللي عليه."},
{en:"Software costs more to maintain than it does to develop.",ar:"السوفتوير بيكلف صيانة أكتر مما بيكلف تطوير.",exp:"بنبنيه مرة، بس بنضل نصلح ونحدث فيه طول عمره."},
{en:"For systems with a long life, maintenance costs may be several times development costs.",ar:"للأنظمة اللي عمرها طويل، الصيانة ممكن تكون أضعاف التطوير.",exp:"كل ما عاش النظام أكتر، صيانته صارت أغلى بكتير."},
{en:"Software engineering is concerned with cost-effective software development.",ar:"هندسة البرمجيات بتهتم بتطوير سوفتوير فعّال من ناحية التكلفة.",exp:"هدف هندسة البرمجيات: سوفتوير كويس وبأقل تكلفة."},
];
let i=0,flipped=false;
function render(){document.getElementById('en').textContent=data[i].en;document.getElementById('ar').textContent=data[i].ar;document.getElementById('exp').textContent=data[i].exp;document.getElementById('counter').textContent='بطاقة '+(i+1)+' من 5';document.getElementById('bar').style.width=((i+1)/5*100)+'%';document.getElementById('front').style.display='block';document.getElementById('back').style.display='none';flipped=false;}
function flip(){flipped=!flipped;document.getElementById('front').style.display=flipped?'none':'block';document.getElementById('back').style.display=flipped?'block':'none';}
function next(){i=(i+1)%5;render()} function prev(){i=(i-1+5)%5;render()} render();
</script><script>(function(){var loc=location.href.replace(/#.*$/,"");var ATTR_NAMES=["data-product-id","data-productid","data-product_id","product-id","productid","product_id","data-source-entity-id","source-entity-id","source_entity_id","data-product","data-metadata","data-meta"];var DATASET_KEYS=["productId","productid","product_id","sourceEntityId","sourceentityid","source_entity_id","product","metadata","meta"];function readProductId(value){if(typeof value!=="string"||value.length===0)return null;if(/^[0-9]{6,}$/.test(value))return value;var match=value.match(/(?:product(?:_|-)?id|source(?:_|-)?entity(?:_|-)?id)["'=:\s]+([0-9]{6,})/i);return match?match[1]:null}function extractProductId(start){for(var node=start;node&&node!==document.body;node=node.parentElement){for(var i=0;i<ATTR_NAMES.length;i++){var attrValue=node.getAttribute&&node.getAttribute(ATTR_NAMES[i]);var attrProductId=readProductId(attrValue);if(attrProductId)return attrProductId}var dataset=node.dataset||null;if(dataset){for(var j=0;j<DATASET_KEYS.length;j++){var dataValue=dataset[DATASET_KEYS[j]];var dataProductId=readProductId(dataValue);if(dataProductId)return dataProductId}}}return null}function isInlineMediaSlotElement(node){return !!(node&&node.getAttribute&&node.getAttribute("data-clippy-inline-media-slot")!==null)}function findInlineMediaSlot(start){for(var node=start;node&&node!==document.body;node=node.parentElement){if(isInlineMediaSlotElement(node))return node}return null}function readInlineMediaUrl(node){if(!node)return null;return node.getAttribute&&((node.getAttribute("data-clippy-inline-media-url")||node.getAttribute("data-url")||node.getAttribute("data_url")))||node.href||null}function stripHash(url){return String(url).replace(/#.*$/,"")}function urlsMatch(a,b){if(!a||!b)return false;try{return stripHash(new URL(a,loc).href)===stripHash(new URL(b,loc).href)}catch(_){return stripHash(a)===stripHash(b)}}function isFirstPartyReelUrl(value){try{var url=new URL(value,loc);if(url.protocol!=="https:")return false;var host=url.hostname.toLowerCase();var supported=host==="instagram.com"||host.endsWith(".instagram.com")||host==="facebook.com"||host.endsWith(".facebook.com");return supported&&/\/reels?\//i.test(url.pathname)}catch(_){return false}}function isInlineMediaUrlClick(node,href){var slot=findInlineMediaSlot(node);if(!slot)return false;var slotUrl=readInlineMediaUrl(slot);if(slotUrl)return urlsMatch(href,slotUrl);return isFirstPartyReelUrl(href)}function findDataHref(start){for(var node=start;node&&node!==document.body;node=node.parentElement){if(node.getAttribute){var href=node.getAttribute("data-href")||node.getAttribute("data-url");if(href)return{href:href,node:node}}}return null}var nativeOpen=window.open;window.open=function(url){if(parent!==window&&typeof url==="string"&&/^https?:\/\//.test(url)){parent.postMessage({type:"ecto:usercontent-link-click",href:url},"*");return null}return nativeOpen?nativeOpen.apply(window,arguments):null};document.addEventListener("click",function(e){var target=e.target instanceof Element?e.target:null;if(!target)return;if(parent===window)return;var a=target.closest?target.closest("a[href]"):null;if(a&&a.href&&/^https?:\/\//.test(a.href)&&a.href.replace(/#.*$/,"")!==loc){if(isInlineMediaUrlClick(a,a.href))return;var productId=extractProductId(target)||extractProductId(a);if(productId){e.preventDefault();parent.postMessage({type:"ecto-artifact-link-click",productId:productId},"*");return}e.preventDefault();parent.postMessage({type:"ecto:usercontent-link-click",href:a.href},"*");return}var dataHref=findDataHref(target);if(dataHref&&/^https?:\/\//.test(dataHref.href)&&dataHref.href.replace(/#.*$/,"")!==loc){if(isInlineMediaUrlClick(dataHref.node,dataHref.href))return;e.preventDefault();parent.postMessage({type:"ecto:usercontent-link-click",href:dataHref.href},"*")}},true)})();</script><script>(function(){var FOCUS_TYPE="ecto:artifact-focus-request";var CLOSE_TYPE="ecto:artifact-close-request";function focusArtifactDocument(){var body=document.body;if(!body)return;try{window.focus();}catch(e){}if(!body.hasAttribute("tabindex"))body.setAttribute("tabindex","-1");try{body.focus({preventScroll:true});}catch(e){try{body.focus();}catch(e2){}}}window.addEventListener("message",function(event){if(event.source!==window.parent)return;var data=event.data;if(!data||typeof data!=="object"||data.type!==FOCUS_TYPE)return;if(document.readyState==="loading"){document.addEventListener("DOMContentLoaded",focusArtifactDocument,{once:true});return;}focusArtifactDocument();});window.addEventListener("keydown",function(event){if(event.key!=="Escape")return;window.setTimeout(function(){if(event.defaultPrevented)return;window.parent.postMessage({type:CLOSE_TYPE},"*");},0);});})();</script></body></html>