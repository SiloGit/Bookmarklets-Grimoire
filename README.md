# :bookmark: :notebook_with_decorative_cover: Bookmarklets-Grimoire :notebook_with_decorative_cover: :notebook:

This is a hub for all things Bookmarklet related. Many are #OSINT related, but there should be something here for everyone. From lists of awesome bookmarklets themselves, places to find other bookmarklets, ways to find plenty more, to tutorials on how to quickly create your own, hopefully you'll find this place useful. I've noticed that bookmarklets don't get nearly the credit and praise as they should. It's an old technology, but because of how awesome they are, I would expect to find tons of collection lists, or collections of info like this one, but I haven't. That's what motivated me to start this. Anyways, thank you! Please bookmark, star, contribute, etc, and please return regularly for new and updated content! 

Things to Note:
    
1 - Please excuse the mess!! The way my dumb ass likes to work is by taking all the ingrediants, tossing them onto the nearest wall, and then making sense of everything afterwords. While I won't insult you by doing that entirely, now and then things won't be in the correct order, etc. I will fix these issues ASAP. This is a work in progress, never complete. 
    
2 - I try my best to credit everyone for their work, but sometimes sources were saved back when I didn't expect to collect them into something public. If you see any of your work here, please contact me and I will immediately credit you, or remove it if you wish. That said, I'll try to do that as little as possible.



![image](https://github.com/user-attachments/assets/ba7ed1d2-d7b7-45c8-a2a0-52d8622ea9a6)


---


# 📜 - **Table of Contents** :

  ## 🧩 BOOKMARKLETS —

> *Just mouse over the code and click the Copy button on the top right. Make a new bookmark, name it and then paste the code in the URL to create the bookmarklet.*

---
    
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
        
- OSINT —
    
    
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







