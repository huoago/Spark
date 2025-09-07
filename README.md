# Spark Web - 短视频社交应用

这是 Spark 短视频社交应用的 Web 版本，基于 React 构建。

## 功能特性

- 🎬 短视频 Feed 流播放
- 📤 视频上传与发布
- 🔍 附近的人（基于地理位置）
- 📺 直播功能（信令占位）
- 📞 一对一视频通话（WebRTC）
- 💬 实时聊天
- 🍾 漂流瓶
- 📱 摇一摇匹配
- 🔐 用户认证与授权

## 技术栈

- React 18
- React Router DOM
- Axios
- Socket.IO Client
- WebRTC API
- Geolocation API
- CSS3 (响应式设计)

## 快速开始

### 1. 安装依赖

```bash
cd spark-web
npm install
```

### 2. 启动后端服务

确保后端服务运行在 `http://localhost:3000`：

```bash
cd ../server
npm install
npm start
```

### 3. 启动前端开发服务器

```bash
npm start
```

应用将在 `http://localhost:3001` 打开。

## 环境配置

创建 `.env.local` 文件：

```env
REACT_APP_API_URL=http://localhost:3000
REACT_APP_SIGNALING_URL=http://localhost:3000
```

## 功能说明

### 短视频 Feed
- 无限滚动加载
- 自动播放当前视频
- 视频信息展示

### 视频上传
- 支持拖拽上传
- 视频预览
- 描述编辑

### 附近的人
- 基于浏览器定位
- 自动上报位置
- 附近用户列表

### 视频通话
- WebRTC 本地媒体流
- 信令服务器通信
- 实时音视频传输

### 实时聊天
- Socket.IO 连接
- 房间管理
- 消息实时同步

## 移动端适配

- 响应式设计
- 触摸友好的界面
- 移动端优化的视频播放

## 浏览器支持

- Chrome 60+
- Firefox 55+
- Safari 11+
- Edge 79+

## 开发说明

### 项目结构

```
src/
├── components/          # 通用组件
├── screens/            # 页面组件
├── services/           # API 服务
├── utils/              # 工具函数
├── contexts/           # React Context
├── navigation/         # 路由配置
└── config/            # 配置文件
```

### 主要文件

- `App.js` - 应用入口
- `navigation/MainTabNavigator.js` - 主导航
- `services/auth.js` - 认证服务
- `services/video.js` - 视频服务
- `utils/location.js` - 定位工具

## 部署

### 构建生产版本

```bash
npm run build
```

### 部署到服务器

将 `build` 目录上传到 Web 服务器即可。

## 注意事项

1. 需要 HTTPS 环境才能使用摄像头和麦克风
2. 地理位置功能需要用户授权
3. WebRTC 需要 STUN/TURN 服务器支持
4. 建议使用现代浏览器以获得最佳体验

## 许可证

MIT License
