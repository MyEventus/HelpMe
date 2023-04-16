---  
last_update: 2023Apr16  
share: true    
---  
  
Related [Docker_Cheatsheet](./Docker_Cheatsheet.md)  
  
Note:  
A docker container is different to a docket image.  
This is intended to be simple not 100% technically accurate for novices.  
  
## Analogue:  
- A docker "image" is static (like a CD ROM).  
	- Built in layers.  
	- Can contain both (small Operating system such as Linux e.g. alpine) AND applications frozen in time (static).  
- A container is build from an image.  
	- Contains you dynamic code on top of image.  
	- Only need to re-build or re-create of new packages upgrade required.  
  
- You dockerfile (recipe for container build) and docker-compose (recipe for multiple related containers) file PLUS your personal data / code / app ( linked via " volumes") is separate.  
  
- As your code / apps are kept on you local computer (separate from image and build container) both the image and container are disposable.  
	- As long as you keep..   
		- A: Docker file (and or Docker-compose file) plus..  
		- B: Your own code / app.  
  
- i.e.  Cake analogy:  
	- You can throw away the ingrediency and equipment or tools (container and as long as you keep the recipe you can always re-create (or rebuild new container based off your or someone else's image).  
