# :bookmark: :notebook_with_decorative_cover: Bookmarklets-Grimoire :notebook_with_decorative_cover: :notebook:

This is a hub for all things Bookmarklet related. Many are #OSINT related, but there should be something here for everyone. From lists of awesome bookmarklets themselves, places to find other bookmarklets, ways to find plenty more, to tutorials on how to quickly create your own, hopefully you'll find this place useful. I've noticed that bookmarklets don't get nearly the credit and praise as they should. It's an old technology, but because of how awesome they are, I would expect to find tons of collection lists, or collections of info like this one, but I haven't. That's what motivated me to start this. Anyways, thank you! Please bookmark, star, contribute, etc, and please return regularly for new and updated content! 

Things to Note:
    
1 - Please excuse the mess!! The way my dumb ass likes to work is by taking all the ingrediants, tossing them onto the nearest wall, and then making sense of everything afterwords. While I won't insult you by doing that entirely, now and then things won't be in the correct order, etc. I will fix these issues ASAP. This is a work in progress, never complete. 
    
2 - I try my best to credit everyone for their work, but sometimes sources were saved back when I didn't expect to collect them into something public. If you see any of your work here, please contact me and I will immediately credit you, or remove it if you wish. That said, I'll try to do that as little as possible.



![image](https://github.com/user-attachments/assets/ba7ed1d2-d7b7-45c8-a2a0-52d8622ea9a6)


---


# 📜 - **Table of Contents** :

  ## 🧩 BOOKMARKLETS —

  ### GENERAL -

### SITE-SPECIFIC -

### DEV-RELATED - 

### EASE-OF-USE - 

### MENUS-OR-COLLECTIONS - 

### GUI - 

### SORT - 


> *Just mouse over the code and click the Copy button on the top right. Make a new bookmark, name it and then paste the code in the URL to create the bookmarklet.*

---

Template (ignore) -
```jsx
   
```



    
- PAGE NAVIGATION & MANAGEMENT —
    - Paywall/Annoying Message Remover -
        
        ```jsx
        javascript:(function()%7B(function () %7Bvar i%2C elements %3D document.querySelectorAll("body *")%3Bfor (i %3D 0%3B i < elements.length%3B i%2B%2B) %7Bif (getComputedStyle(elements%5Bi%5D).position %3D%3D%3D "fixed") %7Belements%5Bi%5D.parentNode.removeChild(elements%5Bi%5D)%3B%7D%7D%7D)()%7D)()
        ```
        
    - Page Increment —
        
        ```jsx
        javascript:(function(){ var e,s; IB=1; function isDigit(c) { return ("0" <= c && c <= "9") } L = location.href; LL = L.length; for (e=LL-1; e>=0; --e) if (isDigit(L.charAt(e))) { for(s=e-1; s>=0; --s) if (!isDigit(L.charAt(s))) break; break; } ++s; if (e<0) return; oldNum = L.substring(s,e+1); newNum = "" + (parseInt(oldNum,10) + IB); while (newNum.length < oldNum.length) newNum = "0" + newNum; location.href = L.substring(0,s) + newNum + L.slice(e+1); })();
        ```
        
    - Page Decrement —
        
        ```jsx
        javascript:(function(){ var e,s; IB=-1; function isDigit(c) { return ("0" <= c && c <= "9") } L = location.href; LL = L.length; for (e=LL-1; e>=0; --e) if (isDigit(L.charAt(e))) { for(s=e-1; s>=0; --s) if (!isDigit(L.charAt(s))) break; break; } ++s; if (e<0) return; oldNum = L.substring(s,e+1); newNum = "" + (parseInt(oldNum,10) + IB); while (newNum.length < oldNum.length) newNum = "0" + newNum; location.href = L.substring(0,s) + newNum + L.slice(e+1); })();
        ```

     - Page Element Isolator —
        
        ```jsx
        javascript:void%28%28%29%3D%3E%7B%28function%28%29%7B%22use%20strict%22%3Bfunction%20m%28t%29%7Blet%20a%2Co%3Dt%2Cs%3Dt.tagName.toLowerCase%28%29%2Ci%3D%22%22%2Cd%3D%22%22%2Cl%3D%22%22%2Cr%3D%22%22%3Bfor%28%3Bo.parentNode%3B%29%7Bif%28%28a%3Do.parentNode%29.tagName%29%7Bi%3Da.tagName.toLowerCase%28%29%3Blet%20c%3Da.querySelectorAll%28%22%3Ascope%20%3E%20%22+o.tagName%29%3Bl%3Dc.length%3E1%3F%22%5B%22+parseInt%28Array.from%28c%29.indexOf%28o%29+1%29+%22%5D%22%3A%22%22%2Cd%3D%28s%3Do.tagName.toLowerCase%28%29%29+l+r+d%2Cr%3D%22/%22%7D%0Ao%3Da%7D%0Areturn%20i%3D%3D%3D%22%22%26%26%28i%3Ds%29%2Cd%3D%22//%22+i+l+r+d%7D%0Afunction%20y%28%29%7Blet%20t%2Ca%2Co%2Cs%3D%210%2Ci%3D%211%2Cd%3Ddocument.querySelectorAll%28%22*%22%29%3Bfunction%20l%28e%2Cn%29%7Bt%3De%2Cn.stopPropagation%28%29%2Ci%7C%7Cc%28e%29%2Cp%28t%29%7D%0Afunction%20r%28e%29%7Be.classList.remove%28%22isolatorHighlight%22%29%7D%0Afunction%20c%28e%29%7Be.classList.add%28%22isolatorHighlight%22%29%7D%0Afunction%20p%28e%29%7Bconsole.clear%28%29%2Cconsole.log%28m%28e%29%29%2Co.innerHTML%3Dm%28e%29%7D%0AArray.from%28d%29.forEach%28e%3D%3E%7Be.addEventListener%28%22click%22%2Cn%3D%3E%7Bconsole.log%28%22preventClicks%20%3D%20%22%2Cs%29%2Cs%26%26%28function%28f%2Cu%29%7Bt%3Df%2Cf.tagName%3D%3D%3D%22HTML%22%26%26%28s%3D%211%29%2Cfunction%28g%29%7Bif%28%21i%29%7Blet%20h%3Dg.parentNode%2Cv%3Dh.childNodes%3Bh.tagName%21%3D%3D%22HTML%22%3FArray.from%28v%29.forEach%28x%3D%3E%7Bx%21%3D%3Dg%26%26x.remove%28%29%7D%29%3Ai%3D%210%7D%7D%28f%29%7D%28e%29%2Cn.preventDefault%28%29%29%7D%29%2Ce.addEventListener%28%22mouseover%22%2Cn%3D%3E%7Bt%3De%2Cn.stopPropagation%28%29%2Ci%7C%7Cc%28e%29%2Cp%28t%29%7D%29%2Ce.addEventListener%28%22mouseout%22%2Cn%3D%3E%7Br%28e%29%7D%29%7D%29%2Cfunction%28%29%7Blet%20e%3Ddocument.createElement%28%22style%22%29%3Be.textContent%3D%22.isolatorHighlight%7Boutline%3A4px%20solid%20black%21important%3Boutline-offset%3A-4px%21important%3B-webkit-box-shadow%3A%200px%200px%200px%204px%20%23fff%3B%20box-shadow%3A%200px%200px%200px%204px%20%23fff%3B%7D%23infoPanel%20%7Bz-index%3A1000%3Bfont-size%3A20px%3Bbackground%3Argba%280%2C0%2C0%2C0.8%29%3Bcolor%3A%23fff%3Bfont-weight%3Abold%3Bpadding%3A10px%3Bposition%3Afixed%3Bbottom%3A20px%3Bleft%3A20px%3Bfont-family%3Asans-serif%3B%7D%20%23infoPanel%3Aempty%20%7Bvisibility%3Ahidden%3B%7D%20%23infoPanel%20code%20%7Bcolor%3Alime%7D%22%2Cdocument.head.appendChild%28e%29%7D%28%29%2C%28o%3Ddocument.createElement%28%22div%22%29%29.setAttribute%28%22id%22%2C%22infoPanel%22%29%2Co.setAttribute%28%22role%22%2C%22status%22%29%2Cdocument.body.appendChild%28o%29%2Cdocument.addEventListener%28%22keydown%22%2Cfunction%28e%29%7Bif%28e.key%3D%3D%3D%22ArrowUp%22%26%26%28e.preventDefault%28%29%2Ct.parentNode%26%26t.tagName%21%3D%3D%22HTML%22%26%26%28r%28t%29%2Cconsole.log%28%22currentEl.parentNode%20%3D%20%22%2Ct.parentNode%29%2Ca%3Dt.parentNode%2Cc%28t%3Da%29%29%2Cp%28t%29%2Co.textContent%3Do.textContent+%22%20%28Press%20Return%20to%20isolate%20this%20element%29%22%29%2Ce.key%3D%3D%3D%22ArrowLeft%22%26%26%28e.preventDefault%28%29%2Ct.previousElementSibling%26%26%28r%28t%29%2Cl%28t%3Dt.previousElementSibling%2Ce%29%29%29%2Ce.key%3D%3D%3D%22ArrowRight%22%26%26%28e.preventDefault%28%29%2Ct.nextElementSibling%26%26%28r%28t%29%2Cl%28t%3Dt.nextElementSibling%2Ce%29%29%29%2Ce.key%3D%3D%3D%22ArrowDown%22%26%26%28e.preventDefault%28%29%2Ct.childNodes.length%3E1%29%29%7Br%28t%29%3Blet%20n%2Cf%3D%211%3BArray.from%28t.childNodes%29.forEach%28u%3D%3E%7Bu.nodeType%21%3D%3D1%7C%7Cf%7C%7C%28f%3D%210%2Cn%3Du%29%7D%29%2Cn%26%26l%28t%3Dn%2Ce%29%7D%0Ae.key%3D%3D%3D%22Enter%22%26%26%28e.preventDefault%28%29%2Ct.click%28%29%29%7D%29%2Cp%28%22Isolator%20started.%20Click%20on%20element%20you%20want%20to%20isolate%20in%20the%20DOM%22%29%7D%0Ay%28%29%7D%29%28%29%3B%7D%29%28%29%3B

        ```
---
SORT -- 

Yandex Reverse Image - Click the bookmarklet, then click on any image currently on the page
```jsx
javascript:javascript%3Afunction yandexify%28event%29%7Blet img%3Devent.target%3Blet y%3D%27https%3A//yandex.com/images/search%3Frpt%3Dimageview%26url%3D%27%3Bwindow.open%28y+img.src%29%3Bimg.removeEventListener%28%27click%27%2Cyandexify%29%3B%7D%0AArray.from%28document.querySelectorAll%28%27img%27%29%29.forEach%28el%3D>el.addEventListener%28%27click%27%2Cyandexify%29%29%3B   
```

View all images on page -
  ```jsx
  javascript:void (()=>%7B(function()%7B"use strict";function v()%7Bconsole.clear();function f(e)%7Blet r=window.getComputedStyle(e);return r.display==="none"%7C%7Cr.opacity===0%7C%7Cr.clipPath==="inset(100%25)"&&r.clip==="rect(1px, 1px, 1px, 1px)"%7C%7Cr.height==="1px"&&r.width==="1px"&&r.overflow==="hidden"%7Dfunction T(e)%7Blet r=window.getComputedStyle(e);r.position==="absolute"&&r.overflow==="hidden"&&(e.style.height="auto",e.style.width="auto",e.style.position="relative",e.style.overflow="visible",e.style.display="block",e.style.opacity=1),(e.getAttribute("hidden")===""%7C%7Ce.getAttribute("hidden")==="hidden"%7C%7Ce.getAttribute("hidden")==="true")&&e.removeAttribute("hidden"),r.visibility==="hidden"&&(e.style.visibility="visible"),r.display==="none"&&(e.style.display="block"),r.opacity===0&&(e.style.opacity=1)%7Dlet l="",o="",k=document.querySelectorAll("img,%5Brole=img%5D"),d=1,u,m=0,b="",c="";Array.from(k).forEach(function(e)%7Blet r=document.createElement("div");r.appendChild(e.cloneNode(!0)),b=r.innerHTML;let t="",p=!1,y=!1,a=!1,n=!1,w=e.querySelector("%5Baria-hidden=true%5D");w&&w.classList.add("remove-from-accname"),e.setAttribute("data-img-ref",d);let i=e.getAttribute("alt");i===null?(i="NO_ALT_ATTRIBUTE",p=!0):i===""&&(i="EMPTY_ALT_ATTRIBUTE",y=!0);let s=i,A=e.getAttribute("src");if(f(e)&&(T(e),f(e)?t+="img is hidden.<br>":t+="img *was* hidden but has been temporarily revealed on the page.<br>"),p&&(e.getAttribute("role")==="img"&&e.tagName!=="IMG"%7C%7C(t="- img has no <code>alt</code> attribute.<br>",n=!0)),y&&(t="- img has an empty <code>alt</code> attribute. This will hide it from AT. Is this correct?.<br>",a=!0),(e.getAttribute("role")==="presentation"%7C%7Ce.getAttribute("role")==="none")&&(t+="- img has a <code>role</code> set (%27"+e.getAttribute("role")+"%27) that will hide it from AT. Is this correct?.<br>",a=!0),e.getAttribute("aria-hidden")==="true"&&(t+="- img has an <code>aria-hidden=true</code>, so it will be hidden from AT. Is this correct?.<br>",a=!0),e.getAttribute("title")&&(i==="EMPTY_ALT_ATTRIBUTE"?(t+="- img has a <code>title</code> AND an empty <code>alt</code> attribute. Because of the empty alt, the image will be hidden to AT, so the title attribute is not used/exposed.<br>",a=!1,n=!0):(t+=%27- img has a <code>title</code> attribute. This <code>title</code> content -- "%27+e.getAttribute("title")+%27" -- will not be perceivable to assistive tech, keyboard and touch screen users.<br>%27,p?n=!0:a=!0)),e.getAttribute("role")==="button"&&(t+="- img has a <code>role</code> of <code>button</code>. Check that it behaves like a <code>button</code>.<br>",a=!0),e.getAttribute("role")==="img"&&(t+="- Not an inline img, so no <code>alt</code> attribute.<br>"),e.getAttribute("role")==="img"&&e.getAttribute("alt")!==null&&e.tagName!=="IMG"&&(t+="- Background image has an <code>alt</code> attribute specified, but cannot be applied to this element; can only be applied to <code>img</code> element.<br>",a=!1,n=!0),e.tagName!=="IMG"&&e.getAttribute("role")==="img"&&(t+="- This has a <code>role</code> of <code>img</code> but is not an <code>img</code> element.<br>"),e.getAttribute("role")==="img")%7Blet h=!1;if(e.tagName!=="IMG")%7Blet I=e.currentStyle%7C%7Cwindow.getComputedStyle(e,!1),S=I.backgroundImage.slice(4,-1).replace(/"/g,"");if(e.getAttribute("aria-label")!==null&&(h=!0,i=e.getAttribute("aria-label"),s=i,t+="- Accessible name provided by an <code>aria-label</code> attribute.<br>",a=!1),!h&&e.getAttribute("aria-labelledby")!==null)%7Bh=!0;let x=e.getAttribute("aria-labelledby").split(" ");x.length>1?(i="",Array.from(x).forEach(function(B)%7Bi+=document.querySelector("#"+B).textContent+" "%7D),i=i.trim(),t+="- Image gets accessible name from <code>aria-labelledby</code> (multiple sources). Check that the accessible name does not contradict the image on screen<br>",a=!0):(i=document.querySelector("#"+e.getAttribute("aria-labelledby")).textContent,t+="- Image gets accessible name from <code>aria-labelledby</code> (single source). Check that the accessible name does not contradict the image on screen<br>",a=!0),s=i%7D%7Dh%7C%7C(t+="- Image has no accessible name provided. It must be set using <code>aria-labelledby</code> or <code>aria-label</code> (not <code>alt</code>)<br>",n=!0)%7Ds===""&&(e.getAttribute("title")?s=e.getAttribute("title"):s="%5Cu203C%5CuFE0F No alt, no title",t+="%5Cu203C%5CuFE0F No alt.<br>",n=!0),n&&(a=!1),o+="<tr",o+=' data-img-ref="'+d+'"',a&&(o+=' class="issue warn"'),n&&(o+=' class="issue err"'),o+=">",e.tagName==="IMG"?u="<code><img></code>":u='<code>role="img"</code>',(s==="NO_ALT_ATTRIBUTE"%7C%7Cs==="EMPTY_ALT_ATTRIBUTE")&&(i="",s=""),o+="<td>"+u+"</td>",o+='<td><img src="'+A+'" alt="" style="max-width:200px;max-height:200px;"></td>',o+="<td>"+s,s.trim()!==i.trim()&&i.trim()!==""&&(o+='<div class="anDiff">Accessible name differs</div>'),o+="</td>",s.trim()!==i.trim()&&s.trim().toLowerCase()===i.trim().toLowerCase()&&(t+="- Same text but case difference noted (likely not an issue)"),o+="<td>",a&&(o+='<div class="issues">Possible issue(s) found with this image</div>'),n&&(o+='<div class="issues">Definite issue(s) found with this image</div>',c="Image '"+A+%60':%0A%60+t+%60Markup with issue:%0A%60+b+%60%0A---------------%0A%60),o+=t+'<button class="showSnippet" type="button" aria-label="Show markup snippet" aria-expanded="false"><code></></code></button><div class="snippet" hidden><label for="snip'+d+'">Markup snippet</label><textarea id="snip'+d+'" aria-label="Markup snippet for this node">'+b+'</textarea><button type="button" class="decrapulate" aria-label="De-crapulate this markup snippet">De-crapulate</button></div></td>',o+='<td><button data-img-ref="'+d+'" class="highlightButton" type="button" aria-pressed="false" aria-label="Highlight this issue on the page visually">Show</button></td>',o+="</tr>",d++,(a%7C%7Cn)&&(m++,c=c.split("<code>").join("%60").split("</code>").join("%60").split("<br>").join(%60%0A%60).split(%60%0A%0A%60).join(%60%0A%60),console.log(c))%7D),l='<style>%5Baria-pressed=true%5D%7Bcolor:white;background:darkred;%7D;div.issues%7Bfont-weight:bold;%7D;textarea %7Bmargin:5px 0;%7D.snippet label %7Bfont-weight:bold;font-size:0.8em;color:black;%7D.snippet%7Bbackground:#efefef;outline:1px solid #666;padding:5px;margin-top:5px;%7D.checkDiffs%7Bbackground:PapayaWhip;%7D.anDiff%7Bcolor:red;font-weight:bold;font-size:10px;display:block%7D.warn %7Bbackground:lightyellow;%7D.err %7Bbackground:PapayaWhip;color:red;%7D.visually-hidden,.a11y,.visuallyhidden,.sr-text,.sr-only %7Bclip-path: inset(100%25);clip: rect(1px, 1px, 1px, 1px);height: 1px;overflow: hidden;position: absolute;white-space: nowrap;width: 1px;%7D* %7B-webkit-box-sizing: border-box;box-sizing: border-box;%7Dhtml %7B/*border: .75em solid #fff;*/min-height: 100vh;%7Dbody %7Bbackground: #f7f7f5;color: #333;font: 400 105%25/1.4 "Work Sans", sans-serif;margin: 1.5em auto;max-width: 54em;width: 90%25;%7Da:img,a:visited %7Bborder-bottom: 1px solid rgba(42, 122, 130, .5);color: #2b7a82;text-decoration: none;%7Da:hover %7Bborder-bottom: 2px solid;color: #1e565c;%7Dbutton:focus,a:focus %7Bbox-shadow: none;outline-offset: 2px;outline: 3px solid rgba(42, 122, 130, .75);%7Da:focus %7Bborder-bottom: none;%7Da:active %7Bbackground: #333;color: #fff;%7Dcode %7Bfont-family: Consolas, monaco, monospace;-moz-tab-size: 4;tab-size: 4;text-transform: none;white-space: pre-wrap;color:brown;%7Dtextarea %7Bwidth: 100%25%7Dlegend h2, legend h3 %7Bmargin: 0;%7Dtable %7Bborder-collapse: collapse;%7Dth,td %7Bpadding: 10px;border:2px solid #2b7a82;%7Dtable caption %7Bfont-weight: bold;text-align: left;margin:1em 0;%7D</style><h1>List of images on this page.</h1>',l+='<input type="checkbox" id="showPotentialProblemsOnly"><label for="showPotentialProblemsOnly">Show only images where there *may* be issues ('+m+" found)</label>",l+=' <button class="highlightButtonAll" type="button" aria-pressed="false">Highlight all images on page</button>',l+='<table border="1" cellpadding="5"><caption>All images (img elements or elements with role="img") on this page, the accessible name and any issues found</caption><thead><tr valign=top><th>Image type</th><th>Image thumbnail</th><th scope="col">Accessible name</th><th scope="col">Notes</th><th>Highlight on the page</th></tr></thead><tbody>'+o+"</tbody></table>",l+="<script>function showImages()%7B",l+="var refWindow=window.opener;",l+=%60var highlightButtons=document.querySelectorAll(".highlightButton");var imgToHighlight;Array.from(highlightButtons).forEach(highlightButton => %7BhighlightButton.addEventListener("click", e => %7BimgToHighlight="%5Bdata-img-ref='" + highlightButton.getAttribute("data-img-ref") + "'%5D";if (highlightButton.getAttribute("aria-pressed")==="false") %7BrefWindow.document.querySelector(imgToHighlight).setAttribute("tabindex","-1");refWindow.document.querySelector(imgToHighlight).focus();refWindow.document.querySelector(imgToHighlight).style.outline="10px solid darkred";refWindow.document.querySelector(imgToHighlight).style.outlineOffset="-10px";highlightButton.setAttribute("aria-pressed","true");%7D else %7BrefWindow.document.querySelector(imgToHighlight).style.outline="";highlightButton.setAttribute("aria-pressed","false");%7D%7D);%7D);%60,l+='var highlightButtonAll=document.querySelector(".highlightButtonAll");highlightButtonAll.addEventListener("click", e => %7Bif (highlightButtonAll.getAttribute("aria-pressed")==="false") %7BArray.from(highlightButtons).forEach(highlightButton => %7BhighlightButton.setAttribute("aria-pressed","false");highlightButton.click();%7D);highlightButtonAll.setAttribute("aria-pressed","true");%7D else %7BArray.from(highlightButtons).forEach(highlightButton => %7BhighlightButton.setAttribute("aria-pressed","true");highlightButton.click();%7D);highlightButtonAll.setAttribute("aria-pressed","false");%7D%7D);',l+='var imgsToCopy=document.querySelectorAll(".imgToCopy");Array.from(imgsToCopy).forEach(imgToCopy => %7BimgToCopy.addEventListener("focus", e => %7BimgToCopy.select();%7D);%7D);',l+='function hideGoodRows()%7BArray.from(trsWithoutIssue).forEach(trWithoutIssue => %7BtrWithoutIssue.setAttribute("hidden","hidden");%7D);%7Dfunction showGoodRows()%7BArray.from(trsWithoutIssue).forEach(trWithoutIssue => %7BtrWithoutIssue.removeAttribute("hidden");%7D);%7Dvar trsWithoutIssue=document.querySelectorAll("tbody tr:not(.issue)");var showProblemCheckbox=document.querySelector("#showPotentialProblemsOnly");showProblemCheckbox.addEventListener("click", e => %7Bif (showProblemCheckbox.checked) %7BhideGoodRows();%7D else %7BshowGoodRows();%7D%7D);',l+='%7Dwindow.addEventListener("load", (event) => %7BshowImages();%7D);<%5C/script>';let g=window.open("","popUpWinImages","height=800,width=1000");g.document.open(),g.document.write(l),g.document.close()%7Dv()%7D)();%7D)();%0A
  ```

Edit - Click this to edit everything on the page! (for the most part. At least text, removing certain things, etc.)
```jsx
javascript:(function(){document.body.contentEditable = true;})()
```

Get a full list of links from page in a small popup -
```jsx
javascript:(function(){var e=[],t=document.getElementsByTagName("a"),n=t.length,r=window.open("","win","width=300,height=300");for(;n>0;n--){var i=t[n-1].getAttribute("href");t[n-1]!=null&&i!=null&&i.charAt(0)==="h"&&i.indexOf(window.location.hostname)==-1&&e.push("<li><a href="+i+">"+i+"</a></li>")}r.document.open("text/html","replace"),r.document.write("<h1>Links Found:</h1><ul>"+e.join("")+"</ul>")})() 
```

Robots.txt - Get info from the robots.txt for the page you're currently viewing -
```jsx
javascript:%28function%28%29%7Bvar%20t%3Ddocument.createElement%28%22style%22%29%3Bt.innerHTML%3D%22@import%20url%28%27https%3A//cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css%27%29%22%3Bdocument.head.appendChild%28t%29%3Bvar%20e%3Dfunction%28%29%7Bvar%20t%3Ddocument.createElement%28%22div%22%29%3Bt.className%3D%22fixed%20inset-0%20flex%20items-center%20justify-center%20bg-black%20bg-opacity-50%20z-50%22%3Bvar%20e%3Ddocument.createElement%28%22div%22%29%3Be.className%3D%22relative%20bg-white%20rounded-md%20shadow-lg%20p-6%20max-w-md%20mx-auto%20flex%20flex-col%20space-y-4%22%3Bt.appendChild%28e%29%3Bvar%20n%3Ddocument.createElement%28%22div%22%29%3Bn.className%3D%22overflow-auto%20max-h-96%22%2Ce.appendChild%28n%29%3Bvar%20o%3Ddocument.createElement%28%22button%22%29%3Bo.textContent%3D%22Close%22%2Co.className%3D%22bg-blue-500%20text-white%20px-3%20py-1%20rounded-md%20self-start%20mt-auto%22%2Ce.appendChild%28o%29%2Ct.addEventListener%28%22click%22%2Cfunction%28e%29%7Be.target%3D%3D%3Dt%26%26t.remove%28%29%7D%29%2Co.addEventListener%28%22click%22%2Cfunction%28%29%7Bt.remove%28%29%7D%29%2Cdocument.body.appendChild%28t%29%3Breturn%20n%7D%28%29%2Cn%3Ddocument.createElement%28%22pre%22%29%2Co%3Dlocation.protocol+%22//%22+location.hostname+%22/robots.txt%22%3Bfetch%28o%29.then%28function%28t%29%7Breturn%20t.text%28%29%7D%29.then%28function%28t%29%7Bn.textContent%3Dt%2Ce.innerHTML%3D%27%3Ch2%20class%3D%22text-xl%20font-semibold%20mb-4%22%3ERobots.txt%20Content%3C/h2%3E%3Cp%20class%3D%22text-gray-700%20mb-4%22%3EThe%20content%20of%20the%20robots.txt%20file%20is%20shown%20below%3A%3C/p%3E%3Ca%20href%3D%22%27+o+%27%22%20target%3D%22_blank%22%20class%3D%22text-blue-500%20mb-4%22%3EOpen%20robots.txt%20in%20a%20new%20tab%3C/a%3E%27%2Ce.appendChild%28n%29%7D%29.catch%28function%28t%29%7Bconsole.warn%28%22Error%20fetching%20robots.txt%3A%22%2Ct%29%7D%29%7D%29%28%29%3B 
```

Search a username in WhatsMyName.app which is a great little OSINT / SOCMINT tool -
```jsx
javascript:input = prompt("Enter username to search on WhatsMyName");wmn = ("https://whatsmyname.app/?q=%22)%20+%20input;function%20Wmn()%20{window.open(wmn);}Wmn();
```

Template (ignore) -
```jsx
   
```



    
- RANDOM —
- DEV —
- SAVING / ARCHIVE —
    - Persistent, safe Notes on Any Page —
        
        ```jsx
        javascript:(function(doc){doc.write('<body contenteditable style="font:12px monospace; max-width:50em; margin:0; padding:12px;">');var key = 'PixelRobot';var body = doc.querySelector('body');if (localStorage[key] != undefined)body.innerHTML = localStorage[key];else body.innerHTML = 'Notes:';body.oninput = function(){localStorage[key] = body.innerHTML;}})(document);
        ```


## 🧰 Learning to Code Bookmarklets :

## 🔹 **Examples and Templates** :

- **Some Useful Templates** - GENERAL —  [(source)](https://github.com/sinwindie/OSINT/blob/master/Bookmarklet%20Templates)
    - Template for extracting targeted text from source code:
        
        ```jsx
        javascript:   
        var html = document.documentElement.innerHTML;        
        var subhtml = html.split('$leftlimittext’)[1];  
        var output = subhtml.split('$rightlimittext’)[0];  
        alert(output)
        ```
        
    - Template for running multiple URL-structured queries
        
        ```jsx
        javascript:   
        var input = prompt("Prompt user for Input");     
        
        var variable1 = "$URLSTRUCTUREONE" + input;  
        var variable2 =  "$URLSTRUCTURETWO" + input;
        var variable3 =  "$URLSTRUCTURETHREE" + input;
        
        SiteOneFunction(); 
        SiteTwoFunction(); 
        SiteThreeFunction(); 
        
        function SiteOneFunction() {   setTimeout(function(){ window.open(variable1, "_blank"); }, 1000); }  
        function SiteTwoFunction() {   setTimeout(function(){ window.open(variable2, "_blank"); }, 1000); }  
        function SiteThreeFunction() {   setTimeout(function(){ window.open(variable3, "_blank"); }, 1000); }
        ```
        
    - Tumblr Examples — ([source](https://raw.githubusercontent.com/sinwindie/OSINT/master/Tumblr/Bookmarklet%20Tools))
        
        ```jsx
        Copy and Paste the Javascript bookmarklets below to create new bookmarks in your browser. 
        These bookmarklets will facilitate Tumblr investigations.
        
        In order for the bookmarklets to work, you must be currently browsing the home page of a Tumblr blog (such as example.tumblr.com)
        at the time you click on the bookmark button.
        
        Tumblr Archive
        javascript: {  var currentLocation = window.location.hostname;  
        var newLocation = currentLocation + "/archive";  
        window.location.replace("http://" + newLocation);   }
        
        Tumblr Full Photo Viewer
        javascript: {  var currentLocation = window.location.hostname;  
        var newLocation = currentLocation + "/avatar/512";  
        window.location.replace("https://api.tumblr.com/v2/blog/" + newLocation);   }
        
        Tumblr Likes
        javascript: {  var currentLocation = window.location.hostname;  
        var newLocation = currentLocation + "/likes";  
        window.location.replace("http://" + newLocation);   }
        
        Tumblr Following
        javascript: {  var currentLocation = window.location.hostname;  
        var newLocation = currentLocation + "/following";  
        window.location.replace("http://" + newLocation);   }
        
        Tumblr Followers
        javascript: {  var currentLocation = window.location.hostname;  
        var newLocation = currentLocation + "/followers";  
        window.location.replace("http://" + newLocation);   }
        
        ```
        
  ### - OSINT --
        
    - Tik-Tok:
        
        ```jsx
        #The below code allows you to open the full size photo of a TikTok user when you are looking at their profile.
        Just copy the below code into a new Bookmark in your browser, navigate to a user's profile, and click the new 
        bookmark to give it a try!
        
        javascript: 
        var html = document.documentElement.innerHTML;     
        var subhtml = html.split('background-image:url(')[1];  
        var subhtml2 = subhtml.split(')')[0];  
        window.open(subhtml2,"_self");
        
        #Prompts the user for a TikTok username and then opens that user's profile if it exists.
        
        javascript:  
        var username = prompt("Please enter TikTok username: ");   
        var url = "https://www.tiktok.com/@" + username;   
        window.open(url,"_self");
        
        #Prompts the user for a TikTok HashTag and then opens a search for that HashTag
        
        javascript:  
        var hashtag = prompt("Please enter TikTok HashTag: ");   
        var url = "https://www.tiktok.com/tag/" + hashtag;   
        window.open(url,"_self");
        
        # All Bookmarklets below may be used while looking at a TikTok video in a web browser
        ###WARNING: YOU MUST REFRESH PAGE PRIOR TO CLICKING ANY OF THE BOOKMARKLETS BELOW
        # If you do not refresh the page of the video you are on prior to use then the info will be pulled from the 
        user's most recent video instead of the one you are currently looking at.
        
        #Displays a quickview of all important information about a video. 
        ###WARNING: If you are using Chrome you will not be able to copy/paste the urls. This is a known issue
        with Chrome caused by the use of newlines ("\n"). You can remove them if you must use Chrome but the output
        will no longer be formatted neatly.
        
        javascript: 
        var html = document.documentElement.innerHTML; 
        var photohtml = html.split('background-image: url(&quot;')[1]; 
        var photohtml2 = photohtml.split('&quot')[0]; photohtml2 = photohtml2.replace("_100x100", ""); 
        var photooutput = "Full-Size User Photo: " + photohtml2; 
        
        var datehtml = html.split('uploadDate":"')[1]; 
        var datehtml2 = datehtml.split('"')[0]; 
        var dateoutput = "Video Upload Time: " + datehtml2; var 
        
        thumbhtml = html.split('poster="')[1]; 
        var thumbhtml2 = thumbhtml.split('"')[0]; 
        var thumboutput = "Video Thumbnail: " + thumbhtml2; 
        
        var videohtml = html.split('poster="')[1]; 
        var videohtml2 = videohtml.split('" loop=')[0]; 
        videohtml2 = videohtml2.split('src="')[1]; 
        videohtml2 = videohtml2.replace("amp;", ""); 
        var videooutput = "Video Download Link: " + videohtml2; 
        
        var fulloutput = (photooutput + "\n" + "\n" + videooutput + "\n" + "\n" + thumboutput + "\n"+ "\n" + dateoutput); 
        alert(fulloutput);
        
        #Opens the thumbnail for the current video
        
        javascript:  
        var html = document.documentElement.innerHTML;      
        var subhtml = html.split('poster="')[1];   
        var subhtml2 = subhtml.split('"')[0];  
        window.open(subhtml2,"_self");
        
        #Opens Full-Size Photo of user that posted the video
        
        javascript:    
        var html = document.documentElement.innerHTML; 
        var photohtml = html.split('background-image: url(&quot;')[1]; 
        var photohtml2 = photohtml.split('&quot')[0];    
        photohtml2 = photohtml2.replace("_100x100", ""); 
        window.open(photohtml2, "_self");
        
        #Opens video so that it can be downloaded. Just right-click when it opens and click save video as.
        
        javascript:  
        var html = document.documentElement.innerHTML;  
        var videohtml = html.split('poster="')[1]; 
        var videohtml2 = videohtml.split('" loop=')[0];  
        videohtml2 = videohtml2.split('src="')[1];  
        videohtml2 = videohtml2.replace("amp;", "");  
        window.open(videohtml2,"_self");
        ```
        
    - Reddit
        
        ```jsx
        Removeddit Bookmarklet (From Reddit Thread)
        javascript: {document.location = document.URL.replace("www.reddit.com/","www.removeddit.com/");}
        
        Reddit Full-Size Banner (From User Profile)
        javascript: var html = document.documentElement.innerHTML;    var subhtml = html.split('<div style="background-image:url(')[1];  var subhtml2 = subhtml.split('?width')[0]; alert("Banner: " + subhtml2);
        
        Reddit Full-Size Profile Photo (From User Profile)
        javascript: var html = document.documentElement.innerHTML;    var subhtml = html.split(`"Profile icon" src="`).pop().split(`" class=`).shift();  if(subhtml.includes("png")) {     subhtml = subhtml.split('.png')[0] + ".png";  } if(subhtml.includes("jpg")) {     subhtml = subhtml.split('.jpg')[0] + ".jpg";  } alert("Avatar: " + subhtml);
        ```
        
    - Pokemon Go
        
        ```jsx
        ##### General Websites Useful in Pokemon GO Investigations #####
        
        # Search by Location
        https://pogotrainer.club/
        https://gamepress.gg/pokemongo/trainer-codes-list
        
        # Mapping
        https://pokelytics.com/
        https://www.openstreetmap.org/
        
        # QR Codes
        https://webqr.com/index.html
        
        ##### Copy and paste the below bookmarklets into a new bookmark in your browser of choice to use the tools #####
        
        # Search for user by trainer code
        
        javascript:      
        var code = prompt("Paste Trainer Code here: ");         
        var google = "https://www.google.com/search?&q=" + '"' + code + '"';       
        var reddit = "https://www.reddit.com/r/PokemonGoFriends/search/?q=" + code +"&restrict_sr=1";   
        var twitter = "https://twitter.com/search?q=" + code;     
        
        GoogleFunction();       
        RedditFunction();  
        TwitterFunction();
        
        function GoogleFunction() {   setTimeout(function(){ window.open(google, "_blank"); }, 1000); }
        function RedditFunction() {   setTimeout(function(){ window.open(reddit, "_blank"); }, 1000); }   
        function TwitterFunction() {   setTimeout(function(){ window.open(twitter, "_blank"); }, 1000); }   
        
        # Search for user by username
        
        javascript:      
        var username = prompt("Enter username here: ");         
        var friendhunter = "https://api.friendhuntr.com/distribute/payload-search?username=" + username;        
        var silph = "https://sil.ph/" + username;        
        var pokebattler = "https://www.Pokebattler.com/profiles?search=" + username +  "&page=0#searchResult";   
        var trainerdex = "https://www.trainerdex.co.uk/u/" + username;     
        
        FriendHunterFunction();
        SilphFunction();
        TrainerDexFunction();
        PokeBattlerFunction();
        
        function FriendHunterFunction() {   setTimeout(function(){ window.open(friendhunter, "_blank"); }, 1000); }
        function PokeBattlerFunction() {   setTimeout(function(){ window.open(pokebattler, "_blank"); }, 1000);}
        function SilphFunction() {   setTimeout(function(){ window.open(silph, "_blank"); }, 1000);}
        function TrainerDexFunction() {   setTimeout(function(){ window.open(trainerdex, "_blank"); }, 1000);}
        ```

## Links to Useful Sites -- 

### Learning JavaScript -
[Learn JS (https://learn-js.org/)]
```embed
title: "Learn JavaScript - Free Interactive JavaScript Tutorial"
image: "https://www.learn-js.org/static/img/share-logos/learn-js.org.png"
description: "learn-js.org is a free interactive JavaScript tutorial for people who want to learn JavaScript, fast."
url: "https://learn-js.org/"
```

[Intro to Programming: Loops (thatandromeda.github.io)]
```embed
title: "Intro to Programming: Loops"
image: "https://thatandromeda.github.io/courseware/Intro-via-jQuery/img/screenshot-chrome.png"
description: "Yay programming!"
url: "https://thatandromeda.github.io/courseware/Intro-via-jQuery/intro.html"
```

### Tools - 
* [Make Bookmarklets](https://make-bookmarklets.com/) - Super useful for turning JS code into a bookmarklet


# 🔧 Bookmarklet Tools :

- **Bookmarklet Combining Tool!** —
    
    [Bookmarklet Combiner](https://w-shadow.com/bookmarklet-combiner/)
    

# 🌐 **Bookmarklet Sites** :

## 🔹🗄️**Collectios** :

- **CodePens** :
    
    https://codepen.io/bookmarklets/pen/NobJbq
    
    https://codepen.io/ArRolin/pen/BtDru
    
    https://codepen.io/osama-belal/pen/ydppQo
    

# 💡Tips :

❕**Use Sherlock's data(dot)json file** for account username URL queries when making bookmarklet or app to find accounts from usernames.

- File: —
    
    [](https://github.com/sherlock-project/sherlock/raw/master/sherlock/resources/data.json)
    
- Selected Accounts Page: —
    
    [SherlockAccounts](https://www.notion.so/SherlockAccounts-a5828929136c4b208938b4a8f6dfe7c9?pvs=21)

  ---
  
 - Find TONS of Bookmarklets -
! Go to Bookmarklet Combiner (https://w-shadow.com/bookmarklet-combiner/), you can find a ton of interesting bookmarklets by incrementing the URL. Start after '=6' and go past '=38000' or better yet, start high and then decrement. I'll add particularly interesting ones I find on my pinned Twitter thread. As for incrementing / decrementing, see below for both of those. [https://w-shadow.com/bookmarklet-combiner/?bookmarklet=6…](https://t.co/m9VkfHxYiJ)

    - Page Increment —
        
        ```jsx
        javascript:(function(){ var e,s; IB=1; function isDigit(c) { return ("0" <= c && c <= "9") } L = location.href; LL = L.length; for (e=LL-1; e>=0; --e) if (isDigit(L.charAt(e))) { for(s=e-1; s>=0; --s) if (!isDigit(L.charAt(s))) break; break; } ++s; if (e<0) return; oldNum = L.substring(s,e+1); newNum = "" + (parseInt(oldNum,10) + IB); while (newNum.length < oldNum.length) newNum = "0" + newNum; location.href = L.substring(0,s) + newNum + L.slice(e+1); })();
        ```
        
    - Page Decrement —
        
        ```jsx
        javascript:(function(){ var e,s; IB=-1; function isDigit(c) { return ("0" <= c && c <= "9") } L = location.href; LL = L.length; for (e=LL-1; e>=0; --e) if (isDigit(L.charAt(e))) { for(s=e-1; s>=0; --s) if (!isDigit(L.charAt(s))) break; break; } ++s; if (e<0) return; oldNum = L.substring(s,e+1); newNum = "" + (parseInt(oldNum,10) + IB); while (newNum.length < oldNum.length) newNum = "0" + newNum; location.href = L.substring(0,s) + newNum + L.slice(e+1); })();
        ```

---







