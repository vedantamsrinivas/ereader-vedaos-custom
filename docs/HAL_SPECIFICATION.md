# E-Reader OS - HAL Specification

## Display HAL

### Methods:
- **setRefreshMode(mode):** FAST | SLOW | FULL refresh
- **updateRegion(x, y, width, height, data):** Update screen region
- **getDisplayCapabilities():** Query display specs
- **setPartialUpdate(enabled):** Toggle partial updates

## Power Management HAL

### Methods:
- **setGovernor(name):** CPU power mode
- **setFrequency(hz):** CPU frequency
- **getBatteryStatus():** Battery info
- **setChargingProfile(id):** Charging behavior

## Input HAL

### Methods:
- **getInputDevices():** List input devices
- **readInputEvents():** Get user input
- **enableSensor(type):** Enable sensor

## Storage HAL

### Methods:
- **mountStorage(path):** Mount device
- **unmountStorage(path):** Unmount device
- **getStorageInfo():** Storage status

## Connectivity HAL

### Methods:
- **enableWiFi() / disableWiFi()**
- **enableBluetooth() / disableBluetooth()**
- **scanNetworks():** Find WiFi networks

## Notes
- Returns: 0 = success, -1 = error
- All methods should be thread-safe
- HAL is device-specific, framework is not
```

Press **Ctrl + S** to save

---

### **3. Create .gitignore**

Right-click file explorer → **New File** → Type: `.gitignore`

Copy and paste this:
```
# Build outputs
out/
build/
*.apk
*.dex
*.so

# IDE
.idea/
.vscode/
*.iml

# Build system
.gradle/
gradle/

# Large files
android-aosp/
*.tar.gz
*.zip

# OS files
.DS_Store
Thumbs.db
*.log