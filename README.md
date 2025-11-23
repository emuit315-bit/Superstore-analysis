# 📖 Final README.md for Superstore-analysis

```markdown
# Superstore-analysis Team Guide

## 📦 Install Required Apps
- [Anaconda](https://www.anaconda.com/download) → install with defaults  
- [GitHub Desktop](https://desktop.github.com) → install with defaults  
- *(Optional)* [VS Code](https://code.visualstudio.com) for editing files

---

## 🔑 First-Time Setup

1. **Clone the repo**
   ```bash
   https://github.com/emuit315-bit/Superstore-analysis.git
   ```
   Place it in a folder like:
   ```
   C:\Users\<YourName>\Downloads\Intro_grp_assign\Superstore-analysis
   ```

2. **Create environment in Anaconda**
   - Name: `superstore`  
   - Python: 3.10+  

3. **Install packages**
   - `jupyterlab`  
   - `pandas`  
   - `numpy`  
   - `matplotlib`  
   - `seaborn`  
   - `scikit-learn`

---

## 📂 Dataset Setup

1. Download Kaggle **Superstore dataset**.  
2. Place it in:
   ```
   Superstore-analysis/Data/Superstore.csv
   ```
3. Confirm with:
   ```python
   import os
   os.listdir("Data")
   # should show ['Superstore.csv']
   ```

---

## 📓 Working in JupyterLab

1. Launch JupyterLab from Anaconda Navigator (`superstore` environment).  
2. Navigate to `Superstore-analysis/notebooks`.  
3. Create notebook: `analysis_superstore_<yourname>.ipynb`.  
4. Load dataset:
   ```python
   import pandas as pd
   df = pd.read_csv("Data/Superstore.csv", encoding="latin1")
   df.head()
   ```

---

## 🔄 Daily Workflow

### Start of Day
- GitHub Desktop → **Fetch origin** → **Pull origin**  
- Confirm teammates’ commits in **History tab**

### Work
- Edit your notebook in JupyterLab  
- Save often (Ctrl+S)

### End of Day
1. Save notebook  
2. GitHub Desktop → **Changes tab**  
3. Write commit message (e.g., `Added profit by category analysis`)  
4. **Commit to main** → **Push origin**  
5. Confirm on GitHub.com

---

## ✅ Confirming on GitHub.com
- Everyone confirms their own push.  
- Go to repo page → check **Commits tab** or file tree.  
- Ensure your notebook and commit message appear.  
- Team lead double-checks daily that all notebooks are visible and synced.

---

## 🛠️ Conflict Handling
- If GitHub Desktop shows **merge conflict**:  
  1. Pull origin  
  2. Resolve conflicts manually in notebook  
  3. Save → Commit → Push again  
- Tip: Always **Pull before starting work** to avoid conflicts.

---

## 📓 Notebook Naming Convention
- Each teammate uses their own notebook:
  ```
  analysis_superstore_<name>.ipynb
  ```

---

## 📝 Commit Message Examples
- ✅ Good:  
  - `Cleaned missing values in sales column`  
  - `Added visualization: profit by category`  
  - `Explored shipping cost distribution`  
- ❌ Bad:  
  - `stuff`  
  - `changes`  
  - `final`

---

## ✅ Recap
- Install tools → Clone repo → Create environment → Install packages  
- Place dataset in `Data/` → Confirm with `os.listdir`  
- Work in your own notebook → Load dataset with `encoding="latin1"`  
- Daily routine: **Fetch/Pull → Work → Commit → Push → Confirm on GitHub.com**  
- Team lead checks repo daily  
- Use clear commit messages and separate notebooks to avoid conflicts
```

Added full team setup and workflow guide
