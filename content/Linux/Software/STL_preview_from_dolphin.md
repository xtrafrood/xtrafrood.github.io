---
title: 💻 KDE STL Preview
author: Chris Schammert (csmertx -- Christopher Schammert )
published: 2023-02-04
weight: -20
---

<!-- The content of this website was written by Christopher Schammert aka Chris Schammert -->

<br />

<br />
<div style="text-align: center;">

![albumimg](/Linux/Software/Screenshot_20220401_000441.png "Kubuntu 21.10 screenshot of opening STL with view3dscene")
<br />

> Kubuntu 21.10 screenshot of opening STL with view3dscene
</div>
<br />

<br />
<div style="text-align: center;">

![albumimg](/Linux/Software/Screenshot_20220401_000521.png "Kubuntu 21.10 screenshot of view3dscene")
<br />

> Kubuntu 21.10 screenshot of view3dscene
</div>
<br />


## View3dscene installation

- Download link: ```https://castle-engine.io/view3dscene.php```

- Or if you prefer: ```https://github.com/castle-engine/view3dscene```

- Extract w/Dolphin > Right Click > Extract > Extract Archive Here

- ```vim $HOME/.local/share/applications/view3dscene.desktop```

    ```
    [Desktop Entry]
    Comment[en_US]=A graphical frontend for viewing 3D meshes
    Comment=A graphical frontend for viewing 3D meshes
    Exec=/home/chris/.sources/view3dscene/view3dscene
    GenericName[en_US]=View3dscene
    GenericName=View3dscene
    Icon=/home/chris/Pictures/Icons/3dview.png
    Name[en_US]=View3dscene
    Name=View3dscene
    StartupNotify=false
    Terminal=false
    Type=Application
    Categories=Utility
    ```

- ```sudoc /home/chris/.sources/view3dscene/view3dscene```

- Right Click .stl file in Dolphin, open with view3dscene (check box to remember)

- ```Icon=``` used: ```https://www.freepngimg.com/png/32221-3d-image```

<br />

<div style="text-align: center; font-size:12px; color:dimgray">
    Created: 04/01/2022 • Edited: 02/09/2025 • Author: Chris Schammert (csmertx) • 
    <a href="https://github.com/csmertx/csmertx.github.io/commits/main/content/Linux/Software/STL_preview_from_dolphin.md" 
       title="Github.com | csmertx \ csmertx.github.io \ commits \ main \ content \ Linux \ Software \ KDE STL Preview">
       History 🕵️
    </a>
</div>