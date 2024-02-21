# Mesa
Enables nonfree video codecs in manjaro mesa stable release.

**These instructions are only for mesa packages version 23.3.5.**

    git clone https://gitlab.manjaro.org/packages/extra/mesa/
    cd mesa
    git reset --hard b5475d046505dfd2ef5fbe2fe39e09f3f44543d9
    git apply ../enable-nonfree.patch
    makepkg --syncdeps -f
    makepkg --install

## Key error during build
    gpg --recv-keys 8D8E31AFC32428A6

## Removal
    sudo pacman -S vulkan-swrast libva-mesa-driver mesa-vdpau vulkan-virtio opencl-clover-mesa vulkan-intel mesa opencl-rusticl-mesa vulkan-mesa-layers mesa vulkan-radeon