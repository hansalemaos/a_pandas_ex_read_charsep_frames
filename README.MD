# Reads data separated by any char  

## pip install a-pandas-ex-read-charsep-frames

### Common problem:


```python
  File "pandas\_libs\parsers.pyx", line 808, in pandas._libs.parsers.TextReader.read_low_memory
  File "pandas\_libs\parsers.pyx", line 866, in pandas._libs.parsers.TextReader._read_rows
  File "pandas\_libs\parsers.pyx", line 852, in pandas._libs.parsers.TextReader._tokenize_rows
  File "pandas\_libs\parsers.pyx", line 1973, in pandas._libs.parsers.raise_parser_error
pandas.errors.ParserError: Error tokenizing data. C error: Expected 4 fields in line 4, saw 5
```

### Fills up missing values with NaN
```python
from a_pandas_ex_read_charsep_frames import pd_add_read_charsep_frames
import pandas as pd
pd_add_read_charsep_frames()
df = pd.Q_read_charsep_frames(
    encoding="utf-8",
    file_or_string=r"C:\Users\Gamer\Documents\Downloads\alladd.txt",
    sep="\t",
)

print(df)


             0_0  ...                                                0_4
0       01001000  ...                                               <NA>
1       01001001  ...                                               <NA>
2       01001010  ...                                               <NA>
3       01001900  ...   UNESP - Universidade Estadual Júlio de Mesqui...
4       01001901  ...                               Edifício Santa Lídia
          ...  ...                                                ...
732758  99975970  ...                                 AGC São João Bosco
732759  99978000  ...                                               <NA>
732760  99980000  ...                                               <NA>
732761  99980970  ...                                 AC David Canabarro
732762  99980974  ...                           AGC São José do Capingui
[732763 rows x 5 columns]


```