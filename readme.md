# Data and Replication Code for When LLMs are Reliable for Judging Empathic Communication


[![DOI](https://zenodo.org/badge/998972343.svg)](https://doi.org/10.5281/zenodo.17230987)

We compare how experts, crowdworkers, and LLMs annotate empathic communication across four evaluative frameworks applied to 200 real-world conversations where one speaker shares a personal problem and the other offers support. 


### Data
We sample 50 conversations from four conversation datasets:
- EmpatheticDialogues: 24,850 crowdsourced conversations with annotations on empathy, fluency, and relevance.    
- EPITOME: 3,081 Reddit conversations with annotations on emotional reactions, interpretations, and explorations.   
- Perceived Empathy: 501 conversations with human responses to personal troubles, rated on various dimensions of perceived empathy.  
- Lend an Ear Pilot: 150 workplace trouble conversations with annotations on validating emotions, encouraging elaboration, demonstrating understanding, providing unsolicited advice, self-orientation, and dismissing emotions.


#### Dataset-Specific Subdirectories:
Each of the four datasets has its own subdirectory containing individual rating files from each annotator in the `annotations/` folder:
- `empatheticdialogues/` - Contains ratings from expert1, expert2, expert3, crowd, gpt, claude, and gemini annotators
- `epitome/` - Contains ratings from expert1, expert2, expert3, crowd, gpt, claude, and gemini annotators  
- `perceived_empathy/` - Contains ratings from expert1, expert2, expert3, crowd, gpt, claude, and gemini annotators
- `lend_an_ear/` - Contains ratings from expert1, expert2, expert3, crowd, gpt, claude, and gemini annotators


#### Download the Dataset
You can find the combined annotations for all four datasets in `annotations/combined_annotations_across_methods_and_datasets.csv`. This file contains annotations from three experts, crowds, and LLMs (GPT-4o, Gemini 2.5 Pro, Claude3.7 Sonnet) for each of the 21 dimensions.

The original data for each 50 conversation sample is stored in the `original_data/` directory. You can find the conversations and annotations in the following files:
- EmpatheticDialogues: `sample_empatheticdialogues.csv`
- EPITOME: `sample_epitome.csv`
- Perceived Empathy: `sample_perceived_empathy_annotations.csv` (conversations available upon request to the authors of the associated paper); `perceived_empathy_self_ratings.csv` support-seeker's perceived empathy ratings for the 50 conversations
- Lend an Ear: `sample_lend_an_ear_conversations.csv` and `sample_lend_an_ear_annotations.csv`


### Analysis
We compare inter-rater reliability between experts, crowds, and LLMs using Cohen's Kappa with quadratic weighting and F1 scores.  We also conduct a qualitative analysis of conversations with high and low agreement between annotators.    


### Replicate our Analysis
You can replicate the results from our paper using the jupyter notebook analysis.ipynb in the repository.
