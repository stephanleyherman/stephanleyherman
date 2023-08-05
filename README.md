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
This is a Strategy&Time Management game where you solve competitive cyber security CTF questions within a given time limit. you control a character in a small map where you need to interact with key items to achieve your goal.
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
   I made a scriptable object that contain two types of questions at that point in time, a fill in the blank type question and multiple choice. I also structured it this way just incase we wanted to add another question type i can just extend the SO and make it have more variables to adjust it.
   
## 3. {P01} - Interactable Laptop
 
   <!-- Table here -->
<table>
  <tr>
    <td> <img src="(https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i5.png)"  alt="1" width = 360px height = 640px ></td>
    <td><img src="https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i5.png" alt="2" width = 360px height = 640px></td>
    
   </tr> 
  
</table>
   
   <!-- !Table here-->
   I wanted to make picking up the laptop feels nice, so i added a few keybinds to let you interact with it differently, as an example a closed laptop cannot be grabbed so you need to open/close it by pressing F, if you have a laptop on you then you can't pick up another one until you put it down by pressing G for picking up/putting down laptops, you cannot open into the question screen of the laptop if the laptop screen is closed. the idea was to use these keys so the player would be more engaged.
  sghsfghdsghd
  sghdsgfhdghs
  srthsfghsfgh

## 4. {P01} - End of the game Review Manager
 
   <!-- Endgame Screen -->
   Also using the singleton that i implemented whenever the game finishes either by the player running out of time or by finishing all the questions they selected, another scene would be put up as the endgame screen. Here they can put their names in the local leaderboard or choose to review the questions that they have missed or failed.
  <!-- Review Image-->
  adfhsfghdfghsg
  sfghdghdsghdg
  sghsfghfgh
  





  
</details>

 <p align = "right"> <a href="#hello--space_invaderrobot"> Back to Top </a></p>  

---           

# {P02} Enviroment Prototype
![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i1.png)
> The Main Menu       
                      
## General Outline            
Mynamejeff

<details>
<summary>More Details </summary>


  
</details>

 <p align = "right"> <a href="#hello--space_invaderrobot"> Back to Top </a></p>  
 
 ---                
 
# {P03} Pathfinding Prototype        
        
![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i1.png)
> The Main Menu       
                      
<details>
<summary>General Outline </summary>
      
              
  ![alt text](https://github.com/stephanleyherman/imagedumprepo/blob/main/p01-i1.png)



---
---
                                                                              
  
</details>

<details>
<summary>More Details </summary>


  
</details>

 <p align = "right"> <a href="#hello--space_invaderrobot"> Back to Top </a></p>  
 
---    
                    
# About Me
..

.
.
.
.

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
