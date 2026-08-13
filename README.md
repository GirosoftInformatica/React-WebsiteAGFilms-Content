# Conteúdo do website AG Films

Repositório de **conteúdo** do site www.agfilms.tv, editado através do backoffice Sveltia CMS (`/admin` no site publicado). Os editores do cliente são colaboradores apenas deste repositório e não têm acesso ao código do site.

O repositório é **público**, porque o conteúdo aqui guardado é o mesmo que o site já publica. Mesmo assim, **não pôr aqui nada que não deva ser público**: rascunhos, contratos, material não licenciado ou qualquer credencial.

- `content/` - documentos JSON das coleções `commercials` (Advertising), `films-tv` e `team`
- `media/` - imagens e vídeos de preview correspondentes (`/media/...` no site)

Em cada commit no `master`, a GitHub Action [sync-site.yml](.github/workflows/sync-site.yml) copia `content/` e `media/` para o repositório do site ([React-WebsiteAGFilms](https://github.com/GirosoftInformatica/React-WebsiteAGFilms)), e esse commit dispara o build e deploy automáticos na Cloudflare. A alteração fica publicada em 2 a 3 minutos.

**Regra importante**: o conteúdo edita-se sempre aqui (ou no backoffice, que commita aqui). As cópias no repositório do site são substituídas pela sincronização e não devem ser editadas à mão.

A Action corre com um secret do repositório, gerido pela GIROSOFT.
