# Instagram unfollower checker.


### Steps:
 1. Go to the profile you want to check. (Must be public or following them if its private.)
 2. Copy the code: ```document.getElementsByClassName("-nal3 ")[2].click();let followed=parseInt(document.getElementsByClassName("g47SY")[2].innerHTML);let followedList=document.getElementsByClassName("FPmhX notranslate  _0imsa ");let followedListClone;let followers;let followersList;let followersListClone;let scroll=setInterval(updateScroll,200);let stopCheck=setInterval(function(){stopTask(1)},200);function stopTask(a){if(a===1){if(followed<=followedList.length){clearInterval(scroll);followedList=document.getElementsByClassName("FPmhX notranslate  _0imsa ");followedListClone=[...followedList];sleep(200);followersF()}}else if(a===2){if(followers<=parseInt(followersList.length)){followersList=document.getElementsByClassName("FPmhX notranslate  _0imsa ");followersListClone=[...followersList];clearInterval(scroll);document.getElementsByClassName("wpO6b ")[1].click();users();clearInterval(stopCheck)}}}function followersF(){clearInterval(stopCheck);document.getElementsByClassName("-nal3 ")[1].click();followers=parseInt(document.getElementsByClassName("g47SY")[1].innerHTML);followersList=document.getElementsByClassName("FPmhX notranslate  _0imsa ");scroll=setInterval(updateScroll,200);stopCheck=setInterval(function(){stopTask(2)},200)}function users(){let usernames=followersListClone.map(function(x){return x.title});for(let i=0;i<followedListClone.length;i++){if(!usernames.includes(followedListClone[i].title)){console.log(followedListClone[i].title)}}}function updateScroll(){let element=document.getElementsByClassName("isgrP")[0];element.scrollTop=element.scrollHeight;numeroACC=element.scrollTop}function sleep(a){let start=new Date().getTime();for(let i=0;i<1e7;i++){if((new Date().getTime()-start)>a){break}}}```
 3. Go to the profile tab and open the developer console or Ctrl+Shift+J and paste the code.
 4. It will start scrolling your followers until reach the end, then It'll print it on the console.
 ![Output after finishing](https://github.com/davidarroyo1234/InstagramUnfollowers/blob/master/Readme/Pixelated%20result.png?raw=true)
 

***The more users you have to check, more time it will take***

To-Do
 - [x] Showing unfollowers in the console.
 - [ ] Option to automatically unfollow them.
