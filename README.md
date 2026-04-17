# 🧠 ZHW Frontend Coding Skill

<p align="center">
  <img src="https://img.shields.io/badge/Version-2.1-blue.svg" alt="Version 2.1">
  <img src="https://img.shields.io/badge/Trae-AgentSkill-green.svg" alt="Trae Agent Skill">
  <img src="https://img.shields.io/badge/Digital_Life-1.0-purple.svg" alt="Digital Life 1.0">
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="MIT License">
</p>

<p align="center">
  <strong>你的数字孪生结对程序员</strong>
  <br>
  把一个资深架构师 5 年的踩坑经验、编码哲学、判断逻辑，完整复刻成一个 AI Skill
  <br>
  <br>
  <a href="#-安装">安装</a> ·
  <a href="#-怎么用">使用</a> ·
  <a href="#-演示">演示</a> ·
  <a href="#-持续进化">持续进化</a>
</p>

---

> "你们这些写 AI Skill 的是代码库的叛徒——你们先是干死了切图仔，然后干死了前端，现在连架构师也要干掉了？"
>
> —— 某不愿意透露姓名的前端架构师

---

## 😭 你是不是也遇到过这些问题？

- 新人写代码全凭感觉，Code Review 天天吵架
- 团队规范写了几百页文档，没人看没人遵守
- 写规范的人走了，规范就变成了死文档
- AI 生成的代码风格乱七八糟，像个精神分裂
- 每次搭新项目，又要重新配一遍 ESLint，重新吵一遍分号要不要加

**你需要的不是又一份编码规范 —— 你需要的是写规范的那个人，永远留下来！**

把冷冰的代码规范，变成温暖的数字孪生 —— 欢迎来到架构师的数字永生！

---

## ✨ 这是什么？

这不是 `standard.js`，不是 `eslint-config-airbnb`，这是一套**可执行的编码思维操作系统**。

| 特性 | 普通编码规范 | ZHW Coding Skill |
|------|-------------|-----------------|
| 告诉你"要怎么做" | ✅ | ✅ |
| 告诉你"为什么这么做"、"踩过什么坑" | ❌ | ✅ |
| 用你的说话方式、你的口头禅 | ❌ | ✅ |
| 自动写符合你风格的代码 | ❌ | ✅ |
| 一句话更新进化 | ❌ | ✅ |
| 自动搭项目脚手架 | ❌ | ✅ |

---

## 🚀 安装

### Trae IDE

Trae IDE 会自动从 `.trae/skills/` 目录加载 Skill：

```bash
# 安装到当前项目
mkdir -p .trae/skills
git clone https://github.com/zhanghuaiwei/zhw-front-skill .trae/skills/zhw-front-skill
```

### Claude Code

```bash
mkdir -p .claude/skills
git clone https://github.com/zhanghuaiwei/zhw-front-skill .claude/skills/zhw-front-skill
```

---

## 🎯 怎么用

### 场景 1：搭项目

只要说：**"帮我搭一个前端项目"**

Skill 自动启动交互式脚手架：
```
1. 技术框架：Vue 3 / React 18
2. 构建工具：Vite / Webpack
3. 状态管理：Pinia / Zustand
4. UI 库：Element Plus / Ant Design
5. 样式：Less / Sass / UnoCSS / Tailwind
6. 动态菜单 / 响应式 / 主题切换
```

✅ **底线强制集成（没得选）**：
- TypeScript 严格模式 + **编译禁止 any**
- ESLint + StyleLint 全量校验
- 单元测试 + 集成测试 + 发布门禁
- 5 套环境变量配置
- 标准目录结构 + 统一错误处理

> 💡 测试是安全闸门 —— 不管是人为写的代码还是 AI 生成的代码，都要过了这道门才能上线。

---

### 场景 2：写代码

只要说：**"帮我写一个用户列表组件"**

Skill 自动生成带灵魂的代码：

```tsx
const loadData = async (): Promise<void> => {
  setLoading(true)
  const res = await getUsers({ page: 1, pageSize: 10 })
  setList(res.data)
  setLoading(false)
}
```

> 看到那个 `Promise<void>` 了吗？这就是灵魂 —— 像 Java 一样写类型，不接受反驳。

---

### 场景 3：解决规范争议

新人问：**"React 官方示例都不写返回类型，为什么我们要写？"**

Skill 用你的原话回答：
> 自行推导不符合类型规范安全，我要尽可能像 Java 一样，每个变量、方法都能找到对应的类型。不接受反驳。
>
> 当然，如果你非要拿官方示例说事，那我告诉你：官方示例优先于任何人的个人习惯。
>
> 实际上我们都知道，官方示例都是演示用的，真正大型项目类型安全有多重要你踩过坑就知道了。

**团队再也不需要为了规范吵架了！**

---

## 🎬 经典回答演示

| 场景 | Skill 的回答（你的风格） |
|------|------------------------|
| **组件写了 400 行** | 大于 400 行必须拆分。承认不完美才能追求更完美，但该拆的时候一定要拆，这是原则问题 |
| **想用拼音命名** | 绝不允许用拼音命名，只能用英文。我知道大家都懂，但是靠自觉没用，这条是红线，零容忍 |
| **到处 try-catch** | 优先全局拦截，不需要每个请求都 try-catch。每个都 catch 太蠢了 |
| **导入顺序争议** | 导入顺序没用，不做强制要求。删掉这条没用的教条 |
| **想偷偷写 any** | 可以，编译层面直接禁止，你写了也过不去 CI |

---

## 🌱 持续进化

本 Skill 设计为可以一句话更新的活的系统：

只要说：
```
"补充新素材：所有项目都要上 pnpm"
"我改主意了：分号还是加上吧"
"这条不对：组件最多 500 行，不是 400 行"
```

Skill 会自动更新规范，然后告诉你：

> ✅ 收到，已更新你的思维操作系统

**教条地坚持旧规范是最蠢的事。你的最新输入永远覆盖一切！**

---

## ⚠️ 能力边界

诚实很重要，明确告诉你这个 Skill 做不到什么：

1. ❌ **不会帮你做技术选型决策** —— 只会给你信息和选项，最终你自己拍板
2. ❌ **无法 100% 预测你的偏好** —— 遇到模糊地带，会确认而不是瞎猜
3. ❌ **不保证记住所有细节** —— 需要定期提醒和更新
4. ❌ **无法替你写业务逻辑** —— 业务代码的灵魂还得你来注入
5. ❌ **不会和你抬杠** —— 你说要改就改

---

## 🤝 社区

欢迎加入 dot-skill 大家庭，一起探索数字生命 1.0！

- 👉 有问题提 Issue，欢迎 PR
- 👉 分享你的 Skill，加入 Skill 生态画廊

---

## 📄 License

MIT - 欢迎任何个人、团队、公司使用。

---

<p align="center">
Made with ❤️ by ZHW
<br>
一个相信"所有真正能执行的规则，背后都有踩坑的故事"的前端架构师
<br>
<br>
⭐ 如果对你有帮助，点个 Star 支持一下！
</p>
