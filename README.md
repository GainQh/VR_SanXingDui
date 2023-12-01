# Abstract
&emsp;&emsp;This project is a VR virtual exhibition hall project based on Unity and Pico with the theme of "Man and God: Sacrifice and Divine Cognition in Sanxingdui Culture", aiming at letting the modern people understand the ancient people's review and thinking about the relationship between man and god by simulating the sacrificial scenes of Sanxingdui civilization in China. I was responsible for utilizing the characteristics of PICO4 equipment and Unity engine to realize a variety of interaction point technology and immersive experience. Through technical methods such as sound, gaze, keystrokes and area collision, we demonstrated a wealth of functional indicators, allowing users to freely explore ancient scenes, learn about the introduction of cultural artifacts, and view artifacts in a 360° rotation, etc., to provide a more realistic, immersive experience of traditional culture.(Demo Video:https://youtu.be/Dkqfabv9YPg)  
![image](https://github.com/GainQh/VR_SanxingDui/blob/main/Abstruact.png?raw=true)
# 1. Project Introduction
## 1.1 Cultural Background
&emsp;&emsp;"God" is in fact the ancient human interpretation of all things in the world, a way of human understanding of the world, a process. The power of ancient man to conquer nature was very limited. People used their imagination to conquer nature. They put their trust in God and all the gods for the woes and misfortunes of the world. Worship of these gods, mainly through rituals for sacrifice and prayer, Sanxingdui artifacts are mainly used for sacrifice; human face artifacts transformed from the human face, into the imagination of the gods deformed
## 1.2 Research on Sanxingdui Museum
&emsp;&emsp;Located in the northeast corner of the national key cultural relics protection unit of Sanxingdui Ruins, Sanxingdui Museum is a large modernized thematic site museum in China.The results of the survey are as follows：
- The official website is more beautiful, with better web interaction design;
- There is an intention to develop a smart digital museum with the help of digital media technology;
- Has a virtual showroom but is more traditional: features only panoramic display, mouse interaction;
- There are 3D artifact displays that are highly informative for modeling;
## 1.3 Technical Background Research
&emsp;&emsp;Immersive interaction design can generate multimodal interaction situations directly from behavioral interactions, giving viewers the ability to interact with the content, have fun, and bring the content to life to participate in virtual scenarios.
![image](https://github.com/GainQh/VR_SanxingDui/blob/main/Technical.png?raw=true)
# 2. Technological Route
## 1.1 3D Modeling
&emsp;&emsp;We strictly follow industry modeling standards, from sculpting to baking to painting materials, following a workflow from blender to Zbrush to SP.
![image](https://github.com/GainQh/VR_SanxingDui/blob/main/Modeling.png?raw=true)
## 1.2 Style Design
&emsp;&emsp;
## 1.3 Functional realization
### 1.3.1 Interaction & Scene Jumping
&emsp;&emsp;We deal with three main scenarios in which the jumping order is: a sacrificial scene in the desert (modern) to an ancient sacrificial scene to a modern museum, which we call Scene one, Scene two, and Scene three in that order. The main scene jumps are based on the player's interactions, including the player's gaze interaction, joystick button interaction, etc.At the same time, the player can also move based on the joystick and explore the scene freely.  
&emsp;&emsp;Scene 1 to Scene 2: Players will take on the role of an expedition member separated from his teammates in Scene One.Then player need to follow the prompt UI to explore. When the player reaches the altar as requested, range detection and gaze interaction will be performed. The gaze interaction is a function that comes with PICO Unity Integration SDK. At this time, the prompt sound effect and light effect will be triggered, and then jump to scene two.  
<div align=center><img src="https://github.com/GainQh/VR_SanxingDui/blob/main/Scene1.png"/></div>

&emsp;&emsp;Scene two is the terrain after our restoration of the Samsungdui site. Upon entering Scene two, players will visit the scenery along the banks of the ancient canal. When arriving at the prompted area. Players can visit the residential area or sacrificial area, need to use the pico handle ray click UI to choose.This leads to different endings   
<div align=center><img src="https://github.com/GainQh/VR_SanxingDui/blob/main/Scene2_1.png"/></div>
<div align=center><img src="https://github.com/GainQh/VR_SanxingDui/blob/main/Scene2_2.png"/></div>
<div align=center><img src="https://github.com/GainQh/VR_SanxingDui/blob/main/Scene2_3.png"/></div>

&emsp;&emsp;Scene two to Scene three: in the sacrificial area, players need to decipher. After the player picks up the ivory through the handle's ray and puts it into the high priest's hand. Trigger a jump from Scene two to Scene three.  
&emsp;&emsp;Scene three is a modern museum in which the panels and artifacts that are the theme of our project are displayed. When the player approaches the artifact, the player is recognized by range detection as well. The artifact introduction UI is displayed as well as the introduction audio is played, and the artifact is rotated 360 degrees for display.
<div align=center><img src="https://github.com/GainQh/VR_SanxingDui/blob/main/Scene3.png"/></div>

### 1.3.2 particle system
&emsp;&emsp;We used the particle system twice in this project, including the simulation of the sand storm effect in Scene one and the firefly effect in Scene two.The sandstorms is to better reflect the desolation of Scene one, and the fireflies are to make Scene two more ancient style.
<div align=center><img width="500" height="400" src="https://github.com/GainQh/VR_SanxingDui/blob/main/SandStorm.png"/></div>
<div align=center><img width="500" height="400"src="https://github.com/GainQh/VR_SanxingDui/blob/main/Firefly.png"/></div>

### 1.3.3 URP
&emsp;&emsp;In Scene 2, in order to simulate a more realistic water surface effect, we upgraded the rendering pipeline to URP rendering pipeline and used the visualization program node provided by Unity to create a beautiful and realistic water surface effect.
<div align=center><img src="https://github.com/GainQh/VR_SanxingDui/assets/150640834/8468db3d-c7c3-45d3-bfce-3655a10e0c62"/></div>

### 1.3.4 UI
&emsp;&emsp;We designed the UI based on the theme colors.Then we rendered the different hints UI in a canvas based on the camera as well as in world coordinates as needed, e.g., the main quest hints would be rendered on the camera, i.e., the VR headset, while the artifacts introductions in Scene 3 would be rendered in world coordinates.
<div align=center><img width="1000" height="500" src="https://github.com/GainQh/VR_SanxingDui/blob/main/UI1.png"/></div>
<p align="center">The image above shows the UI based on the VR headset</p>
<div align=center><img width="1000" height="500" src="https://github.com/GainQh/VR_SanxingDui/blob/main/UI2.png"/></div>
<p align="center">The image above shows the UI based on the game world</p>

### 1.3.5 Map Guide
&emsp;&emsp;We simulated the map effect by placing an overhead camera above the character, so the player could observe their position in real time. Because of the large size of Scene two, we place this feature in Scene two to help players better explore the map
<div align=center><img width="300" height="200" src="https://github.com/GainQh/VR_SanxingDui/blob/main/map.png"/></div>

### 1.3.6 Cruise Ship Simulation
&emsp;&emsp;We made simple rafts for use in Scenario Two. Since Scene 2 is mainly action on a river, we modeled the navigation of a cruise ship. This included a simulation of the bumpy effects  

