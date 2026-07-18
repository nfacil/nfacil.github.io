# nfacil.github.io

[Site de documentações, tutoriais e FAQ](https://nfacil.github.io/)

## Pré-requisitos

Para editar e executar a documentação localmente, é necessário ter instalado:

- [Git](https://git-scm.com/)
- [Python 3.12](https://www.python.org/downloads/)

Os pacotes Python utilizados pelo projeto estão definidos no arquivo
[`requirements.txt`](requirements.txt):

- `mkdocs==1.6.1`: gerador do site de documentação.
- `mkdocs-material==9.6.16`: tema Material para o MkDocs.
- `pymdown-extensions==10.16.1`: extensões Markdown utilizadas nas páginas.

## Configuração em outra máquina

Clone o repositório e acesse o diretório do projeto:

```bash
git clone https://github.com/nfacil/nfacil.github.io.git
cd nfacil.github.io
```

Crie um ambiente virtual dentro do projeto. O ambiente deve ser recriado em
cada máquina e não deve ser copiado de outro diretório, pois contém caminhos
específicos da instalação local.

### Linux ou macOS

```bash
python3.12 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### Windows PowerShell

```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

O ambiente virtual estará ativo quando `(.venv)` aparecer no terminal. Nas
próximas sessões, basta ativá-lo novamente; não é necessário reinstalar os
pacotes enquanto o `requirements.txt` não for alterado.

## Executando a documentação

Com o ambiente virtual ativo, inicie o servidor local:

```bash
mkdocs serve
```

O site ficará disponível, por padrão, em <http://127.0.0.1:8000/>.

Antes de publicar alterações, valide a documentação em modo estrito:

```bash
mkdocs build --strict
```

O comando gera o site estático no diretório `site/`, que não é versionado.
