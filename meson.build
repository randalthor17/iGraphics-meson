project('igraphics', 'cpp')

# include igraphics dir
igraphics_inc = include_directories('include/iGraphics')
# include stb
stb_inc = include_directories('include/stb')

# include nanosvg
nanosvg_inc = include_directories('include/nanosvg')

# external deps
gl = dependency('gl', required: true)
glut = dependency('glut', required: true)
sdl2 = dependency('sdl2', required: true)
sdl2_mixer = dependency('sdl2_mixer', required: false)
freetype2 = dependency('freetype2', required: true)

# this is a header only dep
igraphics_dep = declare_dependency(
  include_directories: [igraphics_inc, stb_inc, nanosvg_inc],
  dependencies: [gl, glut, sdl2, sdl2_mixer, freetype2]
)

# add build_examples flag
if get_option('build_examples')
  subdir('examples')
endif
