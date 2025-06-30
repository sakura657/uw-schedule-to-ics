# UW-Madison 课程表 → ICS 导出工具

🔗 在线体验 → [https://sakura657.github.io/uw-schedule-to-ics](https://sakura657.github.io/uw-schedule-to-ics)

简体中文 | [English](README.md)

一个基于网页的工具，可以将您的 UW-Madison 课程表导出为 iCalendar (.ics) 格式，方便导入到 Google 日历、Apple 日历、Outlook 等日历应用中。

## 🎯 功能特点

- **简易导出**：将 UW 课程表转换为标准 iCalendar 格式
- **时区准确**：正确处理中部时间 (America/Chicago) 和夏令时
- **自定义提醒**：为所有课程设置默认提醒
- **位置支持**：在日历事件中包含教室位置信息
- **响应式设计**：支持桌面和移动设备
- **UW-Madison 品牌**：使用官方大学色彩和样式

## 🚀 快速开始

1. **获取课程表 HTML**：
   - 登录 [MyUW Home](https://my.wisc.edu)
   - 打开 "Course Schedule"
   - 选择学期并点击 "Update"
   - 右键点击 → "View Page Source"（查看页面源代码）
   - 全选 (Ctrl/Cmd+A) 并复制 (Ctrl/Cmd+C)

2. **使用工具**：
   - 在浏览器中打开 `schedule_export.html`
   - 粘贴 HTML 源代码
   - 设置学期开始和结束日期
   - 选择提醒偏好
   - 点击 "Generate ICS File"（生成 ICS 文件）

3. **导入到日历**：
   - 下载生成的 `.ics` 文件
   - 导入到您喜欢的日历应用

## 📋 系统要求

- 现代网页浏览器 (Chrome, Firefox, Safari, Edge)
- 访问 UW-Madison MyUW 门户的权限
- 互联网连接（用于 Tailwind CSS 和字体）

## 🛠️ 技术详情

### 支持的事件类型
- ✅ 讲座 (LEC)
- ✅ 实验 (LAB) 
- ✅ 研讨会 (SEM)
- ✅ 讨论课 (DIS)
- ⚠️ 在线课程（如无具体上课时间则跳过）

### 时区处理
- 所有事件使用 `TZID=America/Chicago` 导出
- 自动处理夏令时 (DST) 转换
- 正确计算中部时间的工作日

### 数据处理
- 解析来自 MyUW 的课程表 HTML
- 提取上课时间、地点和课程信息
- 生成符合 RFC 标准的 iCalendar 格式
- 处理带学期结束日期的每周重复事件

## 🎨 界面特色

- **现代设计**：使用 Tailwind CSS 的简洁专业界面
- **UW 品牌**：官方大学红色 (#c5050c) 配色方案
- **响应式布局**：针对所有屏幕尺寸优化
- **分步指南**：带编号步骤的清晰说明
- **表单验证**：有用的错误消息和输入验证

## 🔧 故障排除

### 常见问题

**"Cannot find const data = { ... }; block"（找不到数据块）**
- 确保复制了完整的 HTML 源代码
- 确保浏览器语言设置为英文
- 尝试刷新 MyUW 页面并重新复制

**"No events found inside data block"（数据块中未找到事件）**
- 验证您选择了正确的学期
- 检查您在所选学期是否有已注册的课程

**事件出现在错误的日期**
- 最新版本已修复此问题
- 工具现在正确处理工作日的时区转换

### 浏览器兼容性
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

## 📁 文件结构

```
Export-ICS-UW-Madison/
├── schedule_export.html    # 主应用程序文件
├── README.md              # 英文文档
├── README_CN.md           # 中文文档
└── images/                # （可选）图标和资源
```

## 🤝 贡献

欢迎贡献！请随时提交问题或拉取请求。

### 开发设置
1. 克隆仓库
2. 在浏览器中打开 `schedule_export.html`
3. 使用示例 UW 课程表数据进行更改和测试

## 📄 许可证

本项目是开源的，采用 MIT 许可证。

## 🙏 致谢

- 威斯康星大学麦迪逊分校的课程表系统
- Tailwind CSS 样式框架
- FullCalendar 日历灵感

## 📞 支持

如果遇到问题：
1. 查看上面的故障排除部分
2. 确保使用支持的浏览器
3. 验证您的 UW 课程表 HTML 是完整的
4. 在 GitHub 上提交问题并提供详细信息

---

**注意**：此工具与 UW-Madison 官方无关。这是一个社区创建的实用工具，帮助学生管理他们的课程表。

## 📚 使用说明

### 详细步骤

1. **准备工作**
   - 确保您已登录 MyUW 系统
   - 建议使用 Chrome 或 Firefox 浏览器

2. **获取源代码**
   - 在课程表页面，确保显示的是您想要导出的学期
   - 使用 Ctrl+U (Windows) 或 Cmd+Option+U (Mac) 快速查看源代码
   - 或右键点击页面空白处选择"查看页面源代码"

3. **设置日期**
   - 学期开始日期：通常是第一周周一
   - 学期结束日期：通常是期末考试周结束
   - 可参考学校官方学术日历

4. **选择提醒**
   - 建议设置 15-30 分钟提前提醒
   - 可根据个人习惯调整

5. **导入日历**
   - Google 日历：设置 → 导入和导出 → 选择文件
   - Apple 日历：文件 → 导入
   - Outlook：文件 → 打开和导出 → 导入/导出

### 注意事项

- 在线课程可能不会显示具体时间，工具会自动跳过
- 如果课程时间有变更，需要重新导出
- 建议定期备份您的日历数据
