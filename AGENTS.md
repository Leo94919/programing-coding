# AGENTS.md

- 回應一律使用繁體中文。
- 專案語言為 Python；一律使用 conda 管理套件，環境名稱為 `iem_python`（已驗證 Python 3.12.13）。
- Greenfield repo：僅有 `README.md`（placeholder）與 Python 版 `.gitignore`，尚無 manifests、lockfiles、CI、lint/test 設定或進入點。

## Conda

- 本機 `conda` 不在 PATH，完整路徑為 `C:\Users\user\anaconda3\Scripts\conda.exe`；PowerShell 需用 `& <完整路徑>` 呼叫。
- 非互動 shell（OpenCode `shell`）優先使用免 activate 寫法：
  - 執行：`conda run -n iem_python python <script.py>`
  - 安裝套件：`conda install -n iem_python <pkg>`；conda 無此套件時才用 `conda run -n iem_python pip install <pkg>`
- 互動開發才用 `conda activate iem_python`。
- 新增 build/test/lint 流程前，先確認實際新增的設定檔，並將確切指令補回此檔。
