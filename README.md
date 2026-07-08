# AI_Dock_CKI
## Method Overview

A library of approximately 800000 drug like compounds from the ZINC database was screened against the cryo EM structure of human uMtCK1 (PDB 9B16). An initial subset of compounds was docked using AutoDock Vina and the resulting binding affinity scores were used as labels to train a Gradient Boosting Regressor model. The trained model was then applied to predict docking scores across the full library. A subsequent classification step was performed to identify putative active compounds. Model reliability was evaluated using an applicability domain assessment and external validation was carried out through re docking of selected candidates. Final prioritization was conducted using PAINS filters and standard drug likeness rules.

## Workflow and Notebooks

The computational pipeline is organized into the following notebooks:

- `compile_final.ipynb`  
  Used for extracting compound identifiers, codes, and SMILES representations from the prepared dataset.

- `regression2.ipynb`  
  Main notebook for feature generation, model development, and training of the regression model, as well as initial prediction of docking affinity scores.

- `classification.ipynb`  
  Used to build and apply classification models for identifying potentially active compounds.

- `class_ad.ipynb`  
  Applied to evaluate the applicability domain of the developed models and assess prediction reliability.

- `dock.ipynb`  
  Used for preparing and performing external validation steps, including re docking procedures. Part of this process was carried out in Ubuntu using AutoDock Vina.

- `filters.ipynb`  
  Used for structural filtering and drug likeness screening, including PAINS and other medicinal chemistry rules.

## About me
I am a PharmD candidate at Mashhad University of Medical Sciences in Iran, researching cheminformatics and drug discovery.

## Get in contact with me:
- Email: Mehran.mansouri811@gmail.com
- Telegram: @Mehran_mns  
- [LinkedIn](http://www.linkedin.com/in/mehran-mansouri-4a7579360)