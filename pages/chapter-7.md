---
transition: fade-out
---

# 第七节：Token 优势 — 消灭谷电

<div class="mt-10 px-8">

<div class="flex items-center justify-center gap-10">

<div v-click class="w-64 p-6 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center">
  <div class="text-4xl mb-3">🏭</div>
  <div class="font-semibold text-lg mb-2">AI 数据中心</div>
  <div class="text-sm text-black/60">7×24 小时不间断运行的<br/>"电力巨兽"</div>
</div>

<div v-click class="text-4xl text-black/30">+</div>

<div v-click class="w-64 p-6 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center">
  <div class="text-4xl mb-3">📉</div>
  <div class="font-semibold text-lg mb-2">谷电难题</div>
  <div class="text-sm text-black/60">夜间和非高峰时段的<br/>低谷用电是电网运营痛点</div>
</div>

<div v-click class="text-4xl text-black/30">=</div>

<div v-click class="w-64 p-6 rounded-xl border-2 border-[var(--ctp-lavender)] text-center" style="background-color: rgba(114,135,253,0.1);">
  <div class="text-4xl mb-3">⚡</div>
  <div class="font-semibold text-lg mb-2">天然互补</div>
  <div class="text-sm text-black/60">AI 算力需求恰好<br/>填平电力负荷曲线</div>
</div>

</div>

</div>

---
transition: slide-up
---

## AI 数据中心与 Agent 的负载特征

<div class="mt-6 px-6">

<div class="grid grid-cols-2 gap-5">

<div v-click class="p-5 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="flex items-center gap-2 mb-2">
    <div class="text-2xl">🔄</div>
    <div class="font-semibold text-base">持续满载运行</div>
  </div>
  <div class="text-sm text-black/70 leading-relaxed">AI 数据中心 7×24 小时持续满载运行，没有"工作日/休息日"之分，GPU 集群一旦启动便不间断地进行训练和推理</div>
</div>

<div v-click class="p-5 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="flex items-center gap-2 mb-2">
    <div class="text-2xl">🌍</div>
    <div class="font-semibold text-base">Agent 负载更均匀</div>
  </div>
  <div class="text-sm text-black/70 leading-relaxed">全球用户分布在不同时区，Agent 任务可以异步执行。当北美深夜时，亚洲正值工作高峰，负载曲线天然被全球化拉平</div>
</div>

</div>

<div v-click class="mt-5 p-5 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="flex items-center gap-2 mb-2">
    <div class="text-2xl">🌐</div>
    <div class="font-semibold text-base">电力通过算力走向全球 — 中东数据中心的启示</div>
  </div>
  <div class="text-sm text-black/70 leading-relaxed">中东大规模建设 AI 数据中心，核心原因是拥有极其廉价的电力（天然气和光伏）。过去电力传输限于电线，现在<strong>电力可以就地转化为算力，通过网络即时出售到全球</strong>。本次伊朗导弹袭击就导致美国 Claude Code 模型后端服务中断半天 —— 证明算力基础设施已成为地缘战略资源</div>
</div>

</div>

---
transition: slide-left
---

## GPU 功耗与算力需求的飙升

<div class="mt-6 px-4">

<div v-click class="mb-6">

<div class="text-sm font-semibold mb-3">单 GPU 功耗演进（TDP）</div>

<div class="flex items-end justify-center gap-4">

<div class="text-center">
  <div class="w-20 bg-[var(--ctp-teal)] rounded-t-lg flex items-end justify-center text-white text-xs font-bold" style="height: 90px;">700W</div>
  <div class="text-xs text-black/60 mt-2">H100<br/>2023</div>
</div>

<div class="text-center">
  <div class="w-20 bg-[var(--ctp-blue)] rounded-t-lg flex items-end justify-center text-white text-xs font-bold" style="height: 130px;">1000W</div>
  <div class="text-xs text-black/60 mt-2">B200<br/>2024</div>
</div>

<div class="text-center">
  <div class="w-20 bg-[var(--ctp-mauve)] rounded-t-lg flex items-end justify-center text-white text-xs font-bold" style="height: 155px;">1200W</div>
  <div class="text-xs text-black/60 mt-2">GB200<br/>2025</div>
</div>

<div class="text-center">
  <div class="w-20 bg-[var(--ctp-red)] rounded-t-lg flex items-end justify-center text-white text-xs font-bold" style="height: 200px;">2300W</div>
  <div class="text-xs text-black/60 mt-2">Vera Rubin<br/>2026 H2</div>
</div>

</div>

</div>

<div v-click class="p-4 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="flex items-start gap-3">
    <div class="text-2xl shrink-0">📊</div>
    <div>
      <div class="font-semibold text-sm mb-1">大摩预测 & 黄仁勋展望</div>
      <div class="text-xs text-black/70 leading-relaxed">摩根士丹利预测仅英伟达平台，AI 服务器机柜需求将从 2025 年约 <strong>2.8 万台</strong>跃升至 2026 年至少 <strong>6 万台</strong>。CES 2026 上黄仁勋表示：五年内算力翻 <strong>100 倍</strong>，而对算力的需求将<strong>远超硬件性能增长</strong></div>
    </div>
  </div>
</div>

</div>

---
transition: fade
---

## Token 经济 = 持续电力需求

<div class="mt-8 px-6">

<div v-click class="flex items-center gap-3 mb-4 p-4 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="text-2xl shrink-0">⚙️</div>
  <div>
    <div class="text-sm font-semibold">每一个 Token = GPU 持续运算 = 持续耗电</div>
    <div class="text-xs text-black/70 mt-0.5">Token 不是存储在数据库里的数字，而是 GPU 实时推理计算的产物，消耗的是真实的电力</div>
  </div>
</div>

<div v-click class="flex items-center gap-3 mb-4 p-4 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="text-2xl shrink-0">📈</div>
  <div>
    <div class="text-sm font-semibold">Agent 爆发推动 Token 消耗量级跃迁</div>
    <div class="text-xs text-black/70 mt-0.5">从普通对话的"百万"级，到 Agent 工作流的"十亿"甚至"万亿"级，Token 消耗呈指数增长</div>
  </div>
</div>

<div v-click class="flex items-center gap-3 mb-6 p-4 rounded-xl border-2 border-[var(--ctp-lavender)]" style="background-color: rgba(114,135,253,0.1);">
  <div class="text-2xl shrink-0">🔋</div>
  <div>
    <div class="text-sm font-semibold">谷电时段不再"谷"</div>
    <div class="text-xs text-black/70 mt-0.5">AI 负载天然填平电力需求曲线，传统电网中难以消纳的低谷电力，成为算力经济的核心能源</div>
  </div>
</div>

<div v-click class="text-center">
  <div class="text-lg font-semibold mb-2">对电力行业的核心意义</div>
  <div class="text-sm text-black/60 max-w-xl mx-auto leading-relaxed">AI Agent 时代的到来，意味着电力不再只是照明和驱动机器的能源，而是成为<strong>全球算力经济的底层燃料</strong>。谁掌握了低成本电力，谁就掌握了 AI 时代的核心竞争力</div>
</div>

</div>
