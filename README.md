<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B132B,50:1B3A6B,100:FFC94D&height=220&section=header&text=IPL%20EDA%20%F0%9F%8F%8F&fontSize=52&fontColor=FDF6E3&animation=fadeIn&fontAlignY=38&desc=A%20deep%2C%20deliberate%20dive%20into%20every%20run%2C%20wicket%20%26%20over&descAlignY=58&descSize=17"/>

<img src="https://readme-typing-svg.demolab.com?font=Georgia&size=21&duration=3000&pause=800&color=1B3A6B&center=true&vCenter=true&width=650&lines=76%2C014+deliveries.+One+dataset.+Zero+shortcuts.;Not+just+plots+%E2%80%94+a+full+reasoning+trail+%F0%9F%94%8D;Univariate+%E2%9E%9C+Bivariate+%E2%9E%9C+Multivariate+%E2%9E%9C+Feature+Eng." />

&nbsp;

<img src="https://img.shields.io/badge/Python-0B132B?style=for-the-badge&logo=python&logoColor=FFC94D" />
<img src="https://img.shields.io/badge/Pandas-1B3A6B?style=for-the-badge&logo=pandas&logoColor=FDF6E3" />
<img src="https://img.shields.io/badge/Seaborn-F2C14E?style=for-the-badge&logo=python&logoColor=0B132B" />
<img src="https://img.shields.io/badge/Matplotlib-0B132B?style=for-the-badge&logo=plotly&logoColor=FFC94D" />

&nbsp;

<img src="https://img.shields.io/badge/focus-Exploratory_Data_Analysis-1B3A6B?style=flat-square" />
<img src="https://img.shields.io/badge/observations-76,014-0B132B?style=flat-square" />
<img src="https://img.shields.io/badge/raw_features-15-F2C14E?style=flat-square" />
<img src="https://img.shields.io/badge/status-EDA_%26_feature_engineering_complete-1B3A6B?style=flat-square" />

</div>

<br>

<div align="center">
<img src="https://user-images.githubusercontent.com/74038190/212284158-e840e285-664b-44d7-b79b-e264b5e54825.gif" width="420">
</div>

<br>

## 🏟️ ୨୧ What This Project Actually Is

> *Before you can predict a score, you have to understand the game. This notebook is that part — the slow, careful part.*

This project is a **pure, in-depth Exploratory Data Analysis** of IPL ball-by-ball data — 76,014 rows describing the state of an innings at different points in time. It is **not** a modeling project. There is no trained model, no accuracy score, no leaderboard here. What it *is*, instead, is a **complete analytical walkthrough**: every plot is followed by *why it was made*, *what question it answers*, and *what it actually tells us about cricket*.

<div align="center">

```
   🏏 raw data  →  🔍 understand  →  📊 visualize  →  🧠 interpret  →  ⚙️ engineer
```

</div>

Think of it less like a script that runs top to bottom, and more like a **lab notebook** — reasoning shown at every step.

<br>

## 📂 ୨୧ The Dataset

<div align="center">

| 🏏 Feature | 📖 What It Tells Us |
|:---:|:---|
| `mid` | Match ID |
| `date` | Match Date |
| `venue` | Stadium the match was played at |
| `bat_team` | Batting Team |
| `bowl_team` | Bowling Team |
| `batsman` | Current Striker |
| `bowler` | Current Bowler |
| `runs` | Current Team Score |
| `wickets` | Wickets Lost |
| `overs` | Overs Completed |
| `runs_last_5` | Runs in Last 5 Overs *(momentum!)* |
| `wickets_last_5` | Wickets in Last 5 Overs |
| `striker` | Runs by current striker |
| `non-striker` | Runs by non-striker |
| **`total`** | 🎯 Final Innings Score |

</div>

<br>

## 🧰 ୨୧ The Toolkit — *and Why Each Tool Earned Its Place*

The notebook opens by justifying every import before using it — not just `import pandas as pd`, but *why pandas, why now.*

<table>
<tr>
<td width="25%" align="center">

**🐼 Pandas**
The backbone.
Loading, inspecting,
cleaning, structuring.

</td>
<td width="25%" align="center">

**🔢 NumPy**
The engine underneath.
Fast numerical
computation.

</td>
<td width="25%" align="center">

**📉 Matplotlib**
The canvas.
Histograms, scatter
plots, box plots.

</td>
<td width="25%" align="center">

**🎨 Seaborn**
The stylist.
Heatmaps, pair plots,
statistical polish.

</td>
</tr>
</table>

<div align="center">

`plt.style.use("ggplot")` — because a good analysis should also look like one 🌸

</div>

<br>

## 🔍 ୨୧ Step 1: Getting to Know the Data

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0B132B,100:FFC94D&height=3&width=800" />
</div>

Before any plot is drawn, the dataset is interrogated like a new signing before their first match:

- 👀 **First & Last 5 Rows** — what does one row actually represent?
- 📐 **Shape** — how many deliveries, how many features?
- 🏷️ **Column Names & Structure** — `dtypes`, memory footprint
- 📊 **Summary Statistics** — `describe()` for every numeric feature
- 🕳️ **Missing Values** — any gaps in the innings?
- 👯 **Duplicate Records** — any ball counted twice?

Every single one of these steps is documented with **Purpose → Why it's required → Questions it answers → Interpretation** — the notebook never just runs a command, it explains itself.

<br>

## 🧵 ୨୧ Step 2: Feature Understanding & Categorization

Every column is sorted into its true role before analysis begins:

<div align="center">

| Type | Examples |
|:---:|:---|
| 🔢 Numerical | `runs`, `wickets`, `overs`, `runs_last_5` |
| 🏷️ Categorical | `venue`, `bat_team`, `bowl_team` |
| 🆔 Identifier | `mid` |
| 📅 Date | `date` |
| 🎯 Target | `total` |

</div>

<br>

## 📊 ୨୧ Step 3: Univariate Analysis — *One Variable at a Time*

Each individual feature — starting with **Runs** — gets the full treatment:

<div align="center">

```
Purpose → Why analyze it → Questions it answers → Interpretation → Key Insights
```

</div>

And the box plots aren't just *shown* — they're **read out loud, step by step**:

<table>
<tr>
<td width="50%" valign="top">

**📦 Anatomy of a Box Plot**
1️⃣ What feature is this?
2️⃣ Identify the box
3️⃣ Find the median
4️⃣ Read the left whisker

</td>
<td width="50%" valign="top">

5️⃣ Read the right whisker
6️⃣ Spot the outliers
7️⃣ Ask: are these errors, or real cricket? 🏏

</td>
</tr>
</table>

<br>

## 🤝 ୨୧ Step 4: Bivariate Analysis — *How Two Variables Talk to Each Other*

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0B132B,100:FFC94D&height=3&width=800" />
</div>

Every relationship explored follows the same rigorous rhythm — *Why analyze this? → Questions Answered → Interpretation → Key Insights*:

- 🏏 **Current Runs 🆚 Final Total**
- ⏳ **Overs 🆚 Final Total**
- ⚠️ **Wickets 🆚 Final Total**
- 🏟️ **Venue 🆚 Average Final Total**

<br>

## 🌐 ୨୧ Step 5: Multivariate Analysis — *Seeing the Whole Pitch at Once*

- 🎨 **Runs, Wickets & Final Total** — color-encoded scatter plots
- 📈 **Runs, Overs & Final Total** — reading a scatter plot, properly explained
- 🔗 **Pair Plot** of all numerical features
- 🔥 **Correlation Heatmap**

<br>

### 🗺️ The Correlation Heatmap Isn't Just Shown — It's *Taught*

This is genuinely one of the loveliest parts of the notebook: a full **step-by-step guide to reading a correlation heatmap**, written like a mini-tutorial —

<div align="center">

```
1. Understand what correlation means
2. Ignore the diagonal
3. Read only one half (it's symmetric!)
4. Start with the target variable
5. Identify strong positive relationships
6. Identify strong negative relationships
7. Validate using real-world cricket knowledge
```

</div>

...followed by real **cricket examples** and a final checklist. This turns a heatmap from "a colorful grid" into an actual analytical skill. 💛

<br>

## ⚙️ ୨୧ Step 6: Feature Engineering — *13 Deliberate Steps*

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0B132B,100:FFC94D&height=3&width=800" />
</div>

Every feature is put on trial before it's kept or dropped — nothing is removed without a documented reason.

<table>
<tr>
<td width="50%" valign="top">

**🔎 The Investigation**
1. Identify irrelevant features
2. Drop identifier column → `mid`
3. Evaluate & drop `date`
4. Understand high-cardinality features
5. Evaluate `batsman` → ❌ removed
6. Evaluate `bowler` → ❌ removed

</td>
<td width="50%" valign="top">

**✅ The Verdict**
7. Retain predictive features (table below)
8. Drop selected columns
9. Verify the updated dataset
10. Identify remaining categorical features
11. Plan One-Hot Encoding
12. Separate `X` (features) & `y` (`total`)
13. Prepare for model training *(next phase!)*

</td>
</tr>
</table>

<br>

### 🏏 The Final Playing XI — *Features That Survived*

<div align="center">

| Feature | Why It Stayed |
|:---:|:---|
| `venue` | Different grounds, different conditions |
| `bat_team` | Batting strength varies by team |
| `bowl_team` | Bowling strength influences scoring |
| `runs` | One of the strongest predictors |
| `wickets` | Batting resources remaining |
| `overs` | Stage of the innings |
| `runs_last_5` | Recent scoring momentum |
| `wickets_last_5` | Recent batting collapses |
| `striker` | Current striker's score |
| `non-striker` | Non-striker's score |
| **`total`** | 🎯 Target variable |

</div>

<div align="center">

**❌ Benched:** `mid` · `date` · `batsman` · `bowler`
*(identifiers, dates, and high-cardinality noise)*

</div>

<br>

## 📌 ୨୧ Key Insights Uncovered

- 🏏 Current score has a **strong positive relationship** with the final total
- 🔥 **Momentum matters** — Runs in Last 5 Overs is a genuinely informative signal
- ⚠️ Every wicket **pulls the projected total down**
- ⏳ Overs alone don't tell the full story — context matters
- 🏟️ **Venue shapes scoring patterns** — every ground has its own personality
- 🧬 High-cardinality features (`batsman`, `bowler`) add complexity without proportional value at this stage

<br>

## 📁 ୨୧ Project Structure

```
IPL-EDA/
│
├── 📂 data/
│   └── ipl_data.csv
│
├── 📓 notebook/
│   └── IPL_EDA.ipynb
│
├── 🖼️ images/
│
└── 📄 README.md
```

<br>

## 🚀 ୨୧ Running This Notebook

```bash
# 1️⃣ Clone the repository
git clone https://github.com/yourusername/IPL-EDA.git

# 2️⃣ Step into the crease
cd IPL-EDA

# 3️⃣ Gear up
pip install pandas numpy matplotlib seaborn

# 4️⃣ Open the notebook
jupyter notebook IPL_EDA.ipynb
```

<br>

## 🔮 ୨୧ What Comes Next *(not yet built — the runway ahead)*

This notebook deliberately stops right where modeling begins — `X` and `y` are prepared, but no model has been trained yet. The natural next phase:

- 🤖 Train Linear Regression / Random Forest / XGBoost regressors
- 📈 Evaluate with MAE, RMSE, R²
- 🎛️ Hyperparameter tuning
- 📡 Live score prediction & deployment

<br>

## 📚 ୨୧ What This Project Demonstrates

<div align="center">

`Data Inspection` · `Feature Categorization` · `Univariate Analysis` · `Bivariate Analysis`
`Multivariate Analysis` · `Correlation Reading` · `Feature Engineering` · `Analytical Reasoning`

</div>

<br>

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0B132B,100:FFC94D&height=3&width=800" />
</div>

## 👩‍💻 ୨୧ Author

<div align="center">

### **Ridhima Gadalay**
*Computer Science Engineering Student*

🤖 Machine Learning · 🧠 Artificial Intelligence · 📊 Data Science · 💻 Full-Stack Development

<img src="https://img.shields.io/badge/GitHub-0B132B?style=for-the-badge&logo=github&logoColor=FFC94D" />
<img src="https://img.shields.io/badge/LeetCode-1B3A6B?style=for-the-badge&logo=leetcode&logoColor=FDF6E3" />

</div>

<br>

<div align="center">

### ⭐ If this analysis made you appreciate cricket data a little more, consider giving it a star!

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:FFC94D,50:1B3A6B,100:0B132B&height=150&section=footer"/>

</div>
