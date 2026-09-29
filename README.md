# 全靜脈營養會診處方試算

成人住院病人的單頁、離線可用試算工具。開啟 `index.html` 即可使用；不需要安裝套件或建立伺服器。

## 操作

1. 輸入體重、身高、臨床狀態及口服／腸道既有攝取。熱量、蛋白質、液體係數可調。
2. 確認輸注途徑、液體上限及臨床警示；檢視每袋配方與待補需求。
3. 選擇液袋、完整袋數、Moriamin-SN 瓶數及輸注時數，檢查覆蓋率、液體與速率警示。
4. 編輯會診草稿，使用「複製回覆」、「匯出 Word」或「列印／存 PDF」。Word 輸出為可由 Word 開啟的 `.doc` HTML 文件。

預設內含 SMOFKabiven Central 1477 mL、SMOFKabiven Peripheral 1448 mL、OliClinomel N4-550E 1500 mL；Addaven、Lyo-Povigent、Moriamin-SN 作為添加／補充項目。按「載入示例」可使用沒有姓名與病歷號的假資料演練。

## 院內校正

在頁面左下展開「院內配方資料（可校正）」可逐欄更改每袋容量、熱量、胺基酸、葡萄糖、脂肪及 Na/K/Mg/P。變更只在目前頁面有效；重新整理會回到預置數值。正式使用前，請由營養科與藥劑科對照院內採購品項、許可證與藥袋標籤確認。若改變濃度或品項，程式內的標示每日與每小時限值也需另行校訂。

## 重要計算範圍

- 需求估算採指定體重 × 可調係數；BMI ≥30 且已填身高和性別時，預設使用 Devine 理想體重加 40% 超額體重。特殊族群可手動輸入估算體重。
- 先扣除口服／腸道熱量和蛋白，以及其他葡萄糖熱量；液體可用量扣除其他輸液與選填上限。
- Moriamin-SN 10% 200 mL 以胺基酸 20 g、約 80 kcal 計；藥師須評估併用方式、安定性和通路。
- 固定液袋成分不能保證同時符合熱量、蛋白及電解質需求。警示依輸入資料觸發，不等於禁忌、相容性或最終醫囑判定。未計入丙泊酚熱量、檸檬酸、藥物稀釋液、維生素添加體積、液袋外補充電解質等，應輸入「其他」欄並逐案覆核。
- 僅供成人。復食風險、重症、肥胖、肝腎衰竭與透析病人的係數和進展速度需個別化；開始 TPN 前確認適應症與可用腸道途徑。
- 病人資料只在當前瀏覽器記憶體中運算，沒有後端或自動儲存。若部署到公開網站，仍須遵守院內資訊安全規範，避免在不受管控裝置上處理可識別病人資料。

## 來源與預置配方

| 品項 | 每袋熱量 / 胺基酸 / 葡萄糖 / 脂肪 | 來源 |
| --- | --- | --- |
| SMOFKabiven Central 1477 mL | 約 1600 kcal / 75 g / 187 g / 56 g | [台灣仿單](https://www1.ndmctsgh.edu.tw/pharm/pic/medinsert/005SMO05.pdf) |
| SMOFKabiven Peripheral 1448 mL | 約 1000 kcal / 46 g / 103 g / 41 g | [產品資料](https://fass.se/health/product/20051112000055/smpc) |
| OliClinomel N4-550E 1500 mL | 約 910 kcal / 33 g / 120 g / 30 g | [台灣仿單](https://mcp.fda.gov.tw/insert/pdfcasefile/i_d4e15e56-d162-43eb-b93b-e9ec9c8a4d0a?c=2) |

[Addaven 仿單](https://www1.ndmctsgh.edu.tw/pharm/pic/medinsert/005ADD01.pdf) · [Lyo-Povigent 仿單](https://www1.ndmctsgh.edu.tw/pharm/pic/medinsert/005LYO03.pdf) · [Moriamin-SN 仿單](https://www1.ndmctsgh.edu.tw/pharm/pic/medinsert/005MOR06.pdf) · [ESPEN 2023 ICU 營養實用指引](https://www.espen.org/files/ESPEN-Guidelines/ESPEN_practical_and_partially_revised_guideline_Clinical_nutrition_in_the_intensive_care_unit.pdf)

## 部署到 GitHub Pages

建立 repository，將 `index.html` 放在根目錄（README 可一併上傳），於 repository 的 **Settings → Pages → Build and deployment** 選擇 **Deploy from a branch**、`main`、`/ (root)`。如果處理可識別病人資料，先由院方資訊安全單位確認可使用的部署與終端環境。
