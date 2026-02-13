# muCommander - Single-Click Dark Edition

Fork of [muCommander 1.5.2](https://github.com/mucommander/mucommander) with usability improvements.

## Changes from Original

### 🖱️ Single-Click Navigation
- **Removed double-click requirement** - single left-click instantly opens files and folders
- **Command+click for multi-select** - hold Command (Mac) or Ctrl (Windows/Linux) and click to select multiple files
- **Right-click context menu** - access rename, delete, and other operations
- **Shift+click for range selection** - select ranges of files
- Eliminated 80+ lines of complex double-click detection code

### 🌙 Dark Mode by Default
- **FlatLaf Dark theme** set as default Look & Feel - no more blinding white screens on startup
- **Native theme** works seamlessly with FlatLaf Dark
- **Early FlatLaf registration** ensures dark theme is available in initial setup dialog
- **Proper preference defaults** for fresh installs

### 🔧 Technical Details

Modified files:
- `FileTable.java` - Simplified mouse click handling, removed double-click logic
- `WindowManager.java` - Changed default LAF to FlatDarkLaf
- `Application.java` - Early FlatLaf registration, conditional LAF initialization
- `InitialSetupDialog.java` - Preselect FlatLaf Dark in setup wizard
- `MuPreferences.java` - Changed default theme to Native (works with FlatLaf Dark)

### 🚀 Installation

Download the latest release and copy `mucommander-core-1.5.2.jar` and `mucommander-preferences-1.5.2.jar` to:
- **macOS**: `/Applications/muCommander.app/Contents/app/app/` and `/Applications/muCommander.app/Contents/app/bundle/`
- **Linux/Windows**: Replace corresponding JAR files in your muCommander installation

Or build from source (requires JDK 11+):
```bash
./gradlew build
```

---

**Why these changes?**
- Double-clicking is slow and inefficient
- Single-click navigation is standard in modern file managers
- Bright white defaults are hostile to users
- Dark themes reduce eye strain and look better

**Original muCommander**: https://www.mucommander.com
