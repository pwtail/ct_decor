# cm_decor

## Install

```commandline
pip install cm_decor
```

## Usage

```python
from cm_decor import cm, ExitStackDecorator


@cm
def f(*, cm):
    f = cm.enter_context(open('file.txt', 'w'))
    f.write('hi')


estack = ExitStackDecorator('estack')


@estack
def f(*, estack):
    f = estack.enter_context(open('file.txt', 'w'))
    f.write('hi')

```