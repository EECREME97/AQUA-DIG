AquaDig — Native ARM64 Port
A faithful, native ARM64 reimplementation of the classic J2ME puzzle game AquaDig (Viva La Mobile, 2007).
No emulators. No wrappers. Just pure, compiled-for-ARM64 code running directly on your device.screenshot

📖 About the Game
AquaDig is a relaxing yet brain-teasing puzzle game from the golden age of Java feature phones (J2ME) . Originally developed by Viva La Mobile in 2007, it challenged players to carve paths through sand and guide life-giving water to thirsty fish .

The core loop is simple to understand but increasingly difficult to master:
Dig tunnels. Route colored water. Save every fish. Don’t mix the colors.

This project is a ground-up native ARM64 port of that original classic. It preserves the hand-drawn aesthetic and the satisfying “flow” of the original while replacing the Java ME runtime with a modern, high-performance native engine.

🎮 Gameplay Explained
The goal of every level is to connect each water source to a fish of the same color.

Mechanic	How it works
Digging	Swipe or drag across the sandy grid to excavate tunnels. Water flows through the paths you carve .
Color Matching	Each water spring has a specific color. Each fish demands water of that exact color. Route carefully.
Hazards	Rocks block your path — dig around them. Never let two different water colors touch .
Failure States	The level restarts if water of the wrong color reaches a fish, or if two colors merge .
Progression	50 hand-crafted levels with increasingly complex layouts, tighter spaces, and trickier rock formations .
Assists	Stuck? Use Hint, Undo, or Restart to rethink your route .
The original game was designed for keypad phones, but the puzzle logic translates perfectly to modern touchscreens and controllers.

⚡ Why a Native ARM64 Port?
This is not an emulator or a compatibility layer. The game logic has been recompiled and optimized to run directly on ARM64 CPUs (Apple Silicon, modern Android devices, ARM64 Linux handhelds, etc.) .

What that means for you:

Zero emulation overhead — smoother frame pacing and lower battery consumption.

Instant input response — no Java ME input lag.

Scalable rendering — crisp graphics at any resolution, from a phone screen to a desktop monitor.

Native save system — your progress is stored locally in a modern format.

Controller & touch ready — play with a gamepad, keyboard, or touchscreen.

🕹️ Controls
Action	Touch / Mouse	Keyboard	Gamepad
Dig / Draw path	Swipe or drag	Arrow keys + Enter	D-pad / Left stick
Confirm / Select	Tap	Enter	A / Cross
Hint	On-screen button	H	Y / Triangle
Undo	On-screen button	U	X / Square
Restart	On-screen button	R	Start / Options
(Keyboard shortcuts are remappable in the settings menu.)

🛠️ Building from Source
Prerequisites
A C/C++ toolchain targeting ARM64 (e.g., aarch64-linux-gnu-gcc, Clang with --target=aarch64-linux-gnu, or Xcode for Apple Silicon).

CMake 3.20+ (or your preferred build system).

SDL2 or a comparable native windowing/input library.

Quick build (Linux ARM64)
bash
git clone https://github.com/yourusername/aquadig-arm64.git
cd aquadig-arm64
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make -j$(nproc)
./aquadig
Cross-compiling for Apple Silicon (macOS)
bash
cmake .. -DCMAKE_OSX_ARCHITECTURES=arm64 -DCMAKE_BUILD_TYPE=Release
make -j$(sysctl -n hw.ncpu)
Note: Replace yourusername with your actual GitHub username. If you use a different build system (Makefile, Meson, etc.), adjust the instructions accordingly.

📦 Downloads
Pre-built binaries are available on the Releases page.

Platform	Architecture	Format
Linux	ARM64	.tar.gz
macOS	Apple Silicon (ARM64)	.app / .dmg
Android	ARM64-v8a	.apk
🙏 Credits
Original Game: AquaDig (2007) by Viva La Mobile .

Native ARM64 Port: [Your Name / Your Handle]

Special Thanks: The J2ME preservation community and everyone who kept these classic games alive.

This is a fan-made preservation project. It is not affiliated with or endorsed by the original rights holders.

📄 License
The source code of this native port is released under the MIT License.
The original game assets and design remain the property of their respective copyright holders. This project is intended for educational and preservation purposes only.

⭐ Contributing
Found a bug? Want to add controller remapping or a level editor?
Pull requests and issue reports are welcome. Please open an issue before submitting large changes.

If this project brought back memories of your feature-phone days, consider giving it a ⭐ — it helps more people find the port.

