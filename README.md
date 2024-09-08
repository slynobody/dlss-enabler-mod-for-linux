# dlss enabler mod ... on linux / steam deck (frame-generation / upscaling; open / free / legal)
## enables dlss- + frame-generation- options in current games (also on AMD / Intel-Chips)
## (regardless of graphics-card, usually doubles framerate)

> git clone https://github.com/slynobody/dlss-enabler-mod-for-linux (stable)
or download latest release (beta)

1. unpack the files insame folder of the main executable
2. search for 'nvngx_dlss.dll', copy it in the exe-folder
3. rename 'nvngx_dlss.dll' to '_nvngx.dll' in the exe-folder
4. add this to 'starting-options' (steam)
add (f.e for jedi survivor)
> WINEDLLOVERRIDES="version,dxgi=n,b" gamemoderun %COMMAND%  --dlss-nvapi=mock
> 
or (>> f.e. for hogwarts legacy, steam)
> WINEDLLOVERRIDES="winmm=n,b" gamemoderun %COMMAND% -dlss-nvapi=mock
>
5. start game ('dlss' and 'frame-generation' should be useable)


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
