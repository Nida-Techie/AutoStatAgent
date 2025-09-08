# AutoStatAgent: An Agent-Based System for Automated Data Analysis and LaTeX Report Generation

**Project Overview**
AutoStatAgent is an intelligent agentic system that automatically performs exploratory data analysis (EDA), statistical testing, and generates professional LaTeX-based PDF reports from any dataset. It democratizes data analytics, allowing users to simply upload a dataset without needing statistical or programming knowledge.

**Objectives**
Accept datasets in multiple formats (CSV, Excel, JSON, etc.)
Automatically generate meaningful statistical questions

**Perform:**
Univariate, bivariate, and multivariate analysis
Hypothesis testing (t-test, ANOVA, chi-square)
Create appropriate visualizations based on variable types
Compile results into a LaTeX-generated PDF report
Use agent-based architecture for modular, intelligent workflow

**Problem Statement**
Many individuals, especially in academia and business, have valuable datasets but lack the statistical knowledge or programming skills to derive insights. AutoStatAgent provides a fully automated solution that analyzes data and presents results in a readable, interpretable, and publishable format.

**Scope**
Exploratory Data Analysis (EDA)
Statistical Question Generation & Answering
Automated Visualizations (based on variable types)
Hypothesis Testing
LaTeX PDF Report Generation
Modular Agentic Architecture (supports future enhancements)

**System Architecture**
graph TD
A[Upload Dataset] --> B[Agent 1: Data Profiler]
B --> C[Agent 2: Question Generator]
C --> D[Agent 3: Answer Generator]
D --> E[Agent 4: Visualizer]
E --> F[Agent 5: Hypothesis Tester]
F --> G[Agent 6: Report Generator]
G --> H[PDF Report Output]

**System Modules**
**1. Dataset Loader Agent**
Accepts CSV, Excel, JSON
Uses pandas for parsing
Identifies variable types and missing values

**2. Data Profiler Agent**
Generates summary statistics
Infers numerical and categorical features
Suggests possible relationships

**3. Question Generator Agent**
Produces intelligent analytics questions like:
“What is the average value of X?”
“Does A affect B?”
“Are there differences between groups?”

**4. Answer Generator Agent**
Executes code to answer generated questions
Uses pandas, scipy, statsmodels for analysis
Converts results into human-readable explanations

**5. Visualization Agent**
Auto-selects visualizations:
Histogram / Boxplot for univariate
Scatterplot for numerical-numerical
Boxplot / Violin for categorical-numerical
Countplot / Chi-square for categorical-categorical
Uses matplotlib and seaborn

**6. Hypothesis Testing Agent**
Builds null and alternate hypotheses
Performs t-test, ANOVA, chi-square
Reports p-values with interpretations

**7. LaTeX Report Generator**
Uses PyLaTeX or Jinja2 templates
Generates structured PDF sections:
Introduction
Dataset Overview
Questions & Answers
Visualizations
Hypothesis Testing Results

**Technology Stack**
Layer	Tool / Library
Language	Python 3.x
Backend	Pandas, NumPy, SciPy, Statsmodels
Visualizations	Matplotlib, Seaborn
Agents	CrewAI / LangGraph (modular design)
Report Engine	LaTeX via PyLaTeX or Jinja2
Web UI (optional)	Streamlit or Flask
File Handling	Pandas, PyReadStat, openpyxl
Deployment	Docker, Hugging Face, Render
**Repository Structure**
AutoStatAgent/
│
├── dataset_examples/          
├── agents/                    
├── reports/                   
├── Dockerfile                
├── requirements.txt          
└── README.md
