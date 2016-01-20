# Lesson 6 Create a webvr scene and edit it 

## ssh into your edison board
1. Go to https://developer.weaved.com/portal/members/home.php
It will provide a ssh login similar to
ssh -l LOGIN proxya.yoics.net -p 34141
2. Bring up a terminal window and type in the command above substituting LOGIN with your name
   * example `ssh -l freddie proxya.yoics.net -p 34141`

## Clone a git repo into your directory
1. Create a subdirectory called lesson6
2. Change directory to go into the lesson6 directory
   * `cd lesson5`
3. Clone a webvr repo using git
   * `git clone https://github.com/borismus/webvr-boilerplate.git`
4. Change to this directory
   * `cd webvr-boilerplate`
5. Run a web server that can show the contents of this directory on port 1880
   * `http-server -p 1880`
6. Go to this site via weaved using google cardboard in safari
   * Go to https://developer.weaved.com/portal/members/home.php and select the edison*_http link


## Change the background of the webvr scene
1. cd to the img directory under webvr-boilerplate
   * `cd img`
2. copy an image of mars to this directory
   * `curl -o mars.jpg https://cdn-images-1.medium.com/max/800/1*fdbs8NqKPF-R8b9zFJegHw.jpeg`
3. change to the parent directory
   * `cd ..`
3. edit index.html to use this image
   * `vi index.html`
4. after setSize remove the loadTexture function and add the following lines
   * `var geometry = new THREE.SphereGeometry(50, 200, 200);`
   * `var material = new THREE.MeshBasicMaterial();`
   * `material.map = THREE.ImageUtils.loadTexture('img/mars.jpg');`
   * `material.side = THREE.BackSide;`
   * `var skybox = new THREE.Mesh(geometry, material);`
   * `scene.add(skybox);`
5. save the file
   * `:wq`	
6. reload the page in google cardboard

## Change the cube to earth
1. copy an image of earth to this directory
   * `cp /home/root/earth.jpg img`
2. edit index.html to use this image of earth
   * `vi index.html`
4. change the following lines
   * `var geometry = new THREE.BoxGeometry(0.5, 0.5, 0.5);`
   * `var material = new THREE.MeshNormalMaterial();`
   * `var cube = new THREE.Mesh(geometry, material);`
   * `cube.position.z = -1;`
   * to 
   * `var geometry = new THREE.SphereGeometry(0.5, 32, 32);`
   * `var material = new THREE.MeshBasicMaterial();`
   * `var earthMesh = new THREE.Mesh(geometry, material);`
   * `earthMesh.position.z = 1;`
   * `earthMesh.position.x = 15;`
   * `earthMesh.position.y = 7.25;`
5. in the animate function change
   * `  cube.rotation.y += 0.01;`
   * to 
   * `  earthMesh.rotation.y += 0.01;`
6. save the file
   * `:wq`	
7. reload the page in google cardboard

 


