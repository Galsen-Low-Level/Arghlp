
project('ahlp', 'c',
  version : '1.1.0',
  default_options : ['c_std=gnu99' ,'warning_level=3'])

cc = meson.get_compiler('c')

add_project_arguments( 
  cc.get_supported_arguments(
    '-Wformat',  
    '-Winline', 
    '-Wunused-result'
    ),  
  language:'c'
  )

inc_dir   =  include_directories('./')
arghlp_so = shared_library('arghlp', 'arghlp.c' , soversion: meson.project_version())
arghlp_dep= declare_dependency(link_with:arghlp_so ,include_directories:[inc_dir] ) 

executable(meson.project_name() ,
           'main.c',
           link_with:[arghlp_so],
           install : true)
