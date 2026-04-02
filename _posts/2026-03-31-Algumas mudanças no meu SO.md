---
title: Mudanças no meu SO
date: 2026-03-31 13:00:00 -0300
categories: [SO]
tags: [softwarelivre]

description: Resolvendo problemas antigos no meu S.O que podiam estar comprometendo o resultado dos tutoriais.

toc: true
comments: true
---

<div style="text-align: justify;">
Já há muito tempo eu tinha sempre algum <i>Warning</i> ou erro mesmo durante execução de comandos que dependiam ou não do
</div>
```bash
sudo apt-get update &&
sudo apt-get upgrade
```
<div style="text-align: justify;">
E então resolvi dar um fim nisso de uma vez por todas, procurei em IA, em sites e consegui uma resolução: <br>
Haviam duas coisas que estavam comprometendo a execução dos comandos, chaves públicas depreciadas de quando instalei alguns programas (Opera e Yarn), então, executei os seguintes comandos:
</div>
```bash
wget -qO- https://deb.opera.com/archive.key | gpg --dearmor | sudo tee /usr/share/keyrings/opera-browser.gpg > /dev/null
sudo gedit /etc/apt/sources.list.d/opera-stable.
// Aqui entrei num editor de texto:
deb [arch=amd64 signed-by=/usr/share/keyrings/opera-browser.gpg] https://deb.opera.com/opera-stable/ stable non-free

curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | gpg --dearmor | sudo tee /usr/share/keyrings/yarnkey.gpg > /dev/null
echo "deb [signed-by=/usr/share/keyrings/yarnkey.gpg] https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-key del 23E71667
```
<div style="text-align: justify;">
E deu tudo certo!
</div>