***These instructions are obsolete as of kwin 5.27.11 release***

# Kwin
Fixes pipewire causing heavy stuttering.

**These instructions are only for kwin package version 5.27.10.**

    git clone https://gitlab.manjaro.org/packages/kde-unstable/plasma/kwin
    cd kwin
    git reset --hard 07e995ba5864b8a560359c4d0bc9b196e65182f9
    git apply ../fix-stutter.patch
    makepkg --syncdeps -f
    makepkg --install
