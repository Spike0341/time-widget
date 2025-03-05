# Retro Digital Time Widget

A lightweight desktop widget for Windows featuring a retro digital clock display with alarm functionality and a Pomodoro timer.

![Screenshot](https://github.com/user-attachments/assets/723f793d-792f-4f10-bcaa-5bbda7e55eb1)

## Features

- Semi-transparent, frameless window with a retro digital display
- Large, easy-to-read time display
- Support for up to 10 customizable alarms
- Built-in Pomodoro timer for productivity
- Minimal RAM usage
- Movable window (click and drag anywhere)
- Clean interface with settings hidden behind a gear icon

## Prerequisites

- [Node.js](https://nodejs.org/) (version 14 or higher recommended)

## Installation

### Quick Start

1. Clone or download this repository
2. Navigate to the project directory in your terminal/command prompt
3. Install dependencies:
   ```
   npm install
   ```
4. Run the application:
   ```
   npm start
   ```

### Complete Setup Guide

#### Setting up from scratch

1. Create a new folder for your project:
   ```
   mkdir time-widget
   cd time-widget
   ```

2. Initialize a new Node.js project:
   ```
   npm init -y
   ```

3. Install Electron:
   ```
   npm install electron --save-dev
   ```

4. Create the following file structure:
   ```
   time-widget/
   ├── main.js
   ├── index.html
   ├── package.json
   └── fonts/
       └── digital-7.ttf (or your preferred font)
   ```

5. Update package.json:
   ```json
   {
     "name": "time-widget",
     "version": "1.0.0",
     "description": "Digital time widget with alarms and pomodoro timer",
     "main": "main.js",
     "scripts": {
       "start": "electron ."
     }
   }
   ```

6. Copy the HTML and main.js code from this repository into your project files

## Usage

### Basic Controls

- **Time Display**: Shows the current time in HH:MM:SS format
- **Gear Icon** (⚙️): Click to show/hide the settings panel
- **Pomodoro Button**: Starts a 25-minute timer for focused work sessions
- **Add Alarm Button**: Creates a new alarm with a custom time and label

### Managing Alarms

1. Click the gear icon to reveal settings
2. Click "Add Alarm" to create a new alarm
3. Enter the time in HH:MM format
4. Type a name for your alarm in the text field
5. Toggle alarms on/off with the button
6. Delete alarms with the × button

### Using the Pomodoro Timer

1. Click the gear icon to reveal settings
2. Click "Pomodoro" to start a 25-minute timer
3. When the timer completes, you'll receive an alert
4. Click "Stop" to cancel the timer

### Moving the Widget

- Click and drag anywhere on the widget to move it around your screen

## Creating a Standalone Executable

To create a standalone .exe file that doesn't require Node.js:

1. Install electron-builder:
   ```
   npm install electron-builder --save-dev
   ```

2. Add to package.json:
   ```json
   "scripts": {
     "start": "electron .",
     "build": "electron-builder"
   },
   "build": {
     "appId": "com.yourname.timewidget",
     "win": {
       "target": "portable"
     }
   }
   ```

3. Build the executable:
   ```
   npm run build
   ```

4. Find your standalone .exe in the `dist` folder

## Creating a Windows Shortcut

For easier access without packaging:

1. Right-click on your desktop
2. Select New > Shortcut
3. Enter: `cmd.exe /c "cd /d [FULL-PATH-TO-PROJECT] && npm start"`
4. Name it "Time Widget" or similar

## Customization

### Changing the Font

1. Download your preferred digital font (.ttf or .woff format)
2. Place it in the `/fonts` directory
3. Update the font-family in the CSS section of index.html

### Changing Colors

1. Find the CSS in index.html
2. Modify the color values:
   - Background color: `rgba(34, 34, 34, 0.8)` (last value controls transparency)
   - Text color: `#0fe4ff` (cyan blue)

## Troubleshooting

### Widget Won't Start

- Ensure Node.js is properly installed
- Check that all dependencies are installed with `npm install`
- Verify your project has the correct structure
- Check that the digital font file exists in the location specified

### Font Not Displaying Correctly

- Make sure your font file is in the correct location
- Verify the font name in the CSS matches the actual font name
- Try using a different font format (TTF, WOFF, WOFF2)

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Digital font: [Digital-7](https://www.dafont.com/digital-7.font)
- Built with [Electron](https://www.electronjs.org/)
