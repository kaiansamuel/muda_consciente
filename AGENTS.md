# Repository Guidelines

## Estrutura do projeto

Este é um site estático de página única. O documento principal está em `index.html`, que concentra a marcação, os estilos e os scripts da página. Recursos locais ficam em `assets/`, organizados por origem ou tipo: imagens, fontes, bibliotecas JavaScript, favicon e metadados `_wd3`. Não há diretórios de código-fonte, testes automatizados ou pipeline de build separados.

## Desenvolvimento local

Não existe `package.json`, Makefile ou outra configuração de dependências. Para visualizar a página localmente, execute na raiz:

```bash
python3 -m http.server 8000
```

Depois, abra `http://localhost:8000`. O uso de um servidor HTTP é preferível a abrir o arquivo diretamente, pois preserva o carregamento relativo dos recursos.

## Estilo e convenções

Mantenha alterações pequenas e compatíveis com a estrutura existente. Preserve a indentação e o estilo já usados em `index.html`; use nomes de classes descritivos em `kebab-case` quando adicionar novos elementos. Prefira CSS e JavaScript nativos no próprio HTML, salvo necessidade clara de incluir um novo recurso local. Ao adicionar imagens, fontes ou bibliotecas, coloque os arquivos em `assets/` e use caminhos relativos.

## Validação

Não há framework de testes ou requisito de cobertura configurado. Após qualquer alteração, valide manualmente a página em um navegador, verificando layout responsivo, navegação, imagens, fontes, animações e ausência de erros no console. Para mudanças visuais, confira pelo menos uma viewport desktop e uma mobile.

## Commits e pull requests

O histórico de commits não está disponível neste checkout; use mensagens curtas e imperativas, por exemplo `Atualiza seção de contato`. Pull requests devem explicar o objetivo, listar as áreas alteradas e incluir capturas de tela para mudanças visuais. Informe como a página foi validada e destaque qualquer recurso externo ou limitação conhecida.

## Configuração e segurança

Não versione credenciais, tokens ou dados pessoais. Verifique URLs e arquivos referenciados antes de remover ou substituir recursos em `assets/`, pois `index.html` depende deles diretamente.
