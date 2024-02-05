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

5. Run `01-writeup.qmd`. Modify `format` to get either [`docx`](/01-writeup.docx), [`html`](01-writeup.html), or [`pdf`](01-writeup.pdf).

6. Save models as wheel files and/or to Hugging Face Hub. See https://huggingface.co/wesslen/en_ner_reddit_cooking for example.
