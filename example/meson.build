# This is just a build illustration  

project('elfc', 'c',
  version : '0.1',
  default_options : ['c_std=gnu99' ,'warning_level=3'])


cc = meson.get_compiler('c') 

arghlp_lib = shared_library('arghlp', '../arghlp.c',)
arghlp_dep = declare_dependency(link_with: arghlp_lib, include_directories:'../')


executable(meson.project_name(),
           'main.c',
           'elfcheck.c',
           dependencies:[arghlp_dep],
           install : true)
