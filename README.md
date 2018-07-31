# OpenGL_Reflection
### Description
Implement effects that are similar to windows, inlcuding Multiple-pass Reflection and Depth of Field with OpenGL.

### Requirement
Use stencil buffer to render Reflection scene in mirror's area.

Use accumulation buffer to accumulate effects of reflection and refraction.

Use back-face/front-face culling: glEnable(GL_CULL_FACE).

UI control:

Keyboard : Move the camera and adjust parameters.
    
    'w' : zoom in
 
    'a' : move left (circle the center)
 
    's' : zoom out
 
    'd' : move right (circle the center)

Aperture is range 0.1 to 0.2.

### Implement Steps:

#### Step 1: Set stencil buffer

Set mirror's area with stencil buffer.

#### Step 2: Reflection

Filp your scene along the mirror to form a reflected scene or camera.
Draw scene to render the effect of reflection.

PS: Front mirror's center position is (-20, 20, 0) and is parallel to yz-plane.

PS: Back mirror's center position is (20, 20, 0) and is parallel to yz-plane.

#### Step 3: Depth of Field

Use about N ( N >= 8 ) passes, moving the eyes' positions to different direction at every pass to create the effect of blurring. 

( the distance of the jittering should be about 0.2~0.3 )

 Saving the result of each pass into accumulation buffer, and output the result back to the color buffer when you're done.

 PS: Defined Keyboard to change (vatx,vaty,vatz)

Switch to focus on the different target

    Press button '1'  : Look at target(-10,12,0)

    Press button '2'  : Look at target(-50,12,0)

    Press button '3' : Look at target(-400,12,0)
