# Hello ! :space_invader::robot:
---
#### I'm a Game Programmer with experience in Unity and Unreal.
#### I have a Bachelor in Computer Science, i studied programming and cyber security during my time in the University.
---
I'm using this page to act as a portfolio of mine on game prototypes that i have made, to make this portfolio clear and concise i would only include some prototypes that i think is worth mentioning and explained. At the end of the page i would put in more statistics and background on how i got here and how game design became my passion.               
Each of the section will also have a General Outline part and the More Details part where i explain more on the game engine side of things and how i made certain things in the prototype.

Feel free to jump to any of the section i've made :   
>- [P01 - CTFDash](#p01-ctfdash)
>- [P02 - Enviroment Prototype](#p02-enviroment-prototype)
>- [P03 - Pathfinding Prototype](#p03-pathfinding-prototype)  
>- [About Me](#about-me)

> [!NOTE]
> The downloadable version of my prototypes is available below !

---                 

# {P01} CTFDash
![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i1.png)
> The Main Menu       
                      
## General Outline               
This is a Strategy&Time Management game where you solve competitive cyber security CTF questions within a given time limit. you control a character in a small map where you need to interact with key items to achieve your goal. Mainly finishing a laptop's question then submitting it to the submission post for points, every laptop that you failed with lose you hearts and if it reaches zero the game is over.
<br>        
               
<!-- Diner Dash Image Here -->
![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i2.png)             
The game that i made took heavy inspiration from DinerDash where instead of using Food and Tables as a main mechanics i use Laptops and Tables.
               
<br>        
               
<!-- Show table, laptop and the conveyor belt-->
![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i3.png)
The conveyor belt will spawn Laptop which you need to put in the "Tables" to be able to operate and see the questions inside, for the purpose of this game i only made 4 categories(Cryptography, WebEx, OSINT, General Knowledge) but i also have put in the function to make custom questions and custom categories as well via a json savefile script.
               
<br>          
           
<!-- Select amount of questions -->
![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i4.png)
The idea is that this game would be used as a gamification concept that connect the more common game mechanics with answering difficult CTF competition questions where they would choose the amount of questions that they're comfortable with and slowly go up doing more and more questions, in a limited amount of time. I also added a Review stage option after the timer runs out, it just contains the Laptops that was wrong or was discarded by the player.
               
<br>         
           
<!-- Tutorial -->
![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i5.png)
I made this game as a part of my thesis, it required me to have people test the game as a part of the user satisfaction section, so i made a tutorial to help them understand how to play the game it is also made with Bahasa language instead of English since most people that test it don't speak english proficiently.
                
## More Details             
<details>
<summary>Click to see more :</summary>
                           
## 1. {P01} - The Foundation of the project
   
   <!-- -->
   I use a Singleton to manage the input and output of questions, the question itself is saved in a scriptable object that you can manually add in the json file or you can add it in game in the Customize page. I also made several other items to make the game more interesting such as different keys that you can use to interact with the laptop like opening, closing and grabbing the laptop. Almost everything is put inside a single Player Script, looking back this is bad practice from my part since Player.cs became so bloated it has about 2000+ lines of code for no reason at all, i've stop doing this in future projects and instead opted out to make separate script files for most things to reduce unnecessary coupling.
   
   
## 2. {P01} - Scriptable Object and Savefile System
   
   <!-- SO picture here -->
   ![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i6.png)           
   I made a scriptable object that contain two types of questions at that point in time, a fill in the blank type question and multiple choice. I also structured it this way just incase we wanted to add another question type i can just extend the SO and make it have more variables to adjust it.
   
## 3. {P01} - Interactable Laptop
 
<table>
  <tr>
    <td><img src="https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i7.png"  alt="1" width = 360px height = 240px ></td>
    <td><img src="https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i8.png" alt="2" width = 360px height = 240px></td>
    <td><img src="https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i9.png" alt="2" width = 360px height = 240px></td>
   </tr> 
  
</table>
   
   <!-- !Table here-->
   I wanted to make picking up the laptop feels nice, so i added a few keybinds to let you interact with it differently i achieve this by using conditionals, as an example a closed laptop cannot be grabbed so you need to open/close it by pressing F, if you have a laptop on you then you can't pick up another one until you put it down by pressing G for picking up/putting down laptops, you cannot open into the question screen of the laptop if the laptop screen is closed. the idea was to use these keys so the player would be more engaged.
                  
   The act of grabbing a laptop is also just an illusion, i wanted to save memory by having less GameObject/Actor when the game is running so i Destroy() the laptop that was being picked up, save it's information in the Player and then Instantiate() a new one when im interacting with a table.

## 4. {P01} - End of the game Review Manager
 
   <!-- Endgame Screen -->
   ![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i10.png)              
   Also using the singleton that i implemented, whenever the game finishes either by the player running out of time or by finishing all the questions they selected, another scene would be put up as the endgame screen. Here they can put their names in the local leaderboard or choose to review the questions that they have missed or failed.
  <!-- Review Image-->
  ![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i11.png)             
  This map is generated by a loop, the topside and the bottomside is generated independently while the length of the body is adjusted accordingly to the amount of questions that was missed/failed. Since this is just for review they can't pick up the laptop nor submit anything it's purely used just to study.





  
</details>

 <p align = "right"> <a href="#hello--space_invaderrobot"> Back to Top </a></p>  

---           

# {P02} Enviroment Prototype
![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p02-i1.png)          
     
                      
## General Outline            
So the whole idea that i had for this one was a apocalyptic scenario where years has passed and people is forced to live underground. The assets that i used was bought i didn't make them myself but i did stitch the whole thing and made the lighting from scratch.

![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p02-i2.png)      
I wanted to test out my level design skill by making a map, where the player would tranverse an abandoned section of the underground, i put things where i thought it would make sense and tell a story of what went down and put the appropriate zombie with the right outfit there.

![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p02-i3.png)      
I also added some functionality to the project, i added movements, guns, and zombie AIs because maybe someday i wanna return to this and develop it some more because this is one of the most fun project i had made.

![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p02-i4.png)      

## More Details             
<details>
<summary>Click to see more :</summary>
                           
## 1. {P02} - The Foundation of the project
   <!--  -->        
   Originally i wanted to make a shooter game that has an Object Pooling implementation, but then the project got sidetracked because i had new ideas and new things that i wanna do so i decided to push the original idea to future projects while i make this lean into more of a exploratory type game that is more dark and gloomy.

## 2. {P02} - Zombie AIs
   
   <!-- Zombie Stuff picture here -->
   ![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p02-i5.png)           
   I thought to myself at that time the project needed obstacles, so i made Zombie AIs with adjustable variables that i can tweak in the Editor, the zombies have different idle animations and different skins as well.           
   ![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p02-i6.png)        
   Learning from previous projects i made sure that this one has emphasis on the readibility in the Editor, i made sure that everything was packaged neatly and understandable just from a glance.         

## 3. {P02} - Map Design and NavMesh
   
   <!-- Zombie Stuff picture here -->
   ![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p02-i7.png)           
   The zombies need to be able to chase me so i added a simple NavMesh, put in some tweaks into the enviroment like making sure they don't walk on the rubbles or suddenly spring up into a sofa or a tent. 

## 4. {P02} - A rifle and a handgun because why not
   
   <!-- Zombie Stuff picture here -->
   ![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p02-i8.png)           
   I also needed a way to defend myself, the gun implementation for this project was one of the first thing that i made, i only made two guns but i did put in the architecture to make adding more guns easier. They also have adjustable variables to make tweaking the guns in the editor easier.


<!-- !!ENVIROMENT PROTOTYPE MORE DETAILS SECTION HERE -->
  
</details>

 <p align = "right"> <a href="#hello--space_invaderrobot"> Back to Top </a></p>  
 
 ---                
 
# {P03} Pathfinding Prototype        
            
![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p03-i1.png)            
                
## General Outline            

  So for this project i will just explain everything in general outline since it's not as long as the others.              
  This project is small, it's just to show the concept of pathfinding in a tower defense game.      
  For this one i followed a tutorial, the idea wasn't mine but this is one of the project that took me the longest and teaches me alot so i thought it's worth mentioning.

  ![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p03-i2.png)    

  There's two castle, the one below is yours while the one on the right is the enemy's castle, you can put turret anywhere on the coordinates that is colored yellow, the one that is grey/white is unplaceable and is unwalkable as well. You can turn off/on debug mode by pressing C to show the coordinates and it's respective color, when you're playing normally the coordinates is not suppose to be shown this is just to help see the pathfinding algorithm at works. the trees on the edges is put there to signify where you can and cannot put turrets.

  ![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p03-i3.png)   

  This project used the Breadth-first search algorithm to define a path for the enemy minions to walk on, it changes dynamically so if i put a turret in their way the minions would adjust their movement accordingly/smoothly as well. It also has an edge case on dealing with what if there's no path ? and the minions cannot reach our turret, the edge case is a try-catch esque conditional that will check the clicked tile to see if there will still be a path or no and return a boolean that will determine the action taken.



 <p align = "right"> <a href="#hello--space_invaderrobot"> Back to Top </a></p>  
 
---    
                    
# About Me                  
I have several other Unity and Unreal projects that i have worked on this Year, these are just the noteable few that i think is enough to show my understanding and my skillset. I've only recently picked up Unreal and been having a blast with the extraordinarily in-depth and powerful system that Unreal has, I currently making something of my own in Unreal as well and this Portofolio will definitely be updated in due time in accordance to my progress.

My Contacts : 
- stephanleyherman99@gmail.com          
- https://www.linkedin.com/in/stephanley-herman/               



> [!IMPORTANT]
> Thank you for taking the time out of your day to read my Portofolio ! 
 <p align = "right"> <a href="#hello--space_invaderrobot"> Back to Top </a></p>  





<!--
**stephanleyherman/stephanleyherman** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
