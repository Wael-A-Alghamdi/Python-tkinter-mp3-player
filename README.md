# Python MP3 Player (Tkinter GUI)

This is a simple MP3 player desktop application built using Python. The graphical interface is developed with Tkinter, and audio playback is handled using the Pygame mixer. The app supports playlist management, volume control, playback buttons, and saves user volume preferences in a config file.

##  How to Run the Project

### Requirements
Install the required libraries using pip:
pip install tk
pip install ttkthemes
pip install pygame
pip install mutagen

### Run the App

To start the MP3 player:
python Main.py

##  Features

- Play / Pause / Stop / Rewind
- Skip forward and backward
- Volume scale with mute button
- Playlist section with add/remove file or directory
- Save / Load / Clear playlist (.mldpl format)
- File and Help navigation bar
- Footer bar with status display
- Config file (`config.cfg`) saves last volume setting

##  Tools and Libraries Used

- Python 3
- Tkinter (GUI framework)
- TtkThemes (custom themes for GUI)
- Pygame (mixer for audio playback)
- Mutagen (for MP3 metadata)
- Threading, OS, Time (built-in modules)

##  Description of Main Functionalities

- `Add File to Playlist`: Uses `filedialog.askopenfilename()` to let user browse and add MP3 files. Filenames are extracted and added to the playlist using `append()`.
- `Play/Stop/Rewind`: Controls playback using `pygame.mixer.music` methods such as `.play()`, `.stop()`, and custom rewinding logic.
- `Volume Control`: The current volume is stored in `config.cfg` and restored on next launch.
- `Exit/Quit`: Stops audio, saves volume, and exits the application cleanly.
- `About`: Opens an info window describing the app via `tkinter.messagebox.showinfo()`.
