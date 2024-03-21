project('parthenon', 'cpp',
    default_options : [
        'cpp_std=vc++latest'
    ]
)

cpp = meson.get_compiler('cpp')

subdir('vendor/imgui')

fs = import('fs')

src = [
    fs.copyfile('Shaders/Default.hlsl'),
    fs.copyfile('Shaders/LightingUtil.hlsl'),
    fs.copyfile('Shaders/TreeSprite.hlsl'),
    fs.copyfile('Models/skull.txt'),
    fs.copyfile('Models/car.txt'),
    fs.copyfile('Textures/bricks.dds'),
    fs.copyfile('Textures/bricks2.dds'),
    fs.copyfile('Textures/bricks2_nmap.dds'),
    fs.copyfile('Textures/bricks3.dds'),
    fs.copyfile('Textures/bricks_nmap.dds'),
    fs.copyfile('Textures/canada.dds'),
    fs.copyfile('Textures/checkboard.dds'),
    fs.copyfile('Textures/default_nmap.dds'),
    fs.copyfile('Textures/desertcube1024.dds'),
    fs.copyfile('Textures/flagArray.dds'),
    fs.copyfile('Textures/grass.dds'),
    fs.copyfile('Textures/grasscube1024.dds'),
    fs.copyfile('Textures/head_diff.dds'),
    fs.copyfile('Textures/head_norm.dds'),
    fs.copyfile('Textures/ice.dds'),
    fs.copyfile('Textures/jacket_diff.dds'),
    fs.copyfile('Textures/jacket_norm.dds'),
    fs.copyfile('Textures/pants_diff.dds'),
    fs.copyfile('Textures/pants_norm.dds'),
    fs.copyfile('Textures/snowcube1024.dds'),
    fs.copyfile('Textures/stone.dds'),
    fs.copyfile('Textures/sunsetcube1024.dds'),
    fs.copyfile('Textures/texassemble.exe'),
    fs.copyfile('Textures/tile.dds'),
    fs.copyfile('Textures/tile_nmap.dds'),
    fs.copyfile('Textures/tree0.bmp'),
    fs.copyfile('Textures/tree01S.dds'),
    fs.copyfile('Textures/tree02S.dds'),
    fs.copyfile('Textures/tree1.bmp'),
    fs.copyfile('Textures/tree2.bmp'),
    fs.copyfile('Textures/tree35S.dds'),
    fs.copyfile('Textures/treearray.dds'),
    fs.copyfile('Textures/treeArray2.dds'),
    fs.copyfile('Textures/uk.dds'),
    fs.copyfile('Textures/upBody_diff.dds'),
    fs.copyfile('Textures/upbody_norm.dds'),
    fs.copyfile('Textures/us.dds'),
    fs.copyfile('Textures/water1.dds'),
    fs.copyfile('Textures/white1x1.dds'),
    fs.copyfile('Textures/WireFence.dds'),
    fs.copyfile('Textures/WoodCrate01.dds'),
    fs.copyfile('Textures/WoodCrate02.dds'),
    'Common/Camera.cpp',
    'Common/d3dApp.cpp',
    'Common/d3dUtil.cpp',
    'Common/DDSTextureLoader.cpp',
    'Common/GameTimer.cpp',
    'Common/GeometryGenerator.cpp',
    'Common/MathHelper.cpp',
    'Waves.cpp',
    'FrameResource.cpp',
    'Parthenon.cpp'
]

deps = [
    cpp.find_library('d3d12'),
    cpp.find_library('dxgi'),
    cpp.find_library('d3dcompiler'),
    imgui
]

exe = executable('parthenon', src,
    cpp_args : [ '/permissive', '-DUNICODE', '/utf-8' ],
    win_subsystem : 'console',
    dependencies : deps
)
