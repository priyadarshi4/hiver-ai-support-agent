# AI Support Agent for AppleSupport

An end-to-end AI support agent built for the Hiver SDE Intern
take-home assignment.

## What it does

1. Classifies customer intent
2. Retrieves similar historical AppleSupport conversations
3. Generates a grounded support reply
4. Decides AUTO-HANDLE vs ESCALATE

## Dataset

Twitter Customer Support Conversations dataset.

Brand selected: AppleSupport.

~106K usable AppleSupport conversation pairs.

## Golden Set

200 hand-labelled examples.

40 examples are held out as the final evaluation set.

## Models Tested

- Majority baseline
- TF-IDF + Logistic Regression
- Multinomial Naive Bayes
- SGD
- Ridge
- Linear SVM
- Random Forest
- DistilBERT

## Best observed result

Linear SVM / DistilBERT:

Accuracy: 50.0%
Macro F1: 49.8%

Important: the 100K training labels are weakly supervised,
while evaluation uses hand-labelled golden examples.

## How to Run

1. Open `hiver_submission_clean.ipynb` in Google Colab.
2. Enable GPU if running the transformer experiment.
3. Upload the Twitter dataset when prompted.
4. Upload `golden_set_200_labeled.csv`.
5. Run the notebook cells in order.

## Repository Structure

- `hiver_submission_clean.ipynb` — complete pipeline
- `golden_set_200_labeled.csv` — golden evaluation set
- `Hiver_AppleSupport_AI_Agent_Final_Report.pdf` — final report
- `requirements.txt` — dependencies

## Limitations

The 40-example test set is small and the 100K training labels
are generated using weak supervision. Results should therefore
be interpreted as an engineering prototype evaluation rather
than a production accuracy estimate.
