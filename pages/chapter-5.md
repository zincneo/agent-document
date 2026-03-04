---
transition: fade-out
---

# 第五节：驱动龙虾需要 Token

<div class="mt-10 px-8">

<div class="flex items-center justify-center gap-12">

<div v-click class="text-center">
  <div class="text-6xl mb-4">🦞</div>
  <div class="text-lg text-black/60">OpenClaw 本身免费开源</div>
</div>

<div v-click class="text-5xl text-black/30">+</div>

<div v-click class="text-center">
  <div class="text-6xl mb-4">🧠</div>
  <div class="text-lg text-black/60">大模型 API（需付费）</div>
</div>

<div v-click class="text-5xl text-black/30">=</div>

<div v-click class="text-center">
  <div class="text-6xl mb-4">⚡</div>
  <div class="text-lg text-black/60">AI Agent 开始工作</div>
</div>

</div>

<div v-click class="mt-10 mx-auto max-w-2xl p-5 rounded-xl bg-[var(--ctp-lavender)]/10 border-2 border-[var(--ctp-lavender)] text-center">
  <div class="text-base leading-relaxed">Token 是 LLM 处理语言的基本单位（约 4 个英文字符 = 1 Token）<br/>每一次推理、记忆调取、工具调用、技能执行都在消耗 Token<br/><strong>Token = AI 时代的"电费"</strong></div>
</div>

</div>

---
transition: slide-up
---

## LLM 后端：两种接入方式

<div class="mt-8 px-6">

<div class="grid grid-cols-2 gap-6">

<div v-click class="p-6 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="text-3xl mb-3">☁️</div>
  <div class="font-semibold text-lg mb-3">云端 API 调用</div>
  <div class="text-sm text-black/70 leading-relaxed mb-4">通过网络调用大模型服务商提供的 Token API 或常规鉴权登录</div>
  <div class="flex flex-col gap-2">
    <div class="flex items-center gap-2 text-sm">
      <span class="text-[var(--ctp-green)]">✓</span> 无需硬件投入，即开即用
    </div>
    <div class="flex items-center gap-2 text-sm">
      <span class="text-[var(--ctp-green)]">✓</span> 始终使用最新最强模型
    </div>
    <div class="flex items-center gap-2 text-sm">
      <span class="text-[var(--ctp-red)]">✗</span> 数据经网络传输，隐私风险
    </div>
    <div class="flex items-center gap-2 text-sm">
      <span class="text-[var(--ctp-red)]">✗</span> 持续产生 Token 费用
    </div>
  </div>
</div>

<div v-click class="p-6 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="text-3xl mb-3">🖥️</div>
  <div class="font-semibold text-lg mb-3">本地模型部署</div>
  <div class="text-sm text-black/70 leading-relaxed mb-4">通过 llama.cpp / Ollama 调用部署在本地的开源模型</div>
  <div class="flex flex-col gap-2">
    <div class="flex items-center gap-2 text-sm">
      <span class="text-[var(--ctp-green)]">✓</span> 数据完全不出内网，隐私安全
    </div>
    <div class="flex items-center gap-2 text-sm">
      <span class="text-[var(--ctp-green)]">✓</span> 可微调行业专属模型
    </div>
    <div class="flex items-center gap-2 text-sm">
      <span class="text-[var(--ctp-red)]">✗</span> 需要 GPU 硬件投入
    </div>
    <div class="flex items-center gap-2 text-sm">
      <span class="text-[var(--ctp-red)]">✗</span> 模型能力受限于硬件规模
    </div>
  </div>
</div>

</div>

</div>

---
transition: slide-left
---

## 闭源模型：Claude（Anthropic）

<div class="mt-4 px-4">

<div class="flex gap-6">

<div class="flex-1">

<div v-click class="p-4 mb-4 rounded-xl bg-[var(--ctp-lavender)]/10 border-2 border-[var(--ctp-lavender)]">
  <div class="text-sm text-black/70 leading-relaxed">当前全球最强 AI 编程与 Agent 能力。Claude Opus 4.6 断档式领先，官方 Claude Code CLI + Cowork 桌面端体验超越 OpenClaw。<strong>专业用户首选</strong>，实测 MAX $200 订阅的研发能力可持平大厂 50 万年薪程序员</div>
</div>

<div v-click class="text-xs mb-3 text-black/50">⚠️ 严格检测 IP 地址，非干净美区 IP 易封号</div>

<div v-click>

| 订阅方案 | 月费 | 核心权益 |
|---------|------|---------|
| Free | $0 | 基础访问，用量有限 |
| Pro | $20 | 5x 用量，全模型访问 |
| Max 5x | $100 | 25x 用量，含 Claude Code |
| Max 20x | $200 | 100x 用量，最高优先级 |

</div>

</div>

<div v-click class="w-72 shrink-0">
  <div class="p-4 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
    <div class="text-sm font-semibold mb-3">API 价格（每百万 Token）</div>
    <div class="flex flex-col gap-2 text-xs">
      <div class="flex justify-between p-2 rounded-lg bg-[var(--ctp-base)]">
        <span class="font-semibold">Opus 4.6</span>
        <span>$5 / $25</span>
      </div>
      <div class="flex justify-between p-2 rounded-lg bg-[var(--ctp-base)]">
        <span class="font-semibold">Sonnet 4.5</span>
        <span>$3 / $15</span>
      </div>
      <div class="flex justify-between p-2 rounded-lg bg-[var(--ctp-base)]">
        <span class="font-semibold">Haiku 4.5</span>
        <span>$0.25 / $1.25</span>
      </div>
      <div class="mt-2 text-black/50">格式：输入 / 输出</div>
      <div class="text-black/50">Batch API 享 5 折</div>
    </div>
  </div>
</div>

</div>

</div>

---
transition: fade-out
---

## 闭源模型：GPT（OpenAI）

<div class="mt-4 px-4">

<div class="flex gap-6">

<div class="flex-1">

<div v-click class="p-4 mb-4 rounded-xl bg-[var(--ctp-teal)]/10 border-2 border-[var(--ctp-teal)]">
  <div class="text-sm text-black/70 leading-relaxed">CodeX 5.3 相对便宜量大管饱。$20/月 Pro 会员一般足够正常开发需求和接入 OpenClaw 使用，是<strong>性价比最高的闭源方案</strong></div>
</div>

<div v-click>

| 订阅方案 | 月费 | 核心权益 |
|---------|------|---------|
| Free | $0 | GPT-5.2 Instant 基础访问 |
| Go | $8 | 无限 GPT-5.2 Instant |
| Plus | $20 | Thinking 模式，5x 用量 |
| Pro | $200 | 无限 GPT-5.2 Pro + Sora 2 |

</div>

</div>

<div v-click class="w-72 shrink-0">
  <div class="p-4 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
    <div class="text-sm font-semibold mb-3">API 价格（每百万 Token）</div>
    <div class="flex flex-col gap-2 text-xs">
      <div class="flex justify-between p-2 rounded-lg bg-[var(--ctp-base)]">
        <span class="font-semibold">CodeX 5.3</span>
        <span>~$2 / ~$12</span>
      </div>
      <div class="flex justify-between p-2 rounded-lg bg-[var(--ctp-base)]">
        <span class="font-semibold">GPT-5.2</span>
        <span>$1.75 / $14</span>
      </div>
      <div class="flex justify-between p-2 rounded-lg bg-[var(--ctp-base)]">
        <span class="font-semibold">GPT-5 Mini</span>
        <span>$0.25 / $2</span>
      </div>
      <div class="flex justify-between p-2 rounded-lg bg-[var(--ctp-base)]">
        <span class="font-semibold">GPT-5 Nano</span>
        <span>$0.05 / $0.4</span>
      </div>
      <div class="mt-2 text-black/50">格式：输入 / 输出</div>
    </div>
  </div>
</div>

</div>

</div>

---
transition: slide-up
---

## 开源模型：国产三强

<div class="mt-4 px-4">

<div class="grid grid-cols-3 gap-5">

<div v-click class="p-5 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="text-3xl mb-2">🟢</div>
  <div class="font-semibold text-lg mb-1">GLM-5</div>
  <div class="text-xs text-black/50 mb-3">智谱 AI · 744B 参数</div>
  <div class="text-sm text-black/70 leading-relaxed mb-3">大部分日常任务可完成，编码水平弱于 CodeX 5.3 但足够使用</div>
  <div class="p-3 rounded-lg bg-[var(--ctp-base)] text-xs">
    <div class="flex justify-between mb-1"><span>输入</span><span class="font-semibold">$1.00/M</span></div>
    <div class="flex justify-between mb-1"><span>输出</span><span class="font-semibold">$3.20/M</span></div>
    <div class="flex justify-between"><span>订阅</span><span class="font-semibold">¥26-32/月</span></div>
  </div>
</div>

<div v-click class="p-5 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="text-3xl mb-2">🟠</div>
  <div class="font-semibold text-lg mb-1">Qwen 3.5</div>
  <div class="text-xs text-black/50 mb-3">阿里巴巴 · 开源可自部署</div>
  <div class="text-sm text-black/70 leading-relaxed mb-3">性能与 GLM-5 接近，适用于大部分日常任务，价格极具竞争力</div>
  <div class="p-3 rounded-lg bg-[var(--ctp-base)] text-xs">
    <div class="flex justify-between mb-1"><span>输入</span><span class="font-semibold">~$0.11/M</span></div>
    <div class="flex justify-between mb-1"><span>输出</span><span class="font-semibold">~$1.20/M</span></div>
    <div class="flex justify-between"><span>Batch</span><span class="font-semibold">5 折优惠</span></div>
  </div>
</div>

<div v-click class="p-5 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="text-3xl mb-2">🔵</div>
  <div class="font-semibold text-lg mb-1">Kimi 2.5</div>
  <div class="text-xs text-black/50 mb-3">月之暗面 · 极速推理</div>
  <div class="text-sm text-black/70 leading-relaxed mb-3">Turbo 级速度（60-100 tok/s），内置自动缓存，输入成本降低 75%</div>
  <div class="p-3 rounded-lg bg-[var(--ctp-base)] text-xs">
    <div class="flex justify-between mb-1"><span>输入</span><span class="font-semibold">$0.60/M</span></div>
    <div class="flex justify-between mb-1"><span>输出</span><span class="font-semibold">$2.50/M</span></div>
    <div class="flex justify-between"><span>缓存输入</span><span class="font-semibold">$0.15/M</span></div>
  </div>
</div>

</div>

<div v-click class="mt-5 p-4 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center text-sm text-black/60">
  三家最新版本跑分表现接近，但与闭源海外头部模型的<strong>实际体验差距仍然较大</strong>。优势在于<strong>价格低廉</strong>且支持<strong>本地化部署</strong>
</div>

</div>

---
transition: slide-left
---

## 旗舰模型 API 价格对比

<div class="mt-8 px-4">

| 厂商 | 模型 | 输入 $/M | 输出 $/M | 特点 |
|------|------|---------|---------|------|
| Anthropic | Opus 4.6 | $5.00 | $25.00 | 最强能力，价格最高 |
| Anthropic | Sonnet 4.5 | $3.00 | $15.00 | 能力/价格均衡 |
| OpenAI | CodeX 5.3 | ~$2.00 | ~$12.00 | 编程性价比之选 |
| OpenAI | GPT-5.2 | $1.75 | $14.00 | 通用旗舰 |
| 智谱 | GLM-5 | $1.00 | $3.20 | 国产性能最强 |
| 月之暗面 | Kimi 2.5 | $0.60 | $2.50 | 极速推理 |
| 阿里 | Qwen 3.5+ | $0.11 | $1.20 | 价格最低 |

</div>

---
transition: fade
---

## 选型建议

<div class="mt-12 flex justify-center gap-8">

<v-click>

<div class="w-56 p-6 rounded-xl bg-[var(--ctp-lavender)]/10 border-2 border-[var(--ctp-lavender)] text-center">
  <div class="text-4xl mb-3">👑</div>
  <div class="font-semibold text-lg mb-2">追求极致能力</div>
  <div class="text-sm text-black/60">Claude Opus 4.6</div>
  <div class="text-xs text-black/40 mt-2">Max $200/月</div>
</div>

</v-click>

<v-click>

<div class="w-56 p-6 rounded-xl bg-[var(--ctp-teal)]/10 border-2 border-[var(--ctp-teal)] text-center">
  <div class="text-4xl mb-3">⚖️</div>
  <div class="font-semibold text-lg mb-2">编程性价比</div>
  <div class="text-sm text-black/60">CodeX 5.3</div>
  <div class="text-xs text-black/40 mt-2">Plus $20/月</div>
</div>

</v-click>

<v-click>

<div class="w-56 p-6 rounded-xl bg-[var(--ctp-peach)]/10 border-2 border-[var(--ctp-peach)] text-center">
  <div class="text-4xl mb-3">🏠</div>
  <div class="font-semibold text-lg mb-2">低成本 + 本地部署</div>
  <div class="text-sm text-black/60">Qwen 3.5 / GLM-5</div>
  <div class="text-xs text-black/40 mt-2">API 按量计费或自部署</div>
</div>

</v-click>

</div>
