# Predicting Text Readability from Scrolling Interactions

Dataset containing scroll interactions of 518 partcipants reading Advanced and Elementary texts from the [OneStopEnglish corpus](https://github.com/nishkalavallabhi/OneStopEnglishCorpus). Participants answer multiple choice reading comprehension questions from [OneStopQA](https://github.com/berzak/onestop-qa).

### Example

![](scroll.gif)


<a name="statistics">

## Statistics (v2.0)

</a>

| Proficiency (%) | Education(%) | Age range (%)   | Hours spent reading Englisdh 
| ---     | ---          | ---       | ---     |
| Native  46.69  | Graduate 53.67           | 18 - 24 18.23     | 0 - 4 24.20  |
| Near-native 14.75     | Undergraduate 39.51   | 25-34 57.19 | 5 - 9 22.87 |
| Advanced  27.78  | High School 3.59   |  35-44 13.38 | 10 - 14  11.72|
| Intermediate  9.83 | Vocational 2.65          | 45-54 8.02    | 15 - 19 7.18 |
| Beginner  0.95 | No formal  0.57          | 55+ 3.17   | 20 + 33.84|

<a name="files">

## Directory Structure 

</a>

**`data_[version]/`**

SR DataViewer Interest Area and Fixation Reports, and syntactic annotations. 

- `sent_ia.tsv` Interest Area report.  
- `sent_fix.tsv` Fixations report. 
- `annotations/` Syntactic annotations.

**`participant_metadata/`**

- `metadata.tsv` metadata on participants.

- `test_scores/`
    - `test_conversion.tsv` unofficial conversion table between standardized proficiency tests (used to convert TOEIC to TOEFL scores).  
    - `michigan/` Item level responses for the Michigan Placement Test (MPT).   
    - `comprehension/` Item level responses for the reading comprehension during the eyetracking experiment.  

**`splits/`**

Trial and participant splits.

- `trials/`
    - `all_trials.txt` trial numbers for all the sentences (1-157).
    - `shared_trials.txt` trial numbers of the Shared Text regime.
    - `individual_trials.txt` trial number of the Individual Text regime.
- `participants/[version]/`
    - `random_order.csv` random participant order.
    - `train.csv` train participants.
    - `test.csv` test participants.

<a name="docs">

**`dataset_analyses.Rmd`**

Analyses for the paper "CELER: A 365 Participants Corpus of Eye Movements in L1 and L2 English Reading".
Note that this script requires:
- CELER (in the folder `data_[version]/`) and, 
- GECO Augmented (in the folder `geco/`). Download [GECO augmented](https://drive.google.com/file/d/1T4qgbwPkdzYmTvIqMUGJlvY-v22Ifinx/view?usp=sharing) with frequency and surprisal values and place `geco/` at the top level of this directory.

## Documentation

</a>

- [Eyetracking Variables](documentation/data_variables.md) Description of the variables in the fixations and interest area reports.
- [Metadata Variables](documentation/metadata_variables.md) Description of the variables in the participants metadata file.
- [Language Models](documentation/language_models.md) Details on langugae models for surprisal values.
- [Syntactic Annotations](documentation/syntactic_annotations.md) Details on syntactic annotations (POS, phrase structure trees, dependency trees).
- [GECO Augmented](documentation/geco_augmented.md) Details on new fields added to GECO.
- [Experiment Builder Programs](documentation/EB_programs.md) Information on the EB experiment.
- [Known Issues](documentation/known_issues.md) Known issues with the dataset.

<a name="cite">

## Citation

CELER: A 365 Participants Corpus of Eye Movements in L1 and L2 English Reading

TODO: Add citation

</a>
