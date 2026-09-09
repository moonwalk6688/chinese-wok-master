# Chinese Wok Master｜中式锅气大师

一个面向 Codex 的家庭中餐烹饪研究与执行 Skill。

它不是简单的菜谱生成器，而是把一道菜拆解成可研究、可比较、可适配、可执行和可复盘的家庭烹饪方案。核心问题是：

> 在家用燃气灶和熟铁锅的条件下，这道菜究竟怎样做更好吃、更稳定、更容易复现？

## 核心能力

- 自动识别菜品、菜系、地区、流派和关键技术难点
- 联网检索传统做法、专业厨师方法、家庭版本与失败案例
- 按 A/B/C/D 对来源进行评级，并对重要结论交叉验证
- 解释不同做法之间的冲突，而不是简单取平均值
- 针对家用天然气灶、熟铁锅和有限火力重新设计流程
- 提供精确用量、0–5级火力、时间轴和看／听／闻判断
- 输出粘锅、出水、发柴、发苦、断裂和没有锅气等失败诊断

## 默认厨房画像

- 福建家庭饮食环境
- 家用天然气燃气灶
- 熟铁锅／碳钢锅
- 默认2–3人份
- 有基础炒菜经验
- 追求家庭可复现、食材状态、火候、锅气和餐厅级口感

用户提供不同设备、人数或口味时，显式条件会覆盖默认配置。

## 四种工作模式

### 1. 做菜模式

输入一道菜名或询问具体做法。Skill 会先联网研究，再给出适配家庭厨房的完整执行方案。

```text
使用 $chinese-wok-master，帮我做家庭燃气灶版干炒牛河。
```

### 2. 深度研究模式

比较不同地区、流派、名厨和餐厅方法，分析争议并形成家庭最优方案。

```text
使用 $chinese-wok-master，深度研究全国最好吃的蛋炒饭。
```

### 3. 冰箱模式

根据现有食材推荐3–5道菜，说明选择理由；确定菜品后再进入完整烹饪流程。

```text
使用 $chinese-wok-master，我有鸡蛋、青椒和猪肉，可以做什么？
```

### 4. 复盘模式

针对一次失败的烹饪进行诊断，给出最可能原因排序和下一锅的具体修改方式。

```text
使用 $chinese-wok-master，我今天炒上海青出了很多水，为什么？
```

## 工作流程

```text
识别菜品与流派
    ↓
拆解关键烹饪问题
    ↓
多轮联网研究
    ↓
来源评级与交叉验证
    ↓
解释流派、设备和食材差异
    ↓
适配家用燃气灶与熟铁锅
    ↓
精确用量、火力、时间轴和感官状态
    ↓
失败诊断与灶边极简执行版
```

## 安装

### Windows

```powershell
git clone https://github.com/moonwalk6688/chinese-wok-master.git "$env:USERPROFILE\.codex\skills\chinese-wok-master"
```

### macOS／Linux

```bash
git clone https://github.com/moonwalk6688/chinese-wok-master.git ~/.codex/skills/chinese-wok-master
```

也可以在 GitHub 页面选择 **Code → Download ZIP**，解压后把 `chinese-wok-master` 文件夹放入 Codex 的 `skills` 目录。

安装完成后，重新启动 Codex 或开启一个新任务。

## 输出内容

完整做菜方案通常包括：

1. 菜品真正的核心
2. 多源研究结论与流派选择
3. 精确食材表与调味系统
4. 开火前准备
5. 火力和时间轴
6. 看、听、闻的感官判断
7. 五个关键秘诀
8. 常见失败点与诊断
9. 家庭锅气强化方案
10. 可放在灶边查看的极简执行版

## 目录结构

```text
chinese-wok-master/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── kitchen-profile.md
│   ├── research-rules.md
│   ├── source-ranking.md
│   ├── wok-heat-system.md
│   ├── cooking-science.md
│   ├── food-safety.md
│   └── output-template.md
├── templates/
│   ├── recipe-template.md
│   ├── deep-research-template.md
│   └── troubleshooting-template.md
└── tests/
    └── test-cases.md
```

## 设计原则

- 具体菜品默认先联网研究，不凭模型记忆冒充“顶级做法”
- 不允许单一低质量来源支持核心结论
- 不伪造厨师观点、餐厅方法、引用或研究结果
- 不机械照搬专业猛火灶操作
- 不用“适量、少许、大火炒熟”等模糊表达代替可观察标准
- 食品安全优先于嫩度、速度和锅气
- 最终目标始终是：**更好吃、更稳定、家庭可复制**

