# MPGLGrid
Visualization of MPGrid results using OpenGL

# Install

```
> pip install MPGLGrid
```

# References
## draw()
+ CLASS METHODS
  + cmp_range(grid, cmp) : set colormap range
  + draw(grid, cmp) : draw grid data
  + draw_axis(grid) : draw axis
  + get_disp(type) : get display flag
  + list() : set render list
  + region(grid) : return draw region
  + set_disp(type, disp) : set display flag, disp = {0:non-display | 1:display}
+ CLASS DATA
  + kind = {0:type | 1:update | 2:value} : draw kind
  + method = {0:quads | 1:cubes} : draw method
  + range = (x0, y0, z0, x1, y1, z1) : draw range

## colormap()
+ CLASS METHODS
  + color() : set default color
  + draw() : draw colormap
  + grad_color(value) : get grad color
  + grayscale() : set default grayscale
  + set_grad_color(id, red, green, blue) : set grad color
  + set_label(id, label) : set label
  + set_step_color(id, red, green, blue) : set step color
  + step_color(id) : get step color
+ CLASS DATA
  + font_color = (red, green, blue) : font color
  + font_type = {0:10pt | 1:12pt | 2:18pt} : font type
  + mode = {0:step | 1:gradation} : colormap mode
  + ngrad = num : number of gradiation color
  + nscale = num : number of scale
  + nstep = num : number of step color
  + range = (min, max) : colormap range
  + size = (width, height) : colormap size
  + title = txt : colormap title

## model()
+ CLASS METHODS
  + button(x, y, down) : process when mouse button pressed
  + fit() : fit scale
  + get_angle() : get angle
  + get_dir() : get direction
  + inverse() : set inverse matrix
  + motion(scene, x, y, ctrl) : process when mouse moved, return true if model modified
  + reset() : reset model matrix
  + rot_x(angle) : rotate around X axis
  + rot_y(angle) : rotate around Y axis
  + rot_z(angle) : rotate around Z axis
  + set_angle(alpha, beta, gamma) : set angle
  + set_dir(x0, x1, x2, [z0, z1, z2]) : set direction
  + trans_x(dist) : translate to X direction
  + trans_y(dist) : translate to Y direction
  + trans_z(dist) : translate to Z direction
  + transform() : OpenGL transformation
  + zoom(scale) : zoom
+ CLASS DATA  
  + button_down : true while button pressed
  + button_mode = {0:Rotate | 1:Translate | 2:Zoom} : mode while button motion
  + button_x : position x where button pressed
  + button_y : position y where button pressed
  + center = (cx, cy, cz) : center of rotation
  + mat = ((m00, m01, m02, m03), (...), (...), (...)) : transformation matrix
  + mat_inv = ((i00, i01, i02, i03), (...), (...), (...)) : inversed transformation matrix
  + scale = scale : scale

## scene()
+ CLASS METHODS
  + front_text(x, y, string, font_type) : draw front text
  + light_add(x, y, z, w) : add light
  + light_ambient(id, red, green, blue, alpha) : set light ambient
  + light_diffuse(id, red, green, blue, alpha) : set light diffuse
  + light_position(id, x, y, z, w) : set light position
  + light_specular(id, red, green, blue, alpha) : set light specular
  + resize(width, height) : resize window
  + setup() : setup scene
+ CLASS DATA
  + clear_color = (red, green, blue, alpha) : clear color
  + height : screen height
  + mat_emission = (red, green, blue, alpha) : material emission
  + mat_shininess = shininess : material shininess
  + mat_specular = (red, green, blue, alpha) : material specular
  + proj = {0:frustum 1:ortho} : projection mode
  + width : screen width
  + zfar = z : zfar of viewing volume
  + znear = z : znear of viewing volume
