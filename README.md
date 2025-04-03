# 'dlss' for non-nvidia-cards on linux / steam deck (FSR3.1-workaround; open / free / legal)
## also enables 'frame-generation' in current games (AMD / Intel-Chips since 2015; usually doubles framerate)

> git clone https://github.com/slynobody/dlss-enabler-mod-for-linux (stable)

1. unpack the files in same folder of the main executable
2. search for 'nvngx_dlss.dll', copy it in the exe-folder
3. rename 'nvngx_dlss.dll' to '_nvngx.dll' in the exe-folder
4. add this to 'starting-options' (steam)

add (>> f.e for hogwarts legacy, steam)
> WINEDLLOVERRIDES="version,dxgi=n,b" %COMMAND%  --dlss-nvapi=mock
> 
or (>> f.e. for jedi survivor, steam)
> WINEDLLOVERRIDES="winmm=n,b" %COMMAND% -dlss-nvapi=mock
>
5. start game ('dlss' and 'frame-generation' should be useable)

# it does not work with rdr2 (vulkan)?!
dlss only (no fg yet): download rdr3_dlss.tar.gz, untar, put all files in rdr2-folder, add >WINEDLLOVERRIDES="version=n,b" %COMMAND%< to steams starting options)

# want a more user-friendly version (linux)
try: https://github.com/xXJSONDeruloXx/Decky-Framegen (needs decky-loader: https://decky.xyz/)

# FAQ
## where do i find the 'nvngx_dlss.dll'?
search in games folders, f.e. hogwarts has it in "Hogwarts Legacy/Engine/Plugins/Runtime/Nvidia/DLSS/Binaries/ThirdParty/Win64/nvngx_dlss.dll"

## in what folder should i put the content of the package?
in the same folder the main executeable resides, f.e. hogwarts has it in "Hogwarts Legacy/Phoenix/Binaries/Win64/"

## it does not work
1. try removing dxgi.dll and / or
2. try to put this in 'starting-options' (steam)
> `WINEDLLOVERRIDES="winmm=n,b" %COMMAND%

## is this legal?
yes, it depends only on open / free components

## is this scriptable?
offer PRs

----
# about
this repo tries to make the 'dlss-enabler' mod (https://www.nexusmods.com/site/mods/757?tab=files) usable for linux / steam-deck-users in the most simple way.

<a href="https://artsandculture.google.com/experiment/viola-the-bird/nAEJVwNkp-FnrQ?cp=e30."><img src="https://images.pling.com/img/00/00/78/78/79/2160403/proxy-image1.jpeg"/></a>
