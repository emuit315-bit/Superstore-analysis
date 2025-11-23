
# 🧩 Complete Setup Guide (Anaconda + VS Code + GitHub Desktop + Git)  

**!!!! note that the code you paste in is b/n bash and ```. ok do not put ``` in to the code. you can also put all this into copilot so it can help you everystep of the way.** !!!!!!

## Step 1 — Install Required Tools
- Install **Anaconda**
- Install **GitHub Desktop**
- Install **VS Code** (+ extensions: Python, Jupyter, Pylance)
- Install **Git** (from [git-scm.com](https://git-scm.com/downloads))

---

## Step 2 — Verify Git Installation
Open **Command Prompt** or **Anaconda Prompt** and type:
```bash
git --version
```
You should see something like:
```
git version 2.52.0
```

---

## Step 3 — Clone Repository
- Open **GitHub Desktop**
- Clone repo:
  ```bash
  https://github.com/emuit315-bit/Superstore-analysis.git
  ```
- Save in:
  ```
  C:\Users\<YourName>\Downloads\Intro_grp_assign\Superstore-analysis
  ```

---

## Step 4 — Add Dataset File
Inside your cloned repo folder, ensure you have:
```
Superstore-analysis/
└── data/
    └── Superstore.csv
```
✅ This dataset is required for notebooks to run.

---

## Step 5 — Create Python Environment (Command Line Method — Recommended)
In **Anaconda Prompt**:
```bash
conda create -n superstore python=3.14
conda activate superstore
```
Install libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter statsmodels
```

---

## Step 6 — Optional: Create Environment in Anaconda Navigator (GUI Method)
If teammates prefer a graphical interface:
1. Open **Anaconda Navigator**
2. Go to the **Environments tab → Create**
3. Name: `superstore`
4. Python version: `3.14`
5. Add packages: `pandas, numpy, matplotlib, seaborn, scikit-learn, jupyter, statsmodels`
6. In the **Home tab**, select the `superstore` environment and launch **VS Code** or **Jupyter Notebook** directly.

**Why this is not mandatory:**
- Navigator is just a GUI wrapper for the same commands.
- Using the command line ensures **everyone runs identical reproducible steps** (important for team projects).
- Navigator is optional for teammates who dislike the command line.

---

## Step 7 — Link Git to VS Code
1. Open **VS Code**
2. Go to **View → Source Control** (branch icon on sidebar)
3. Open folder: `File → Open Folder → Superstore-analysis`
4. Git controls (commit, push, pull) should appear

---

## Step 8 — Set VS Code as External Editor in GitHub Desktop
1. In **GitHub Desktop**, go to:  
   **File → Options → Integrations**
2. Under **External Editor**, select **Visual Studio Code**.
   - If VS Code doesn’t appear, click **Browse…** and select:
     ```
     C:\Users\<YourName>\AppData\Local\Programs\Microsoft VS Code\Code.exe
     ```
3. Now you’ll see **“Open in Visual Studio Code”** in the repo menu.
   - If you prefer, you can always open the folder manually in VS Code (`File → Open Folder → Superstore-analysis`).

---

## Step 9 — Confirm Anaconda Environment in VS Code
1. Open **VS Code**
2. Command Palette (`Ctrl+Shift+P`) → `Python: Select Interpreter`
3. Choose:
   ```
   Python (superstore)
   ```
4. If missing, register it:
   ```bash
   conda activate superstore
   python -m ipykernel install --user --name=superstore --display-name "Python (superstore)"
   ```
   Restart VS Code.

---

## Step 10 — Folder Structure (Outputs Included)
```
Superstore-analysis/
│
├── data/
│   └── Superstore.csv
│
├── notebooks/
│   ├── analysis_superstore_<name>.ipynb   # Each teammate creates their own notebook
│
├── visuals/        # Save charts, plots, and figures here
├── report/         # Final written report (Word/PDF)
├── slides/         # Presentation slides (PowerPoint/Google Slides)
│
├── README.md
└── download_data
```

---

## Step 11 — Create Notebook
1. In VS Code, right‑click the `notebooks` folder → **New File**
2. Name it:
   ```
   analysis_superstore_<name>.ipynb
   ```
   (replace `<name>` with your identifier)
3. Open the notebook → select kernel **Python (superstore)**
4. Start coding:
   ```python
   import pandas as pd
   df = pd.read_csv("../data/Superstore.csv", encoding="latin1")
   df.head()
   ```
5. **Keyboard shortcuts:**
   - Run code cell → **Shift + Enter**
   - Save notebook → **Ctrl + S**

---

## Step 12 — Test Everything
1. Save your notebook
2. Commit changes in GitHub Desktop with a clear message
3. Push origin
4. Verify notebook appears on GitHub.com

---

## Extra Info — Git Prompt Commands (Optional)
You don’t need these for daily work (GitHub Desktop + VS Code is enough), but the Git Prompt gives you **manual control** if the GUI misbehaves or for advanced fixes.

- Check Git installation
  ```bash
  git --version
  ```
- Clone a repo
  ```bash
  git clone https://github.com/emuit315-bit/Superstore-analysis.git
  ```
- Check repo status
  ```bash
  git status
  ```
- Stage changes
  ```bash
  git add .
  ```
- Commit changes
  ```bash
  git commit -m "Added analysis_superstore_<name>.ipynb"
  ```
- Push to GitHub
  ```bash
  git push origin main
  ```
- Pull updates from teammates
  ```bash
  git pull origin main
  ```

**Note:** This section is **extra info only**. Use GitHub Desktop for everyday commits/pushes. The Git Prompt is your backup tool when you need full control.
```

---
---

## ✅ Setup Checklist

- [ ] Install required tools (Anaconda, GitHub Desktop, VS Code with extensions, Git)
- [ ] Verify Git installation with `git --version`
- [ ] Clone the repository into local folder using GitHub Desktop
- [ ] Ensure dataset file `Superstore.csv` is placed inside `/data`
- [ ] Create Python environment `superstore` (via Anaconda Prompt or Navigator)
- [ ] Install required libraries (`pandas, numpy, matplotlib, seaborn, scikit-learn, jupyter, statsmodels`)
- [ ] Open repo folder in VS Code (`File → Open Folder → Superstore-analysis`)
- [ ] Set VS Code as external editor in GitHub Desktop (File → Options → Integrations)
- [ ] Confirm VS Code is using the correct interpreter (`Python (superstore)`)
- [ ] Verify folder structure includes `/data`, `/notebooks`, `/visuals`, `/report`, `/slides`
- [ ] Create notebook in `/notebooks` named `analysis_superstore_<name>.ipynb`
- [ ] Run code cell with **Shift + Enter**
- [ ] Save notebook with **Ctrl + S**
- [ ] Commit changes in GitHub Desktop with a clear message
- [ ] Push changes to GitHub
- [ ] Verify notebook and outputs appear correctly on GitHub.com


