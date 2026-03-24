# minesense-vue3
一个多模态融合的智能矿压管理系统,建立了系统概览层/传感层/数据层/模型层/决策执行层的五层结构,融入模型训练模块和生成式AI
# MineSense · 智能矿压系统 (Vue 3 版)

基于 Vue 3 + Vite 构建的智能矿压监测系统前端界面。

## 技术栈

- **Vue 3** - 使用 Composition API
- **Vite** - 极速构建工具
- **原生 CSS3** - 无需额外 CSS 框架

## 项目结构

```
minesense-vue3/
├── public/              # 静态资源
├── src/
│   ├── assets/          # 资源文件
│   │   └── styles/      # 全局样式
│   ├── components/      # Vue 组件
│   │   ├── ParticleBackground.vue   # 粒子背景组件
│   │   ├── NavigationIndicators.vue # 导航指示器组件
│   │   ├── TopNav.vue               # 顶部导航栏组件
│   │   └── OverviewView.vue         # 概览视图组件
│   ├── App.vue          # 根组件
│   └── main.js          # 应用入口
├── index.html           # HTML 模板
├── package.json         # 项目依赖
└── vite.config.js       # Vite 配置
```

## 快速开始

### 1. 安装依赖

```bash
cd minesense-vue3
npm install
```

### 2. 启动开发服务器

```bash
npm run dev
```

访问 http://localhost:3000 查看效果。

### 3. 构建生产版本

```bash
npm run build
```

构建后的文件将输出到 `dist/` 目录。

### 4. 预览生产构建

```bash
npm run preview
```

## 核心功能

### 五大功能模块

1. **系统概览** - 展示系统整体运行状态和关键指标
2. **传感层** - 展示自移式多源监测钻孔机器人的数据采集功能
3. **数据层** - 展示多模态数据融合与处理能力
4. **模型层** - 展示AI预测模型与分析功能
5. **决策执行层** - 展示冲击地压防控与保水充填协同减灾方案

### 交互特性

- **动态粒子背景** - 根据当前界面主题动态变化粒子颜色和动画效果
- **左右滑动切换** - 支持鼠标拖拽、触摸滑动和键盘方向键导航
- **自动演示模式** - 一键开启自动轮播功能
- **响应式设计** - 适配不同屏幕尺寸的设备
- **无障碍支持** - 符合 WCAG 标准，支持减少动画模式

## 设计规范

### 色彩系统

| 模块 | 主色值 | 说明 |
|------|--------|------|
| 系统概览 | #06B6D4 | 科技蓝 |
| 传感层 | #00D9C0 | 青绿色 |
| 数据层 | #3B82F6 | 蓝色 |
| 模型层 | #10B981 | 绿色 |
| 决策执行层 | #F59E0B | 金色 |

### 字体系统

- 字体族：Inter / -apple-system
- 标题字重：600-700
- 正文字重：400-500
- 数据字重：700

## 组件说明

### ParticleBackground.vue
粒子背景组件，根据当前界面索引动态生成不同颜色和动画效果的粒子。

**Props:**
- `currentIndex` (Number) - 当前界面索引

### NavigationIndicators.vue
底部导航指示器组件，显示当前界面位置。

**Props:**
- `total` (Number) - 总界面数
- `current` (Number) - 当前界面索引

**Events:**
- `switch` - 切换界面时触发

### TopNav.vue
顶部导航栏组件，包含系统 Logo 和操作按钮。

**Events:**
- `demo` - 点击自动演示按钮时触发
- `reset` - 点击重置按钮时触发

### OverviewView.vue
概览视图组件，展示各个模块的详细信息。

**Props:**
- `data` (Object) - 界面数据（标题、描述、卡片等）
- `isActive` (Boolean) - 是否为当前激活界面

**Events:**
- `demo` - 演示状态变化时触发
- `reset` - 重置时触发

## 浏览器兼容性

- Chrome/Edge (最新版本)
- Firefox (最新版本)
- Safari (最新版本)
- 移动端浏览器 (iOS Safari, Chrome Mobile)

## 优化建议

1. 添加路由管理（Vue Router）以支持更复杂的页面跳转
2. 集成状态管理工具（Pinia）处理全局状态
3. 添加数据可视化组件展示实时监测数据
4. 增加 3D 矿井模型展示功能
5. 集成用户认证和权限管理系统

## 开发说明

### 添加新的功能模块

1. 在 `src/components/` 目录下创建新组件
2. 在 `App.vue` 中的 `views` 数组添加新模块数据
3. 遵循现有的组件结构和命名规范

### 修改粒子效果

编辑 `src/components/ParticleBackground.vue` 中的 `layerColors` 对象：

```javascript
const layerColors = {
  0: { color: '#06B6D4', animation: 'float' },
  // 添加或修改其他层级
}
```

## 许可证

本项目基于"西部煤炭开发智能矿压感知预警与保水充填韧性减灾协同调控体系"开发，版权归原项目团队所有。
