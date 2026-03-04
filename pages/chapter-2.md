---
transition: fade-out
---

# 第二节：OpenClaw（龙虾）是什么

<div class="flex items-center justify-center gap-12 mt-12">

<div v-click class="text-left max-w-sm">
  <p class="text-lg leading-relaxed">
    OpenClaw 是一个<strong>免费开源</strong>的自主 AI Agent，由奥地利开发者 <strong>Peter Steinberger</strong> 于 2025 年 11 月创建。
  </p>
  <p class="text-sm text-black/50 mt-4">
    最初名为 Clawdbot → 因 Anthropic 商标投诉更名为 Moltbot → 最终定名 OpenClaw
  </p>
</div>

<img v-click src="/images/openclaw.svg" class="h-40 rounded-xl" alt="OpenClaw" />

</div>

---
transition: slide-up
---

## 产品定义

<div class="flex gap-10 mt-8 px-4">

<div class="flex-1">

<v-click>

<div class="p-5 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] mb-6">
  <div class="font-semibold text-lg mb-2">自主执行的 AI Agent</div>
  <div class="text-sm text-black/70 leading-relaxed">
    能够自主执行指令、与应用程序交互并完成任务，<strong>无需持续人工监督</strong>。与传统聊天机器人只生成文本回复不同，它可以在用户自己的电脑或服务器上<strong>本地运行</strong>，连接外部工具和应用。
  </div>
</div>

</v-click>

<v-click>

<div class="p-5 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)]">
  <div class="font-semibold text-lg mb-3">多平台消息交互</div>
  <div class="flex flex-wrap gap-3 text-sm">
    <span class="px-3 py-1 rounded-full bg-[var(--ctp-surface0)]">WhatsApp</span>
    <span class="px-3 py-1 rounded-full bg-[var(--ctp-surface0)]">Telegram</span>
    <span class="px-3 py-1 rounded-full bg-[var(--ctp-surface0)]">Slack</span>
    <span class="px-3 py-1 rounded-full bg-[var(--ctp-surface0)]">Discord</span>
    <span class="px-3 py-1 rounded-full bg-[var(--ctp-surface0)]">飞书</span>
    <span class="px-3 py-1 rounded-full bg-[var(--ctp-surface0)]">更多...</span>
  </div>
</div>

</v-click>

</div>

<div v-click class="flex flex-col items-center justify-center w-48">
  <div class="text-6xl">🦞</div>
  <div class="mt-3 text-center">
    <div class="text-sm font-semibold">太空龙虾</div>
    <div class="text-xs text-black/50">Space Lobster</div>
  </div>
</div>

</div>

---
transition: fade
---

## 整体架构

<div class="mt-8 flex items-center justify-center gap-6">

<div v-click class="px-8 py-6 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center">
  <div class="text-4xl">📱</div>
  <div class="text-base font-semibold mt-2">消息平台</div>
  <div class="text-xs text-black/50 mt-1">WhatsApp / Telegram / Slack ...</div>
</div>

<div v-click class="text-4xl text-black/40">→</div>

<div v-click class="px-8 py-6 rounded-xl bg-[var(--ctp-lavender)]/15 border-2 border-[var(--ctp-lavender)] text-center">
  <div class="text-4xl">🖥️</div>
  <div class="text-base font-semibold mt-2">Gateway</div>
  <div class="text-xs text-black/50 mt-1">本地控制平面</div>
</div>

<div v-click class="text-4xl text-black/40">→</div>

<div v-click class="flex flex-col gap-4">

  <div class="px-8 py-4 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center">
    <div class="text-2xl">🧠</div>
    <div class="text-sm font-semibold mt-1">LLM API</div>
  </div>

  <div class="px-8 py-4 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center">
    <div class="text-2xl">🧩</div>
    <div class="text-sm font-semibold mt-1">Skills 技能</div>
  </div>

  <div class="px-8 py-4 rounded-xl bg-[var(--ctp-mantle)] border border-[var(--ctp-surface0)] text-center">
    <div class="text-2xl">💾</div>
    <div class="text-sm font-semibold mt-1">Memory 记忆</div>
  </div>

</div>

</div>
