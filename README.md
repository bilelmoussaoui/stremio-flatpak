# stremio-flatpak
Stremio Flatpak package (WIP)

## TODO:
- [ ] Add tray icon support on old distro
- [ ] Add an AppData file
- [ ] Bundle a higher resolution icon
- [ ] Contact upstream to use it as an official distribution system
- [ ] The application keeps running on the background when you close it (tray icon is hidden)


## How to build:
1 - Install [Flatpak](https://flatpak.org/setup/) & flatpak-builder

2 - Add Flathub remote

```
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```

3 - Install freedesktop's runtime

```bash
flatpak install flathub org.freedesktop.Platform//18.08
flatpak install flathub org.freedesktop.Sdk//18.08
```

4 - Install Electron's BaseApp

```
flatpak install flathub org.electronjs.Electron2.BaseApp//stable
```

5 - Clone the repository

```
git clone --recurse-submodules https://github.com/bilelmoussaoui/stremio-flatpak/
cd ./stremio-flatpak
``` 

6 - Build & Install Stremio's Flatpak package
```
flatpak-builder --install stremio com.stremio.Stremio.yml
```
