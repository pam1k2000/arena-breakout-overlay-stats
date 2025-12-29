# 🎮 Arena Breakout Stats

> Real-time statistics tracker and overlay system for Arena Breakout: Infinite streamers

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Electron](https://img.shields.io/badge/Electron-28.0.0-blue.svg)](https://www.electronjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-LTS-green.svg)](https://nodejs.org/)

Arena Breakout Stats is a powerful desktop application designed for streamers of Arena Breakout: Infinite. It automatically tracks game statistics using OCR technology and provides beautiful, customizable overlays for OBS Studio.

## ✨ Features

### 📊 Automatic Statistics Tracking
- **Red Items** - Track rare items found during raids
- **Player Kills** - Monitor enemy eliminations
- **Loot Value** - Calculate total extracted loot value
- **Gear Spent** - Track equipment costs
- **Profit Calculation** - Automatic profit/loss calculation

### 🔍 OCR Technology
- **Automatic Recognition** - Uses Tesseract.js for OCR scanning
- **Custom Region Selection** - Configure scan areas for optimal accuracy
- **Real-time Updates** - Statistics update automatically during gameplay
- **Multi-language Support** - Supports English and Russian text recognition

### 🎨 Multiple Overlay Styles
Choose from 8 different overlay designs:
- **Main Overlay** - Classic design
- **Horizontal Minimal** - Clean horizontal layout
- **Horizontal Neon** - Eye-catching neon style
- **Vertical Minimal** - Compact vertical layout
- **Vertical Cards** - Card-based design
- **Webcam Frames** - 3 styles with animated frames for webcam integration

### 🎮 Smart State Management
- **PRE_RAID** - Captures gear cost before raid
- **IN_RAID** - Tracks activity during raid
- **POST_RAID** - Waits for results screen
- **RESULTS_FIXED** - Automatically transfers stats to stream total

### ⌨️ Global Hotkeys
- `Ctrl+Shift+1` - OCR scan for gear cost
- `Ctrl+Shift+2` - OCR scan for loot value
- `Ctrl+Shift+3` - OCR scan for kills
- `Ctrl+Shift+F1` - Add red item
- `Ctrl+Shift+F2` - Add player kill
- `Ctrl+Shift+F5` - Reset statistics

### 🌐 Multilingual Interface
- Russian and English language support
- Easy language switching in the UI

## 📸 Screenshots

> *Screenshots coming soon*

## 🚀 Installation

### Prerequisites
- Windows 10/11
- OBS Studio (for overlay integration)
- Arena Breakout: Infinite game

### Quick Start

1. **Download the latest release**
   ```bash
   # Download from Releases page
   ```

2. **Extract and run**
   - Extract the archive
   - Run `arena-breakout-stats.exe`
   - Activate license on first launch

3. **Configure OBS**
   - Add Browser Source in OBS
   - URL: `http://localhost:3001/overlay`
   - Set width: 1920, height: 1080

## 📖 Usage

### Initial Setup

1. **Configure OCR Regions**
   - Open Settings
   - Click "Add New Region"
   - Select screen areas for:
     - Gear cost display
     - Loot value display
     - Kills counter

2. **Enable Auto-Scanning**
   - Toggle on desired OCR regions
   - Application will automatically scan every 500ms

3. **Add Overlay to OBS**
   - Create Browser Source
   - Use URL: `http://localhost:3001/overlay`
   - Adjust size to match your stream resolution

### Basic Workflow

1. Launch Arena Breakout: Infinite
2. Start Arena Breakout Stats
3. Open OBS Studio with overlay configured
4. Start streaming - statistics update automatically!

### Manual Controls

- **Add Statistics** - Manually input values if OCR fails
- **Reset Stats** - Clear current or stream statistics
- **Transfer Stats** - Move current stats to stream total
- **State Buttons** - Manually switch between raid states

## 🛠️ Development

### Requirements
- Node.js (LTS version)
- npm or yarn

### Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/arena-breakout-stats.git
cd arena-breakout-stats

# Install dependencies
npm install

# Run in development mode
npm start

# Build for Windows
npm run build
```

### Project Structure

```
arena-breakout-stats/
├── electron/          # Electron-specific modules
│   ├── hotkeyManager.js
│   └── regionSelector.js
├── public/            # Frontend files
│   ├── overlay*.html  # Overlay templates
│   ├── control.html   # Control panel
│   └── settings.html  # Settings page
├── server/            # Backend services
│   ├── database.js    # SQLite database
│   ├── ocrScanner.js  # OCR engine
│   └── statsController.js
├── src/               # Core modules
│   └── core/          # License, HWID, i18n
├── utils/             # Utility functions
│   ├── screenCapture.js
│   └── windowFinder.js
└── main.js            # Electron main process
```

## 🧪 Technologies

- **Electron** - Cross-platform desktop framework
- **Tesseract.js** - OCR engine for text recognition
- **Express** - Web server for overlay API
- **SQLite3** - Local database for statistics
- **Sharp** - Image processing
- **RobotJS** - Global hotkey support

## 📝 Configuration

Configuration files are stored in `config/`:
- `regions.json` - OCR scan regions
- `settings.json` - Application settings

Statistics are stored in SQLite database: `stats.db`

## 🔧 Troubleshooting

### OCR Not Working
- Ensure regions are properly configured
- Check screen resolution matches region setup
- Verify text is clear and visible
- Try adjusting brightness/contrast

### Overlay Not Showing
- Verify application is running
- Check URL: `http://localhost:3001/overlay`
- Ensure port 3001 is not blocked
- Refresh Browser Source in OBS

### Game Window Not Found
- Launch game before application
- Manually select window from list
- Check window title contains "Arena Breakout"

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📧 Support

For issues, questions, or support:
- Open an issue on GitHub
- Check existing issues for solutions

## 🎯 Roadmap

- [ ] Linux support
- [ ] macOS support
- [ ] Additional overlay themes
- [ ] Export statistics to CSV/JSON
- [ ] Cloud sync for statistics
- [ ] Advanced OCR accuracy improvements

## 🙏 Acknowledgments

- Built with [Electron](https://www.electronjs.org/)
- OCR powered by [Tesseract.js](https://tesseract.projectnaptha.com/)
- Icons from [Icons8](https://icons8.com/)

---

**Made with ❤️ for the Arena Breakout streaming community**

