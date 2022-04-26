# Usage Instructions
## TODO Adaptation
- Windows 7 or above (64-bit)
- Genshin Impact running at 1920x1080, 1366x768 or 1280x720 windowed
- TODO To be updated Yuanxia Palace and Crane Temple
- English version TBA

## Running via a Release
- Download the latest release and unzip it.
- Run `main.exe` with administrator privileges. Make sure the path to it has no special characters in it. Genshin Impact must be in the foreground, running at a supported window resolution.

## Running via Source Code
- Configure python 3.7 + opencv 3.1~3.4 (the latter is tricky due to patent issues) + opencv-contrib. I use opencv-python3.4.2.17
- Install other libraries required by the project (pyqt5, keyboard...)
- Run `main.py` with administrator privileges

## Features
- Search and mark map resources
- Delete all markers on the currently visible map
- Delete the marker at the cursor and add it to the resource respawn queue
- Get contextual information based on the cursor location
- Delete the current location marker and add it to the respawn queue
  - After deletion in this manner, it will be refreshed after the corresponding respawn time.
- ~~Minimap tracking map_track.py (TODO The current solutions speed is 0.6s/time and the accuracy is ok in non-towns~~

## Technical solutions
- python + opencv + qt5
- opencv surf-flann-based matching for current map coordinates
- Use file cache image feature points to speed up
- ![celestial coordinate]([celestial coordinate](https://github.com/GengGode/GenshinImpact_AutoTrack_DLL#%E5%A4%A9%E7%90%86%E5%9D%90%E6%A0%87%E6%A8%A1%E5%9E%8B)) conversion
- Use opencv TM_SQDIFF_NORME algorithm D template matching to find Genshin Impact ui buttons
- Wwin32 API simulates keyboard and mouse
- pyqt to render the UI

## Map data
- Map point data from ![Kongying Taverns yuan-shen-map](https://github.com/kongying-tavern/yuan-shen-map)

## Configuring shortcuts
- Modify each line after the colon
- For specific shortcut keys, please refer to python keyboard
