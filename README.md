# Experiment Results

| # | Training Dataset   | Training (n) | Evaluation       | Base Model     | F1   | Precision    | Recall    | Model Size   |
|---|--------------------|--------------|------------------|----------------|------|------|------|--------|
| 1 | GPT3.5             | 400          | 20% of training  | None           | 0.32 | 0.44 | 0.24 | 6 MB   |
| 2 | GPT3.5             | 500          | Hold out eval    | None           | 0.36 | 0.41 | 0.31 | 6 MB   |
| 3 | GPT3.5 + Workshop  | 1577         | Hold out eval    | None           | 0.52 | 0.56 | 0.48 | 6 MB   |
| 4 | GPT3.5 + Corrected | 699          | Hold out eval    | None           | 0.38 | 0.44 | 0.34 | 6 MB   |
| 5 | GPT3.5 + Workshop  | 1577         | Hold out eval    | en_core_web_lg | 0.59 | 0.58 | 0.59 | 600 MB |

Dataset Key:

GPT3.5 = [Zero Shot GPT3.5 labeled data](data/gpt3-5-zeroshot.jsonl)

Workshop = [Full PyData NYC workshop annotations](data/pydata-nyc-2023.jsonl)

Corrected = [Sample of corrected PyData NYC workshop annotations](data/hmwk-1-review.jsonl)

Hold out eval = [Sample of 200 evaluation annotations](data/eval-reddit.jsonl)

# Steps to reproduce repo

1. Clone

```
git clone https://github.com/wesslen/dsba6188-homework-1.git
```

2. Create virtual environment

```
$ python3.9 -m virtualenv venv
$ source venv/bin/activate
$ python -m pip install --upgrade pip
$ env PRODIGY_KEY=XXXX-XXXX-XXXX-XXXX
(venv) $ python -m pip install prodigy -f https://$PRODIGY_KEY@download.prodi.gy
(venv) $ python -m pip install -r requirements.txt
```

3. Install [Quarto](https://quarto.org/docs/get-started/). 

4. Run experiments in [00-experiments.ipynb](/00-experiments.ipynb) Jupyter notebook. 

5. Run `01-writeup.qmd`. Modify `format` to get either [`docx`](/01-writeup.docx), [`html`](/01-writeup.html), or [`pdf`](/01-writeup.pdf).

6. Save models as wheel files and/or to Hugging Face Hub. See https://huggingface.co/wesslen/en_ner_reddit_cooking for example.
