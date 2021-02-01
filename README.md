Goal: 

- make <https://epogrebnyak.gitlab.io/doks-howto> a sample multilingual site for doks theme

Non-goal:

- this site also deployed with Netlify at https://gifted-pasteur-36c387.netlify.app/

Changes:

- added `.gitlab-ci.yml`
- removed `public` from `.gitignore`
- changed `baseurl="https://epogrebnyak.gitlab.io/doks-howto"` in `config/_default/config.toml`
  (surprisingly this does not break Netlify deployment)

Covinience:

- added justfile command runner for `just publish` command

Mind model:

- parameters are in `config.toml` in root or `config` folder
- markdown files are in `content` folder
- `static` folder holds images 
- `hugo` command will create html files in `public` folder
- `public/index.html` is site first page - it is served with `hugo serve` command at `localhost`

Barriers:

- cannot render remotely on Gitlab Pages with Hugo due to functions behaviour, serving now `public` folder content

Next:

1. change link to repo + make link a gitlab
2. simplify documentation structure
3. remove or change index.html page
4. add another language `[ru]`
5. show use of shortcodes