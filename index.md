---
layout: default
---

# 📰 AI 每日简报

每日自动抓取大模型（LLM）、智能体（Agent）领域的核心动态、技术进展、行业热点与前沿论文。

## 📅 按日期查看
<div id="calendar-container" style="max-width: 600px; margin: 2rem auto; padding: 1rem; border-radius: 8px; background: var(--bg-color, #fff); box-shadow: 0 2px 8px rgba(0,0,0,0.1);"></div>

## 📋 历史报告列表
- [2026年03月19日](2026-03-19.md)

---
✨ 本报告每日20:00自动更新，由 [OpenClaw](https://github.com/openclaw/openclaw) 智能生成。

<script src="https://cdn.jsdelivr.net/npm/vanilla-calendar-pro@2.9.6/build/vanilla-calendar.min.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/vanilla-calendar-pro@2.9.6/build/vanilla-calendar.min.css">

<script>
document.addEventListener('DOMContentLoaded', () => {
  const calendar = new VanillaCalendar('#calendar-container', {
    settings: {
      selection: {
        day: 'single',
      },
      visibility: {
        weekend: true,
        daysOutside: false,
      },
      lang: 'zh-CN',
    },
    actions: {
      clickDay(e, dates) {
        const selectedDate = dates[0];
        const dateStr = selectedDate.replace(/\//g, '-');
        const reportUrl = `/${dateStr}.md`;
        // 检查文件是否存在
        fetch(reportUrl)
          .then(res => {
            if (res.ok) {
              window.location.href = reportUrl;
            } else {
              alert('该日期暂无报告哦~');
            }
          })
          .catch(() => alert('该日期暂无报告哦~'));
      }
    }
  });
  calendar.init();
});
</script>
