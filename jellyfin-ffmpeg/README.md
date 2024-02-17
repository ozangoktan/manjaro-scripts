# Instructions for building an override of jellyfin-ffmpeg
This is necessary to actually use hardware acceleration with nvidia-470 driver on Kepler family GPU's. The packaged version is not built against ffnvcodec-headers-11-1, which means that package is incompatible and fails on runtime. 

    git clone https://github.com/jellyfin/jellyfin-ffmpeg.git
    cd jellyfin-ffmpeg
    ./configure --bindir=/usr/lib/jellyfin-ffmpeg
    make -j$(nproc)
    sudo make install
