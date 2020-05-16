# Piltover

Developed with Unreal Engine 4.25.0

# Introduction

Playing Legends of Runterra, I fall in love with the background image where Jinx is standing in front of a very nice looking city.  
I didn't know what this city was and started searching the internet and found out that it was Piltover (& Zhaun).  
With this information, I found more and more pictures of this city and thought that there is something like a 3D environment for it, so that it can be used for the Wallpaper Engine, for example.  
It turns out: No 😔

To me:
I'm not very experienced in creating 3D environments and in my daily work I'm a frontend developer using Vue and TypeScript.  
So this journey may take a long time and may not lead to a final end result.  
I do it in my free time and for fun.

# TOC

- [History](#history)
- [Reference Image(s)](#reference-images)
- [Sessions](#sessions)
  - [1. Session](#1-session)
  - [2. Session](#2-session)

## History

| Session         | Date       | Duration | Summary                                                             | Commit                                                                                                                                                  |
| --------------- | ---------- | -------- | ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [1](#1-session) | 2020-05-10 | ~3h      | Initiate the project<br>Create greybox pivot building               | [166990a..6f14db4](https://github.com/Shinigami92/Piltover/compare/166990a9ef48d74ecc80f17830bc29d335e958df...6f14db48ca0ddcca163350f268a93ddc1ac1a425) |
| [2](#2-session) | 2020-05-11 | ~6h      | Find camera position<br>Add whitebox buildings in right bottom area | [6f14db4..97bdc83](https://github.com/Shinigami92/Piltover/compare/6f14db48ca0ddcca163350f268a93ddc1ac1a425...97bdc83280aa4afe107e70d4943684935d8e9c2e) |

## Reference Image(s)

![image](https://vignette.wikia.nocookie.net/leagueoflegends/images/8/8b/Piltover_Zaun_LoR_Background.jpg/revision/latest?cb=20191022172320)

Other references that I found:

- https://img.rankedboost.com/wp-content/uploads/2019/10/Piltover-Zaun-Cards-1.png
- https://i.ytimg.com/vi/ApmZu24gIkM/maxresdefault.jpg
- https://cdnb.artstation.com/p/assets/images/images/017/227/147/large/patrick-faulwetter-pfaulwetter-piltover-01-as.jpg?1555117676
- https://vignette.wikia.nocookie.net/leagueoflegends/images/2/2b/Piltover_Zaun_Connected_Cities.jpg/revision/latest/scale-to-width-down/340?cb=20170112210626
- https://universe-meeps.leagueoflegends.com/v1/assets/images/factions/image-gallery/zaun-collecttechmaturgy.jpg
- https://i.ytimg.com/vi/yM8o77bAzUw/maxresdefault.jpg
- https://revelationvr0.files.wordpress.com/2020/04/6796a-1.png
- https://am-a.akamaihd.net/image?f=https%3A%2F%2Funiverse-meeps.leagueoflegends.com%2Fv1%2Fassets%2Fimages%2Fpiltover_environment_01.jpg&resize=:1200
- [VISIONS OF PILTOVER](https://universe.leagueoflegends.com/en_US/region/piltover/?mv=image-gallery)

## Sessions

### 1. Session

I created a basic pivot building to orient myself and get a feel of scaling.  
So I picked the building down there next to the fountain.

I created a simple tower, a box building and a roof. Some windows and lights added.  
I also made a hole in the ground to simulate Zhaun. (I may never add Zhaun fully to this project 🤣)

<img src="https://user-images.githubusercontent.com/7195563/81501323-14eeb180-92d8-11ea-931c-b38fa0989c4b.png" alt="Pivot Buidling" width="600" />

### 2. Session

To create other buildings around my pivot building, I added a camera to take the position of the view of the reference image.  
It turned out to be very difficult and I had to learn a few things about perspective. I found that a 60° field of view works well.  
I took the reference image and my camera view and tapped between the image and the engine to match the view. I went crazy and used some post-its to get some anchor points.  
Because of the light coming from behind in this scene, I added two lights and a shiny golden material to improve the process.

<img src="https://user-images.githubusercontent.com/7195563/82113027-f151be00-9752-11ea-8a6b-134ff43e6ca7.jpg" alt="Post-Its Reference Image" width="400" /> <img src="https://user-images.githubusercontent.com/7195563/82113029-f31b8180-9752-11ea-8f19-465107dcd098.jpg" alt="Post-Its Engine" width="400" />

After finding a good camera angle and position, I started adding the front right buildings and expanded Zhaun's abyss.  
I also used post-its for them, building by building, working my way to the rear right building.

Then I rebuilt the pivot building based on my measurements with improved scaling.

I started baking lights and it already took about 5-10 minutes to bake 😮  
I was confused why the light on the ground floor of the tower no longer casts shadows 🤔

Then I made a real stupid mistake 😣 I forgot that I controlled the reference camera and looked at the result with normal engine controls.  
So I lost the angle and position of the view for the reference image... `CTRL + Z` was too late.  
So I had to find the position again, but because of the progress in real time, I just found a rather poor similar position. So I have to fix this next session.  
To avoid this mistake again, I created a backup camera at the exact position of the reference camera with `CTRL + C` `CTRL + V`.

Final result of this session:

<img src="https://user-images.githubusercontent.com/7195563/81608511-b78d5a00-93d6-11ea-9689-50c26768480c.png" alt="Result Session 2" width="600" />
