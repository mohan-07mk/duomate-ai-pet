# DuoMate Desktop Pet 💕
### 3D Animated Desktop Couple Pet with PC Monitoring & Assistant

A cute, lightweight Windows desktop pet application featuring **Mohan** and **AI Companion** in 3D animated figurine form, faithful to the reference image character design.

---

## 🌟 Key Features

### 1. 3D Character Figurine Models & Animations
- **Mohan**: Boy with styled dark hair, black cap with perched sunglasses, maroon hoodie with kangaroo pocket & drawstrings, cream trousers, maroon-and-white skate sneakers.
- **AI Companion**: Blonde anime girl with soft bangs and shoulder locks, maroon hoodie, cream trousers, maroon-and-white sneakers, sparkling eyes with eyelashes, and rosy blushing cheeks.
- **10 Smooth Real-Time Animations**:
  - `idle`: Gentle breathing, chest rise/fall, natural relaxed sway.
  - `blink`: Automatic natural eyelid blinking every few seconds.
  - `smile`: Warm cheerful smile and facial expressions.
  - `look_at_each_other`: Dynamic head & neck tracking looking at each other.
  - `walk`: Natural leg swing, knee bend, foot plant, and arm counter-swing.
  - `sit`: Hips lowering, knees bending, hands resting on lap.
  - `hug`: Romantic embrace, arms wrapped around partner, heads leaning close with warm blushing.
  - `hold_hands`: Inner hands reaching and clasping together.
  - `blush`: Cheeks glowing warm pink/red with shy head tilt.
  - `couple_walk`: Synchronized couple walk cycle side-by-side.
- **Automatic Romantic Couple Interactions**:
  - Automatically every few minutes, the female companion looks at Mohan, approaches him, interacts (romantic hug or holding hands with floating heart particles), and walks together with him.

### 2. Transparent Floating Desktop Pet
- **Frameless & Transparent**: Pure 3D characters floating on top of Windows applications without window borders or background boxes.
- **Independent Drag & Drop**:
  - Drag Mohan anywhere across the 3D pet space.
  - Drag AI Companion independently.
  - Drag the top handle or background to move the entire window anywhere on the desktop.
  - Automatically saves desktop window coordinates and character offsets.
- **Mouse & Context Menu Interactions**:
  - Click Mohan: Mohan smiles and waves.
  - Click AI Companion: Companion speaks friendly greetings with lip-sync.
  - Double Click: Instantly triggers a romantic hug!
  - Right Click: Context menu to trigger actions, check PC stats, or open settings.

### 3. Female Voice & Animated Speech Bubbles
- Offline Windows TTS integration (Web Speech API with Microsoft Zira / Jenny / female voice options).
- Speech bubble with typing effect and tail pointing to AI Companion.
- Lip-sync: Mouth moves and head gestures while speaking.
- Mute/unmute control and volume slider.

### 4. Real PC Hardware Monitoring
Genuine hardware readings using `systeminformation`:
- **CPU Temperature** (Genuine reading or `Unavailable`).
- **CPU Usage %**.
- **GPU Usage & GPU Temperature** where supported by hardware.
- **RAM Usage %** and GB details.
- **Battery %** and charging status (or `Unavailable (Desktop PC)`).
- Friendly voice warnings when thresholds are exceeded:
  - *"Mohan! CPU temperature romba high-ah irukku. Check pannunga!"*
  - *"Mohan! RAM usage 90% aagudhu!"*
  - *"Mohan! Battery 15% dhaan irukku. Charger connect pannunga!"*

### 5. Water & Break Reminders
- **Water Reminder**: Configurable intervals (default 45 mins).
  - *"Mohan! Water kudikka marandhuteengala? Konjam water kudinga!"*
- **Break Reminder**: Configurable work sessions (default 50 mins work + 10 mins break).
  - *"Mohan! Romba nerama work panreenga. Konjam break eduthukonga!"*
- Simple enable/disable switches and test buttons.

### 6. Settings Window & System Tray
- Simple, beautiful settings dialog:
  - Voice on/off & volume slider.
  - Character size: Small / Medium / Large.
  - Water reminder intervals.
  - Work & break intervals.
  - Hardware monitoring enable/disable.
  - Notification enable/disable.
  - Start with Windows toggle (`openAtLogin`).
  - Couple interaction frequency.
- System Tray menu for quick access, mute/unmute, and couple actions.

---

## 🚀 How to Run

### Option 1: Quick Launch (One-Click)
Double-click `start-duomate.bat` in the project folder.

### Option 2: Run via Terminal
```bash
npm start
```

### Option 3: Install Windows App (.exe)
Run the official setup installer in `dist/`:
```
dist/DuoMate Desktop Pet-Setup-1.0.0.exe
```
Or run the single-file standalone portable executable:
```
dist/DuoMate Desktop Pet-Portable-1.0.0.exe
```
Or run the unpacked executable:
```
dist/win-unpacked/DuoMate Desktop Pet.exe
```

---

## 📁 Project Structure

```
duomate-ai/
├── couple-reference.png              # Visual reference image
├── start-duomate.bat                 # One-click launch script
├── package.json                      # Dependencies and electron-builder config
├── README.md                         # Documentation
├── assets/
│   ├── icons/                        # Application icons (.ico and .png)
│   └── models/
│       ├── mohan.glb                 # 3D Rigged Mohan with 10 animations
│       ├── companion.glb             # 3D Rigged AI Companion with 10 animations
│       └── couple_scene.glb          # Full couple scene
├── dist/                             # Built Windows installer & portable app
│   ├── DuoMate Desktop Pet-Setup-1.0.0.exe      # Windows Setup Installer
│   ├── DuoMate Desktop Pet-Portable-1.0.0.exe   # Standalone Portable .exe
│   └── win-unpacked/
│       └── DuoMate Desktop Pet.exe
├── src/
│   ├── main.js                       # Electron main process, tray, IPC
│   ├── preload.js                    # Secure context bridge
│   ├── monitor.js                    # Hardware monitor (CPU, GPU, RAM, Battery)
│   ├── reminders.js                  # Water & break timers
│   ├── character.js                  # 3D Character controller & skeletal rigging
│   ├── pet.html                      # Transparent desktop pet overlay
│   ├── pet.js                        # Three.js 3D viewport, drag & drop, TTS
│   ├── settings.html                 # Settings window UI
│   ├── settings.js                   # Settings logic and live stats updater
│   └── lib/                          # Bundled Three.js and GLTFLoader modules
└── scripts/
    ├── generate-characters.mjs       # Script to regenerate 3D models & animations
    └── generate-icons.py             # Script to regenerate application icons
```

---

## 🎮 Controls & Shortcuts

| Action | Control |
|---|---|
| Move Character Independently | Click & drag Mohan or AI Companion |
| Move Desktop Pet Window | Drag the top header pill or background |
| Mohan Click Reaction | Left click Mohan (Smiles & waves) |
| Companion Voice Greeting | Left click AI Companion (Speaks greetings) |
| Instant Romantic Hug | Double click anywhere on the pet window |
| Context Menu | Right click on the pet window |
| Open Settings | Click ⚙️ in the top bar or via System Tray |
| Mute / Unmute Voice | Click 🔊 in the top bar or via Settings / Tray |
| Exit Application | Right click -> Close Pet, or Exit via System Tray |

---

## 🛠️ Rebuilding Assets & Distribution

To regenerate the 3D GLB character models:
```bash
npm run build:assets
```

To build a fresh Windows installer and executable:
```bash
npm run dist
```
