example_sources = []

# You manually glob .c files in examples/ folder
foreach file : run_command('find', '.', '-maxdepth', '1', '-name', '*.cpp', check: true).stdout().split('\n')
  if file != ''
    exe_name = file.split('/')[-1].split('.')[0]
    executable(exe_name, file, dependencies: igraphics_dep)
  endif
endforeach

