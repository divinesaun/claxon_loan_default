Financial institutions face significant risks due to loan defaults. Accurately predicting the <br>
probability of default (PD) on loans is critical for risk management and strategic planning. In this <br>
competition, participants are tasked with developing a predictive model that estimates the <br>
probability of default on loans using historical loan data.

How I approach the problem:

Imported the package:
- import a very long list of packages

Loaded the data:
- the had an index column issue which was simple to fix
- some columns were repeated

Data analysis:
- fixed remaining_term values
- fixed job values
- fixed location values and combined underepresented categories
- removed currency
- removed country
- add a nan value to other in gender


Feature engineering:
- created features based on their correlation to the target

Preprocessing:
- imputed gender using a Random Forest model
- imputed other categories using simple imputer

Model selection:
- Tested out a bunch of models using cross validation

Feature selection:
- tried using rfe but was not satisfied with results

Tuning:
- Used randomized search

Intepretation:
Used shap






