# Steps to reproduce repo

```
git clone 
```

# Steps to create repo

1. Create [GitHub Repo via VSCode](https://code.visualstudio.com/docs/sourcecontrol/intro-to-git).

2. Create README, `.gitignore`, virtual environment (`requirements.txt`), add `/data` files

```
$ python3.9 -m virtualenv venv
$ source venv/bin/activate
$ python -m pip install --upgrade pip
$ env PRODIGY_KEY=XXXX-XXXX-XXXX-XXXX
(venv) $ python -m pip install prodigy -f https://$PRODIGY_KEY@download.prodi.gy
(venv) $ python -m pip install -r requirements.txt
```

3. Install [Quarto](https://quarto.org/docs/get-started/). 

4. Run experiments. Use `01-writeup.qmd` and different doc format.

5. Save models to Hugging Face Hub