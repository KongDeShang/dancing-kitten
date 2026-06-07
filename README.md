# 🐱 Dancing Kitten — 终端像素动画

在终端里播放像素风小猫动画！将 GIF 渲染为 ANSI True Color 画面，支持自动抠图、自适应缩放，默认 2×2 网格四只猫同步跳舞。

![Demo](pixel_animation/cat_pixel_animation.gif)

## ✨ 特性

- 读取 GIF 帧并在终端中循环播放
- 自动抠除白色背景和浅色底板（flood fill + 形态学处理）
- ANSI True Color 渲染，保持像素风格
- 2×2 网格布局，四只小猫同步播放
- 自动适配终端窗口大小

## 🚀 快速开始

```bash
# 克隆
git clone https://github.com/KongDeShang/dancing-kitten.git
cd dancing-kitten

# 安装依赖
pip install -r pixel_animation/requirements.txt

# 开玩！
python pixel_animation/animation.py
```

按 `Ctrl + C` 退出动画。

## 📁 项目结构

```
.
├── .gitignore
├── LICENSE
├── README.md
├── pixel_animation/
│   ├── animation.py              # 主程序
│   ├── cat_pixel_animation.gif   # 动画源文件
│   ├── requirements.txt          # Python 依赖
│   └── README.md                 # 详细文档
```

## ⚙️ 自定义

编辑 `pixel_animation/animation.py` 中的常量：

| 常量 | 默认值 | 说明 |
|------|--------|------|
| `DEFAULT_RENDER_WIDTH` | 48 | 默认渲染宽度 |
| `MIN_RENDER_WIDTH` | 20 | 最小渲染宽度 |
| `CAT_GAP` | `"    "` | 小猫间距 |
| `WHITE_DISTANCE_THRESHOLD` | 24 | 白底识别阈值 |

## 📋 环境要求

- Python 3.10+
- 支持 ANSI True Color 的终端（Windows Terminal、iTerm2、macOS Terminal 等）

## 📄 许可证

[MIT](LICENSE)

---

*一只会跳舞的小猫，送给每一个热爱像素风的人。*
