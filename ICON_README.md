# 网站图标说明

本项目包含以下图标文件：

## 📁 图标文件

### 主要Logo
- `logo.svg` - 主要品牌Logo，包含完整的设计元素
- 尺寸：120x120px
- 用途：网站头部logo，营销材料

### Favicon文件
- `favicon.svg` - 现代浏览器支持的SVG favicon
- `favicon-simple.svg` - 简化版SVG favicon
- 尺寸：32x32px / 16x16px
- 用途：浏览器标签页图标

### Web App Manifest
- `site.webmanifest` - PWA应用清单文件
- 包含应用元数据和图标引用

## 🔧 生成PNG格式图标

要生成完整的favicon套装，您需要创建以下PNG文件：

### 所需PNG文件
```
favicon-16x16.png    (16x16px)
favicon-32x32.png    (32x32px) 
apple-touch-icon.png (180x180px)
```

### 生成方法

#### 方法1：使用在线工具
1. 访问 https://realfavicongenerator.net/
2. 上传 `logo.svg` 文件
3. 按需调整设置
4. 下载生成的文件包

#### 方法2：使用命令行工具
```bash
# 安装 ImageMagick (如果尚未安装)
# macOS: brew install imagemagick
# Ubuntu: sudo apt-get install imagemagick

# 从SVG生成PNG
magick logo.svg -resize 16x16 favicon-16x16.png
magick logo.svg -resize 32x32 favicon-32x32.png
magick logo.svg -resize 180x180 apple-touch-icon.png
```

#### 方法3：使用Node.js工具
```bash
npm install -g sharp-cli
sharp -i logo.svg -o favicon-16x16.png --width 16 --height 16
sharp -i logo.svg -o favicon-32x32.png --width 32 --height 32
sharp -i logo.svg -o apple-touch-icon.png --width 180 --height 180
```

## 🎨 设计说明

### Logo设计元素
- **主色调**：香蕉黄 (#fbbf24)
- **渐变色**：从明黄到深黄橙
- **科技元素**：蓝色电路图案和nano点阵
- **现代感**：毛玻璃效果和阴影

### 品牌寓意
- **香蕉形状**：代表"Nano Banana"品牌
- **科技元素**：体现AI技术属性
- **渐变色彩**：现代、专业的视觉感受
- **简洁设计**：确保小尺寸下的清晰度

## 📱 浏览器支持

- **SVG Favicon**：Chrome 80+, Firefox 41+, Safari 9+
- **PNG Fallback**：所有浏览器
- **Apple Touch Icon**：iOS Safari, 安卓浏览器
- **Web App Manifest**：支持PWA的现代浏览器

## 🚀 使用建议

1. **主要使用SVG**：现代浏览器优先使用SVG格式
2. **提供PNG后备**：确保老旧浏览器兼容性
3. **移动端优化**：Apple Touch Icon确保iOS体验
4. **PWA就绪**：Web App Manifest支持渐进式Web应用

生成PNG文件后，将它们放在网站根目录即可完成图标系统的部署。
