# Abstract
&emsp;&emsp;This project is a VR virtual exhibition hall project based on Unity and Pico with the theme of "Man and God: Sacrifice and Divine Cognition in Sanxingdui Culture", aiming at letting the modern people understand the ancient people's review and thinking about the relationship between man and god by simulating the sacrificial scenes of Sanxingdui civilization in China. I was responsible for utilizing the characteristics of PICO4 equipment and Unity engine to realize a variety of interaction point technology and immersive experience. Through technical methods such as sound, gaze, keystrokes and area collision, we demonstrated a wealth of functional indicators, allowing users to freely explore ancient scenes, learn about the introduction of cultural artifacts, and view artifacts in a 360° rotation, etc., to provide a more realistic, immersive experience of traditional culture.
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
### 1.3.1 particle system
&emsp;&emsp;We used the particle system twice in this project, including the simulation of the sand storm effect in Scene one and the firefly effect in Scene two.The sandstorms is to better reflect the desolation of Scene one, and the fireflies are to make Scene two more ancient style.
<div align=center><img src="https://github.com/GainQh/VR_SanxingDui/blob/main/SandStorm.png"/></div>
<div align=center><img src="https://github.com/GainQh/VR_SanxingDui/blob/main/Firefly.png"/></div>

### 1.3.2 URP
&emsp;&emsp;In Scene 2, in order to simulate a more realistic water surface effect, we upgraded the rendering pipeline to URP rendering pipeline and used the visualization program node provided by Unity to create a beautiful and realistic water surface effect.
<div align=center><img src="https://github.com/GainQh/VR_SanxingDui/assets/150640834/8468db3d-c7c3-45d3-bfce-3655a10e0c62"/></div>

### 1.3.2 UI
&emsp;&emsp;We rendered the different hints UI in a canvas based on the camera as well as in world coordinates as needed, e.g., the main quest hints would be rendered on the camera, i.e., the VR headset, while the artifacts introductions in Scene 3 would be rendered in world coordinates.
<div align=center><img width="1000" height="600" src="https://github.com/GainQh/VR_SanxingDui/blob/main/UI1.png"/></div>
<p align="center">The image above shows the UI based on the VR headset</p>
<div align=center><img width="1000" height="600" src="https://github.com/GainQh/VR_SanxingDui/blob/main/UI2.png"/></div>
<p align="center">The image above shows the UI based on the game world</p>
