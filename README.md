![Banne](https://i.pinimg.com/originals/3f/35/90/3f3590a3809163db554425361295f121.jpg)

# Doctor Strange Filter with Python

This project is a test of my skills in computer vision. The project was created using Mediapipe and OpenCV libraries and Python program language. As the name suggests, I tried to replicate the magic circles that appear on the palms of the popular MARVEL hero Dr. Strange when he casts a spell.

To summarize the working logic of the project, the script starts by detecting hand gestures from your device's camera and then calculates the midpoint of your palm and the openness of your palm with these points.  If your hand is open enough, a mask (the filter itself) is created using the previously given images and pasted onto the calculated midpoint.  

Of course, this was a very simple explanation. There are many things to know about perspective, rotating image objects and creating transparent objects during this project. I hope this project will help you to understand these topics :

## Folder Structure

```
.
├── Models                    # Models to be used when creating the filter
|   ├── Inner Circles         # Circle models to be found on the inner side 
|   └── Outer Circles         # Circle models to be found on the outer side 
├── functions.py              
├── main.py                    
├── requirements.txt                   
└── README.md
```

## Requirements

- Python 3.7 or higher
- Webcam/Camera
- Windows/Mac/Linux

## Installation & Setup

### Step 1: Clone the Repository
```bash
git clone https://github.com/shloksathe18-dotcom/Doctor-Strange-Filter
cd Doctor-Strange-Filter
```

### Step 2: Create Virtual Environment (Recommended)
```bash
python -m venv venv
```

### Step 3: Activate Virtual Environment

**Windows:**
```bash
.\venv\Scripts\activate
```

**Mac/Linux:**
```bash
source venv/bin/activate
```

### Step 4: Install Dependencies
```bash
pip install -r requirements.txt
```

## How to Run

### Method 1: Using Batch File (Windows - Easiest)
Simply double-click the `run.bat` file in the project folder.

### Method 2: Using Python Command
```bash
python main.py
```

### Method 3: Using Virtual Environment
```bash
.\venv\Scripts\python.exe main.py
```

### Method 4: Using run_simple.py (With Step-by-Step Output)
```bash
python run_simple.py
```

## How to Use

1. **Start the Application** - Run the program using any of the methods above
2. **Camera Window Opens** - A window titled "Image" or "Doctor Strange Filter" will appear
3. **Show Your Hand** - Position your hand in front of the camera
4. **See the Magic:**
   - **Open Hand (fingers spread wide)** → Magic circles appear and rotate on your palm
   - **Closed Hand/Fist** → Connecting lines appear between your fingers
5. **Exit** - Press the **'q'** key to quit the application

## Configuration

You can customize the filter by editing `config.json`:

```json
{
    "camera": {
        "width": 1280,
        "height": 720,
        "device_id": 0
    },
    "line_settings": {
        "color": [0, 140, 255],
        "thickness": 5
    },
    "overlay": {
        "inner_circle_path": "Models/inner_circles/orange.png",
        "outer_circle_path": "Models/outer_circles/orange.png",
        "rotation_degree_increment": 2,
        "shield_size_multiplier": 3.0
    },
    "keybindings": {
        "quit_key": "q"
    }
}
```

### Customization Options:
- **Camera Settings:** Change resolution or camera device ID
- **Line Color:** Modify RGB values for hand gesture lines
- **Circle Images:** Choose different circle designs from the Models folder
- **Rotation Speed:** Adjust `rotation_degree_increment` for faster/slower rotation
- **Circle Size:** Change `shield_size_multiplier` for larger/smaller circles

## Troubleshooting

### Camera Not Opening
- Make sure your camera is connected
- Close other applications using the camera
- Try changing `device_id` in config.json (0, 1, or 2)

### Window Not Appearing
- Check if the window is minimized or behind other windows
- Try running from command prompt to see error messages

### Import Errors
- Make sure all dependencies are installed: `pip install -r requirements.txt`
- Use virtual environment to avoid conflicts

### Performance Issues
- Lower the camera resolution in config.json
- Close other resource-intensive applications

## Features

- Real-time hand detection using MediaPipe
- Rotating magic circles effect
- Hand gesture recognition
- Customizable colors and effects
- Multiple circle design options

## Technologies Used

- **Python** - Programming language
- **OpenCV** - Computer vision and image processing
- **MediaPipe** - Hand tracking and detection
- **NumPy** - Numerical computations



## Contributing

Feel free to fork this project and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is open source and available for educational purposes.

## Author

**Shlok**

<p align="center">
<a href="https://github.com/shloksathe18-dotcom">
<img src="https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github&logoColor=white"/ >
</a>
</p>

---

<p align="center">Made with ❤️ using Python, OpenCV, and MediaPipe</p>
