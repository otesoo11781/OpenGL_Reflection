# OpenGL_Reflection
Implement effects that are similar to windows, inlcuding Multiple-pass Reflection and Depth of Field with OpenGL.

Use stencil buffer to render Reflection scene in mirror's area.

Use accumulation buffer to accumulate effects of reflection and refraction.

Use back-face/front-face culling: glEnable(GL_CULL_FACE).

### UI control:
Keyboard : Move the camera and adjust parameters.

'w' : zoom in

'a' : move left (circle the center)

's' : zoom out

'd' : move right (circle the center)

Aperture is range 0.1 to 0.2.
