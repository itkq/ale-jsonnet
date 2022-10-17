# ale-jsonnet

## Usage

Minimum config of dein

```vim
[[plugins]]
repo = 'itkq/ale-jsonnet'

[[plugins]]
repo = 'dense-analysis/ale'
hook_add = '''

let g:ale_linters = {
\   'jsonnet': ['jsonnetfmt'],
\}

execute ale#fix#registry#Add('jsonnetfmt', 'ale#fixers#jsonnetfmt#Fix', ['jsonnet'], 'Fix jsonnet files with jsonnetfmt')

let g:ale_fixers = {
\   'jsonnet': ['jsonnetfmt'],
\}
'''
```
