---
transition: fade-out
---

# 第六节：Agent 对 Token 的需求远超普通 AI 对话

<div class="mt-12 flex items-center justify-center gap-12">

<div v-click class="w-64 p-6 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center">
  <div class="text-4xl mb-3">💬</div>
  <div class="font-semibold text-lg mb-2">普通 AI 对话</div>
  <div class="text-sm text-black/60">一问一答<br/>每轮消耗几百~几千 Token</div>
</div>

<div v-click class="text-4xl text-black/30">vs</div>

<div v-click class="w-64 p-6 rounded-xl bg-[var(--ctp-lavender)]/10 border-2 border-[var(--ctp-lavender)] text-center">
  <div class="text-4xl mb-3">🤖</div>
  <div class="font-semibold text-lg mb-2">自主 AI Agent</div>
  <div class="text-sm text-black/60">数十轮内部推理 + 工具调用<br/>Token 消耗呈几何级增长</div>
</div>

</div>

---
transition: slide-up
---

## Token 消耗量对比

<div class="mt-8 px-6">

<div class="grid grid-cols-3 gap-6">

<div v-click class="p-6 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center">
  <div class="text-4xl mb-3">📞</div>
  <div class="text-sm text-black/50 mb-2">普通客服对话</div>
  <div class="text-3xl font-bold text-[var(--ctp-teal)]">500 - 2K</div>
  <div class="text-sm text-black/50 mt-1">Token / 次</div>
</div>

<div v-click class="p-6 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center">
  <div class="text-4xl mb-3">⚙️</div>
  <div class="text-sm text-black/50 mb-2">Agent 复杂工作流</div>
  <div class="text-3xl font-bold text-[var(--ctp-peach)]">5,000+</div>
  <div class="text-sm text-black/50 mt-1">Token / 次交互</div>
</div>

<div v-click class="p-6 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center">
  <div class="text-4xl mb-3">🔬</div>
  <div class="text-sm text-black/50 mb-2">Anthropic 案例研究</div>
  <div class="text-3xl font-bold text-[var(--ctp-red)]">~150K</div>
  <div class="text-sm text-black/50 mt-1">Token / 单任务（优化前）</div>
</div>

</div>

<div v-click class="mt-6 p-4 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center text-sm text-black/60">
  Anthropic 案例中，标准方法单任务需约 <strong>15 万</strong> Token，优化后仅需约 <strong>2,000</strong> Token —— 相差 <strong>75 倍</strong>，可见原始消耗之巨大
</div>

</div>

---
transition: slide-left
---

## 为什么 Agent 如此"吃" Token？

<div class="mt-4 px-6">

<div v-click class="flex items-center gap-3 mb-3 p-3 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="text-2xl shrink-0">📦</div>
  <div>
    <div class="text-sm font-semibold">每次调用的上下文负载</div>
    <div class="text-xs text-black/70 mt-0.5">系统提示词 + 用户消息 + 历史记忆 + 工具定义，每次 API 调用都要<strong>全量发送</strong>，Token 随上下文积累不断膨胀</div>
  </div>
</div>

<div v-click class="flex items-center gap-3 mb-3 p-3 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="text-2xl shrink-0">🔄</div>
  <div>
    <div class="text-sm font-semibold">自主推理循环</div>
    <div class="text-xs text-black/70 mt-0.5">思考 → 调用工具 → 获取结果 → 再思考 → 再调用…… 一个任务可能<strong>循环数十次</strong>，每轮都在消耗 Token</div>
  </div>
</div>

<div v-click class="flex items-center gap-3 mb-3 p-3 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="text-2xl shrink-0">💾</div>
  <div>
    <div class="text-sm font-semibold">长期记忆检索</div>
    <div class="text-xs text-black/70 mt-0.5">每次决策前搜索并加载记忆文件，将历史上下文注入当前会话，进一步增加输入 Token 量</div>
  </div>
</div>

<div v-click class="flex items-center gap-3 p-3 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="text-2xl shrink-0">🔗</div>
  <div>
    <div class="text-sm font-semibold">多技能链式调用</div>
    <div class="text-xs text-black/70 mt-0.5">复杂任务串联调用多个 Skill，每个结果作为下一步输入，形成<strong>Token 消耗链</strong></div>
  </div>
</div>

</div>

---
transition: fade-out
---

## 一个形象的类比

<div class="mt-12 flex items-center justify-center gap-10">

<v-click>

<div class="w-72 p-8 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center">
  <div class="text-5xl mb-4">📞</div>
  <div class="font-semibold text-xl mb-3">普通 AI 聊天</div>
  <div class="text-base text-black/60 leading-relaxed">像<strong>打个电话</strong></div>
  <div class="text-sm text-black/40 mt-3">说完即挂，按分钟计费</div>
</div>

</v-click>

<v-click>

<div class="text-4xl text-black/30">→</div>

</v-click>

<v-click>

<div class="w-72 p-8 rounded-xl bg-[var(--ctp-lavender)]/10 border-2 border-[var(--ctp-lavender)] text-center">
  <div class="text-5xl mb-4">👨‍💼</div>
  <div class="font-semibold text-xl mb-3">AI Agent</div>
  <div class="text-base text-black/60 leading-relaxed">像<strong>雇了一个 24h 在线的员工</strong></div>
  <div class="text-sm text-black/40 mt-3">持续思考、持续执行、持续消耗</div>
</div>

</v-click>

</div>

<div v-click class="mt-10 text-center text-lg text-black/50">
  "电话费" 和 "员工薪资" 不可同日而语
</div>

---
transition: slide-up
---

## 商业机遇：行业垂直模型的本地化部署

<div class="mt-2 px-4">

<div v-click class="p-3 mb-3 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="flex items-center gap-2">
    <div class="text-xl shrink-0">💡</div>
    <div class="text-xs text-black/70 leading-relaxed">当前 Token 价格昂贵，闲鱼平台已有个人用 4090 部署开源模型出售算力的盈利案例，揭示了潜在的商业模式</div>
  </div>
</div>

<div class="grid grid-cols-2 gap-3">

<div v-click class="p-3 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="flex items-center gap-2 mb-1">
    <div class="text-xl">⚡</div>
    <div class="font-semibold text-sm">电力行业</div>
  </div>
  <div class="text-xs text-black/70">电网运行数据、设备参数等敏感数据不宜上云，适合行业数据微调后本地部署</div>
</div>

<div v-click class="p-3 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="flex items-center gap-2 mb-1">
    <div class="text-xl">🏥</div>
    <div class="font-semibold text-sm">医疗行业</div>
  </div>
  <div class="text-xs text-black/70">患者病历等隐私数据受严格监管，本地部署可满足合规并提供 AI 辅助能力</div>
</div>

<div v-click class="p-3 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="flex items-center gap-2 mb-1">
    <div class="text-xl">🏭</div>
    <div class="font-semibold text-sm">工业制造</div>
  </div>
  <div class="text-xs text-black/70">生产工艺参数、质检数据需严格保密，本地模型可嵌入产线控制系统</div>
</div>

<div v-click class="p-3 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="flex items-center gap-2 mb-1">
    <div class="text-xl">🏛️</div>
    <div class="font-semibold text-sm">政务与金融</div>
  </div>
  <div class="text-xs text-black/70">信创与国产化要求下，本地部署国产开源模型契合政策导向</div>
</div>

</div>

<div v-click class="mt-3 p-3 rounded-xl bg-[var(--ctp-lavender)]/10 border-2 border-[var(--ctp-lavender)] text-center text-xs leading-relaxed">
  <strong>商业模式</strong>：行业数据微调开源大模型 → 本地化部署为垂直模型 → 以算力服务形式出售 Token 额度
</div>

</div>
