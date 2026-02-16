# 🟦 Cube Studio 2D-X

**The Next-Generation C++/Lua Game Framework** Developed and Maintained by **Cubey Studio Codex**.

---

## 🚀 Overview

**Cube Studio 2D-X** is a high-performance, lightweight 2D game engine inspired by the classic Cocos2d-x architecture but rebuilt from the ground up for the modern era. It exclusively supports **C++** and **Lua**, eliminating the overhead of multi-language runtimes to provide raw performance for professional developers.

### Key Features
* **Modern C++ Core:** Engineered for **C++17, C++20, C++23, and C++26**.
* **Codex Bridge:** Ultra-fast Lua 5.4 bindings using a custom Sol3-based architecture.
* **Pure Workflow:** No JavaScript/TypeScript. Just pure C++ power and Lua flexibility.
* **Visual Studio 2026 Optimized:** Full support for the latest MSVC compilers and modules.

---

## 🛠️ Getting Started (Visual Studio 2026)

### 1. Prerequisites
Ensure you have the following installed:
* **Visual Studio 2026** (Preview or Stable) with "Desktop development with C++" workload.
* **vcpkg** (Recommended for dependency management).
* **CMake 3.28+**.

### 2. Project Configuration
To leverage the full power of **C++26**, set your project language standard in Visual Studio:
1. Right-click on your Project -> **Properties**.
2. Navigate to **Configuration Properties > C/C++ > Language**.
3. Set **C++ Language Standard** to `ISO C++ Latest Draft (/std:c++latest)`.

### 3. Installation
```bash
git clone [https://github.com/cubey-studio-codex/cube-studio-2dx.git](https://github.com/cubey-studio-codex/cube-studio-2dx.git)
cd cube-studio-2dx
# Initialize submodules (Lua, SDL2, etc.)
git submodule update --init --recursive
```

#### 📝 Example Usage (Lua)
The Cube Studio 2D-X API is designed to be clean and intuitive:
```Lua
local cs = require("CubeStudio")

function cs.LoadImage()
    sheet = cs.Sprite:loadImage("images/hero.png")
    sheet:setSheet(256, 256)
end

function cs.Update(dt)
    -- Moving the sprite using C++23 powered math backend
    if sheet:getPos() == cs.LEFT then
        sheet:moveX(100 * dt)
    end
end

function cs.Draw()
    sheet:draw()
end
```

##### ⚖️ Licensing
This project is governed by the **Cubey LICENSE 1.0**.
As a unique and secure license, all terms regarding commercial use, attribution, and technical compliance are defined in the structured [LICENSE.yaml](./LICENSE.yaml) file.

**Summary:**

- **Non-Commercial Use:** Free for education and personal projects.

- **Commercial Use:** Requires a signed contract from **Cubey Studio Codex**.

- **Attribution:** Mandatory splash screen and source headers.

###### 🤝 Contributing
We welcome contributions that follow our high-performance standards. Please ensure all Pull Requests:
1. Target C++17 as the baseline, preferably using **C++23** features.
2. Maintain the integrity of the **Codex Bridge**.
3. Pass all memory leak tests in Visual Studio 2026.
**Organization:** [https://github.com/cubey-studio-codex](https://github.com/cubey-studio-codex)
