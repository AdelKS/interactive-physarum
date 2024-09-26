project('interactive-physarum', 'cpp',
version : '0.0.1',
default_options : [
  'cpp_std=c++20',
  'buildtype=release',
  'optimization=3',
  'default_library=shared',
  # 'prefer_static=true',
  'b_ndebug=if-release',
  'c_args=-pipe',
  'cpp_args=-pipe',
  # 'warning_level=3'
]
)

inc = include_directories(
  'src'
)

sources = files(
  'src/main.cpp',
  'src/ofApp.cpp',
)

deps = [
  dependency('ofxGamepad'),
]

fs = import('fs')
subdir('data')

exe = executable('interactive-physarum',
  sources,
  include_directories: inc,
  dependencies: deps,
  install: true)

test('run program', exe, workdir: meson.current_source_dir())
