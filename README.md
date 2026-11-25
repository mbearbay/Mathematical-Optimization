# Mathematical Optimization

[English](#english) | [Dansk](#dansk)

## English

Exam project in mathematical optimisation, written in Python with Gurobi (`gurobipy`) in a Jupyter notebook. It covers two problems: production scheduling and support vector machines formulated as optimisation models.

### Problem 1: Job shop scheduling

A mixed integer programming (MIP) model that assigns the operations of 4 jobs to 4 machines and minimises the makespan (the time until all jobs are finished).

- Basic model with assignment, completion time and precedence constraints
- Machine capacity: sequencing constraints so operations do not overlap on the same machine
- Workload limit per machine, with sensitivity analysis of the limit α
- Emission costs per operation and machine: the trade-off between makespan and emissions, found with the ε-constraint method and shown as a Pareto front

### Problem 2: Support vector machines as optimisation models

Classification of a dataset with 13 explanatory variables (`classificationdata.csv`).

- ℓ1-norm SVM formulated as a linear programme, with sensitivity analysis of the penalty parameter C
- Feature selection SVM: a mixed integer model with binary variables (big-M) and a limit k on the number of variables used, with sensitivity analysis of C and k

### Files

| File | Content |
| --- | --- |
| `exam.ipynb` | Notebook with all models and results |
| `classificationdata.csv` | Data for problem 2 |
| `Exam description.pdf` | The exam assignment |

### How to run

You need Python 3 and a Gurobi license (free for students via [Gurobi Academic](https://www.gurobi.com/academia/academic-program-and-licenses/)).

```bash
pip install gurobipy pandas numpy matplotlib jupyter
jupyter notebook exam.ipynb
```

Change the file path to `classificationdata.csv` in the notebook to `"classificationdata.csv"` so it points to the file in the repository.

**Tools:** Python, Gurobi, pandas, NumPy, Matplotlib, Jupyter

---

## Dansk

Eksamensprojekt i matematisk optimering, skrevet i Python med Gurobi (`gurobipy`) i en Jupyter notebook. Projektet dækker to problemer: produktionsplanlægning og support vector machines formuleret som optimeringsmodeller.

### Problem 1: Produktionsplanlægning (job shop)

En blandet heltalsmodel (MIP), der fordeler operationerne fra 4 jobs på 4 maskiner og minimerer makespan (tiden til alle jobs er færdige).

- Grundmodel med fordelings-, færdiggørelses- og rækkefølgebetingelser
- Maskinkapacitet: sekvensbetingelser, så operationer ikke overlapper på samme maskine
- Grænse for arbejdsbyrde pr. maskine med følsomhedsanalyse af grænsen α
- Udledningsomkostninger pr. operation og maskine: afvejningen mellem makespan og udledning, fundet med ε-constraint-metoden og vist som en Pareto-front

### Problem 2: Support vector machines som optimeringsmodeller

Klassifikation af et datasæt med 13 forklarende variable (`classificationdata.csv`).

- ℓ1-norm SVM formuleret som et lineært program med følsomhedsanalyse af straffeparameteren C
- SVM med variabeludvælgelse: en heltalsmodel med binære variable (big-M) og en grænse k for antallet af variable, med følsomhedsanalyse af C og k

### Filer

| Fil | Indhold |
| --- | --- |
| `exam.ipynb` | Notebook med alle modeller og resultater |
| `classificationdata.csv` | Data til problem 2 |
| `Exam description.pdf` | Eksamensopgaven |

### Sådan køres koden

Du skal bruge Python 3 og en Gurobi-licens (gratis for studerende via [Gurobi Academic](https://www.gurobi.com/academia/academic-program-and-licenses/)).

```bash
pip install gurobipy pandas numpy matplotlib jupyter
jupyter notebook exam.ipynb
```

Ret filstien til `classificationdata.csv` i notebooken til `"classificationdata.csv"`, så den peger på filen i repoet.

**Værktøjer:** Python, Gurobi, pandas, NumPy, Matplotlib, Jupyter
