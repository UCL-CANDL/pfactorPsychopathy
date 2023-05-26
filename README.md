# pfactorPsychopathy
This repository contains code for the analyses of the paper ‘Psychopathic traits and their relationship with vulnerability to general psychopathology in a young adult sample’ (Carlisi, Fielder et al., in prep). For any queries relating to this code, please email jennifer.fielder.21 (at) ucl.ac.uk.

De-identified data for this study are available by request at https://haririlab.com/projects/procedures.html.

Structural Equation Models were defined using Onyx (Oertzen et al., 2015), a free software environment available at https://onyx-sem.com/. The Onyx files for the two models are ‘bifactor.xml’ and ‘hierarchical.xml’. The model scripts were then exported to be compatible with Lavaan (Rosseel, 2012) for R (R Core Team, 2020) by right clicking on model within Onyx -> Show script -> lavaan. 

The R script pfactorPsychopathy_code.R then defines these models to estimate latent variable factor scores, log transforms skewed variables, and runs regression analyses to then plot. Note that some analyses from the paper (e.g. table of Spearman’s Rho correlations, descriptive statistics) were performed using JASP (JASP Team, 2020) for ease of copying the result tables. JASP is freely available software, found at: https://jasp-stats.org/. 

A key describing the variable names used is below:

Used for the SEM:
- STAI_TOT = State-Trait Anxiety Inventory–Trait Anxiety total score
- CESD_TOT = Center for Epidemiological Studies–Depression Scale total score
- AUDIT_TOT = Alcohol Use Disorders Identification Test total score
- RDU_TOT = Recreational Drug Use Questionnaire total score
- Zd_Anx_combo = mean Z-scored values from the anxious arousal and general distress subscales from the Mood and Anxiety Symptom Questionnaire 
- Zd_Dep_combo = mean Z-scored values from the anhedonic depression and general distress subscales from the Mood and Anxiety Symptom Questionnaire
- Zd_panic_disorder_combo = mean Z-scored symptom counts of social phobia, panic disorder, and agoraphobia from the e-M.I.N.I. (Mini International Neuropsychiatric Interview)
- score19 = Cannabis use symptom counts from the e-M.I.N.I.
- score9 = OCD symptom counts from the e-M.I.N.I.
- score5 = Mania symptom counts from the e-M.I.N.I.
- score22 = Psychosis symptom counts from the e-M.I.N.I.

Used in regression models:
- p_factor_bi = p factor ‘score’ derived from the bifactor model
- internalising_bi = Internalising factor ‘score’ derived from the bifactor model
- externalising_bi = Externalising factor ‘score’ derived from the bifactor model
- p_factor_hi = p factor ‘score’ derived from the hierarchical model
- internalising_hi = Internalising factor ‘score’ derived from the hierarchical model
- externalising_hi = Externalising factor ‘score’ derived from the hierarchical model
- SRP_Int = Self Report Psychopathy Short Form - Interpersonal facet
- SRP_Aff = Self Report Psychopathy Short Form - Affective facet
- SRP_Life = Self Report Psychopathy Short Form - Lifestyle facet
- SRP_Ans_2 = Self Report Psychopathy Short Form - Antisocial facet (using question2)
- SES_AV = Socioeconomic status, averaged from self, mother and father evaluations.
- Sex = Sex

(the suffix of _ log to variables, is after a log transform)
