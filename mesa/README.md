# Mesa
Enables nonfree video codecs in manjaro mesa stable release.

**These instructions are only for mesa packages version 24.0.8-1**

    git clone https://gitlab.manjaro.org/packages/extra/mesa/
    cd mesa
    git reset --hard a69e0afc3f406a8a0225b5a7c86994d136cca515
    git apply ../enable-nonfree.patch
    makepkg --syncdeps -f
    makepkg --install

## Key error during build
    gpg --recv-keys 8D8E31AFC32428A6

## Removal
    sudo pacman -S libva-mesa-driver mesa mesa-vdpau opencl-clover-mesa mesa opencl-rusticl-mesa vulkan-intel vulkan-mesa-layers vulkan-nouveau vulkan-radeon vulkan-swrast vulkan-virtio