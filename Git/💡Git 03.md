# ๐กGit 03


## Git install package


#### 1. pip install (package name)
> ํจํค์ง ์ค์นํ๊ธฐ

```bash
$ pip install requests
Collecting requests
  Using cached requests-2.28.1-py3-none-any.whl (62 kB)
Requirement already satisfied: charset-normalizer<3,>=2 in c:\users\Username\appdata\local\programs\python\python39\lib\site-packages (from requests) (2.1.0)
Requirement already satisfied: certifi>=2017.4.17 in c:\users\Username\appdata\local\programs\python\python39\lib\site-packages (from requests) (2022.6.15)
Requirement already satisfied: urllib3<1.27,>=1.21.1 in c:\users\Username\appdata\local\programs\python\python39\lib\site-packages (from requests) (1.26.10)
Requirement already satisfied: idna<4,>=2.5 in c:\users\Username\appdata\local\programs\python\python39\lib\site-packages (from requests) (3.3)
Installing collected packages: requests
Successfully installed requests-2.28.1
WARNING: You are using pip version 22.0.4; however, version 22.1.2 is available.
You should consider upgrading via the 'C:\Users\Username\AppData\Local\Programs\Python\Python39\python.exe -m pip install --upgrade pip' command.
```


#### 2. pip uninstall (package name)
> ํจํค์ง ์ญ์ ํ๊ธฐ

```bash
$ pip uninstall requests
Found existing installation: requests 2.28.1
Uninstalling requests-2.28.1:
  Would remove:
    c:\users\Username\appdata\local\programs\python\python39\lib\site-packages\requests-2.28.1.dist-info\*
    c:\users\Username\appdata\local\programs\python\python39\lib\site-packages\requests\*
Proceed (Y/n)? Y
  Successfully uninstalled requests-2.28.1
```


#### 3. pip list
> ๋ด ์ปดํจํฐ์ ์ค์น๋ ํจํค์ง๋ฅผ ๋ณด์ฌ์ค๋ค.
> ํจํค์ง๋ฅผ ์ค์นํ ํ ์ค์น๊ฐ ๋๋์ง ํ์ธํ  ์ ์๋ค.

```bash
$ pip list
Package            Version
------------------ ---------
certifi            2022.6.15
charset-normalizer 2.1.0
idna               3.3
pip                22.0.4
requests           2.28.1 --<requests ์ค์น!>--
setuptools         58.1.0
urllib3            1.26.10
WARNING: You are using pip version 22.0.4; however, version 22.1.2 is available.
You should consider upgrading via the 'C:\Users\Username\AppData\Local\Programs\Python\Python39\python.exe -m pip install --upgrade pip' command.
```


#### 4. which (package name)
> ๋ด ์ปดํจํฐ ์ ์ด๋์ ํจํค์ง๊ฐ ์ค์น๋์ด ์๋์ง ๊ฒฝ๋ก๋ฅผ ๋ณด์ฌ์ค๋ค.

```bash
$ which python
/c/Users/Username/AppData/Local/Programs/Python/Python39/python
```


## ๊ฐ์ ํ๊ฒฝ ๋ง๋ค๊ธฐ
> ๊ฐ์ ํ๊ฒฝ์ ์ฌ์ฉํ๋ ์ด์ ๋ ์ปดํจํฐ๋ง๋ค ์ค์น๋์ด ์๋ ํจํค์ง ๋ฒ์ ์ด ๋ค๋ฅผ ์ ์๊ธฐ ๋๋ฌธ์ด๋ค.
> ํจํค์ง ๋ฒ์ ์ด ๋ค๋ฅธ ๊ฒฝ์ฐ ํ๋ก์ ํธ ๋ณ๋ก ํด๋น ํจํค์ง๋ฅผ ๋๋ฆฝ์ ์ผ๋ก ๊ด๋ฆฌํ  ์ ์๋ค.


#### 1. python -m venv venv
> ๊ฐ์ ํ๊ฒฝ ์์ฑ ๋ช๋ น์ด

```bash
$ python -m venv venv
```


#### 2. python venv/Scripts/activate
> ๊ฐ์ ํ๊ฒฝ์ ์คํ์ํค๋ ๋ช๋ น์ด

```bash
$ python venv/Scripts/activate
(venv)
```

#### 2-1. ์ค๋ฅ ๋ฐ์ ์ ํด๊ฒฐ ๋ฐฉ๋ฒ
> `python venv/Scripts/activate` ์ฝ๋๋ฅผ ์คํํ์ ๋ `SyntaxError` ๋ฐ์
>
> `python`์ `source`๋ก ๋ณ๊ฒฝํด์ ์คํํ๋ค. 

```bash
$ python venv/Scripts/activate
  File "C:\Users\Username\Desktop\์ ๊ทํ๋ก์ ํธ\venv\Scripts\activate", line 4
    deactivate () {        
                  ^        
SyntaxError: invalid syntax
```

```bash
$ source venv/Scripts/activate
(venv) 
```

#### 3. pip list
> ๊ฐ์ ํ๊ฒฝ์ด ์คํ๋์๋์ง ํ์ธํ๋ค.
> ๋งจ ์๋์ `(venv)` ํ์๊ฐ ์์ผ๋ฉด ๊ฐ์ ํ๊ฒฝ์ด ์คํ๋ ๊ฒ์ด๋ค.

```bash
$ pip list
Package    Version
---------- -------
asgiref    3.5.2
Django     4.0.6
pip        22.0.4
setuptools 58.1.0
sqlparse   0.4.2
tzdata     2022.1
WARNING: You are using pip version 22.0.4; however, version 22.1.2 is available.
You should consider upgrading via the 'C:\Users\Username\Desktop\์ ๊ทํ๋ก์ ํธ\venv\Scripts\python.exe -m pip install --upgrade pip' command.
(venv) 
```


#### 4. which python
> python ํจํค์ง๊ฐ ๋ด ์ปดํจํฐ ์ด๋์์ ์คํ๋๊ณ  ์๋์ง ๊ฒฝ๋ก๋ฅผ ๋ณด์ฌ์ค๋ค.

```bash
$ which python
/c/Users/Username/Desktop/์ ๊ทํ๋ก์ ํธ/\Users\Username\Desktop\์ ๊ทํ๋ก์ ํธ\venv/Scripts/python
(venv)
```


#### 5. pip freeze > requeirments.txt
> ํ์ฌ ๋ด ์ปดํจํฐ์ ์ค์น๋์ด ์๋ ํจํค์ง๋ค์ ๋ฒ์  ์ ๋ณด๋ฅผ txt๋ก ๋ง๋ ๋ค.
>
> ํ๋ก์ ํธ๋ฅผ ์งํํ๊ธฐ ์  ํ์๋ค์ด ์์ ์ ์ปดํจํฐ์ ์ค์น๋ ํจํค์ง ๋ฒ์ ์ ํ์ธํ๋ ์ฉ๋์ด๋ค.

```bash
$ pip freeze > requeirments.txt
(venv)
```

```
requeirments.txt

------------------
asgiref==3.5.2
Django==4.0.6
sqlparse==0.4.2
tzdata==2022.1
```
