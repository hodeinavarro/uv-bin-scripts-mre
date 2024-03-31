# Reproduction steps

## Common

```bash
git clone https://github.com/hodeinavarro/uv-bin-scripts-mre.git
cd uv-bin-scripts-mre
```

## With UV - bugged

```bash
uv venv with-uv
source with-uv/bin/activate
uv pip install -e .
my_package
```

### Output

```bash
❯ my_package
zsh: /Users/hodeinavarro/Developer/astral.sh/uv-bin-scripts-mre/with-uv/bin/my_package: bad interpreter: /Users/hodeinavarro/Library/Caches/uv/.tmp0DXsam/.venv/bin/python: no such file or directory
```

## With venv - expected

```bash
python -m venv with-venv
source with-venv/bin/activate
pip install -e .
my_package
```

### Output

```bash
❯ my_package
Hello, World!
```
