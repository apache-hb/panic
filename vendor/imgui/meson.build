src = [
    'imgui.cpp',
    'imgui_demo.cpp',
    'imgui_draw.cpp',
    'imgui_widgets.cpp',
    'imgui_tables.cpp',

    'backends/imgui_impl_win32.cpp',
    'backends/imgui_impl_dx12.cpp',

    'misc/cpp/imgui_stdlib.cpp',
]

inc = include_directories('.', 'misc/cpp', 'backends')

deps = [ cpp.find_library('d3d12'), cpp.find_library('dxgi') ]

libimgui = static_library('imgui', src,
    include_directories : inc,
    dependencies : deps
)

imgui = declare_dependency(
    link_with : libimgui,
    include_directories : inc,
    dependencies : deps
)
