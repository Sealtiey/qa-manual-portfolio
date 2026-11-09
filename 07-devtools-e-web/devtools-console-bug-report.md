# DevTools — Console: bug report

Bug encontrado analisando os erros da aba *Console* em uma página de artigo do Conduit: a imagem do artigo não carrega porque o `src` aponta para o arquivo errado. Conteúdo original em inglês.

| Category | Label | Value |
|---|---|---|
| Bug overview | Summary | Article image is not displayed because the image source contains an incorrect file number. |
| Environment | Browser | Google Chrome (última versão) |
| | OS | macOS |
| | URL | https://conduit.mate.academy/article/the-meowst-useful-article-ever-ul7y7c |
| Bug details | Precondition | The user has access to the article page. |
| | Steps to reproduce | 1. Open the article page<br>2. Scroll to the article image<br>3. Observe the image |
| | Expected result | The image should be displayed correctly |
| | Actual result | The image is broken and is not displayed because the image source references an incorrect file (4 instead of 3). |
| | Attachments | [image-load-error-logs.png](https://ibb.co/XfPyvPtd) · [image-displayed-correctly](https://ibb.co/prvVN25P) |
| | Severity | Medium |
