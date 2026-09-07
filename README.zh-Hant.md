![Team Leader：給 AI 項目配一位負責人，帶領團隊朝正確的方向前進](assets/cover.zh-hant.svg)

[English](README.md) · [繁體中文](README.zh-Hant.md) · [简体中文](README.zh-CN.md)

**Codex · Astra** ｜ **v0.5.16** ｜ **MIT**

[快速上手](#start) · [設計原理](#loop) · [崗位分工](#roles) · [使用反饋](#feedback) · [下載完整 Skill](https://github.com/aidesign996/team-leader/releases/download/team-leader-v0.5.16/team-leader-0.5.16.zip)

**做 AI 項目時，你是否還要反覆提醒目標、檢查結果，再催下一步？**

我設計了 Team Leader，把持續協調項目這件事交給一位職責明確的 AI 負責人：它圍繞你的目標安排專業崗位，檢查做出來的結果，並組織修正。已經確認的需求、決定和進度則保存到項目文件中，方便後續接著做。

它面向需要持續迭代、跨產品設計、技術設計、開發和驗證的項目。希望減少使用者反覆轉述和協調的負擔；實際效果仍需要更多場景驗證。

<a id="start"></a>

## 兩步開始使用

**1. 把這句話交給能夠聯網和安裝 Skill 的 AI 工具：**

> 請閱讀 <https://github.com/aidesign996/team-leader>，幫我安裝其中完整的 Team Leader Skill。

**2. 安裝後，在項目對話中選中 Team Leader，或點名 `$team-leader`，然後說：**

> 接下來這個項目由你負責，你跟進一下。

按照這套方法，負責人應先讀取現有資料和目標；缺少關鍵需求時主動問你，明確後繼續推進。你可以像向團隊負責人交代工作一樣，逐步補充想法。首次選中 Skill 很重要，短句本身不保證所有工具都能自動發現技能。

希望採用團隊模式時，再補一句：“請為這個項目建立完整團隊，由你負責協調。”實際建隊取決於工具支持和你的授權，已有崗位會複用。

<details>
<summary>工具不能直接安裝？查看手動安裝方法</summary>

1. [下載完整 ZIP](https://github.com/aidesign996/team-leader/releases/download/team-leader-v0.5.16/team-leader-0.5.16.zip)並解壓。
2. 將完整的 `team-leader` 文件夾放到個人 `~/.agents/skills/`，或項目的 `.agents/skills/` 中。完整包共22個文件，包含 MIT 許可，不要只複製 `SKILL.md`。
3. 在新項目對話中確認能讀取 Skill；若未發現，重啟 Codex。升級前備份已有自定義修改，並保留項目記錄。

</details>

<a id="loop"></a>

## 它怎樣帶隊：目標、反饋、行動

設計受到《系統之美》的調節反饋啟發：用戶確定目標，負責人觀察結果並判斷差距，專業崗位據此行動，再把新的結果帶回檢查。

<p align="center"><img src="assets/loop.zh-hant.png" width="470" alt="目標輸入負責人，負責人對照項目成果判斷差距，再協調專業崗位更新成果。"></p>

負責人既要安排誰來做，也要持續判斷“這輪工作有沒有讓項目更接近目標”。早期可以探索多個方案，進入實現時再依據目標與約束收斂。新增負責人並不自動保證穩定，觀察質量、反饋及時性和修正落實同樣重要。

<a id="roles"></a>

## 一個負責人，五類專業職責

| 角色 | 負責什麼 |
| --- | --- |
| **0 · 團隊負責人** | 維護目標，安排工作，檢查差距並協調交付。 |
| **1 · 環境配置** | 準備和檢查可復現的工作條件。 |
| **2 · 產品設計** | 明確需求、使用流程與體驗。 |
| **3 · 技術設計** | 設計架構、接口和實現邊界。 |
| **4 · 開發** | 實現、自查與修正。 |
| **5 · 獨立 AI 驗收** | 由未參與該項製作的角色檢查結果。 |

0.5.16 在採用團隊模式且獲得授權後補齊六類職責；每輪按任務需要調動相關崗位。負責人還會組織項目文檔，讓需求、產品方案、技術方案、進度和經驗各有可查找的位置。記錄需要在後續任務中主動讀取和應用，保存文件本身不等於自動記住。

<a id="fit"></a>

## 適用範圍與投入

- **主要設計對象是 Codex 中的 Astra。** Sol 有部分專業崗位實踐，尚無同條件下完整 Sol 團隊的效果結論。
- **可能消耗較多額度。** 負責人通常從 XHigh 起步，按任務安排專業崗位推理級別，並在工具支持時整理上下文；實際設置遵循用戶偏好和工具能力。
- **簡單任務可以保持單人。** 當前已檢查包完整性、乾淨目錄解壓與基礎結構；新賬號完整首次運行、長期自主糾偏和節省額度尚未系統驗證。

[閱讀完整設計文章（GitHub）](https://github.com/aidesign996/ai-practice/blob/main/docs/team-leader/ARTICLE.zh-Hant.md) · [查看版本說明與校驗文件](https://github.com/aidesign996/team-leader/releases/tag/team-leader-v0.5.16)

<a id="feedback"></a>

## 歡迎把工作中遇到的問題帶回來

**不需要先寫一份規範報告，一條留言說清楚就好：** 你在做什麼、它實際怎樣處理、你希望怎樣處理會更好。模型和輸出片段有助於理解問題，分享前可去掉私人信息。

例如：“我讓負責人接手一個已有項目，它重新擬了計劃，卻沒接著做上一輪未完成的事。我更希望它先找到繼續點，完成後再提出調整。”這是說明反饋方式的假設場景。

[查看 GitHub 公開討論](https://github.com/aidesign996/ai-practice/discussions/1) · [在現有共享評論區留言](https://aidesign996.github.io/ai-practice/article-team-leader.zh-hant.html#comments)

網站英文、繁體、簡體版本共用同一討論映射，留言以原語言公開顯示。我會結合真實場景整理反饋，改進方法，並在後續版本說明裡交代已做的調整。

---

Team Leader Skill 採用 [MIT 許可](team-leader/LICENSE)，署名 AI Design 996。文章與配圖單獨提供。[設計參考](https://github.com/aidesign996/ai-practice/blob/main/SOURCES.md)
