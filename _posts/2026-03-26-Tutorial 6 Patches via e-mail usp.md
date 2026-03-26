---
title: Aprendendo sobre envio de patches por e-mail USP via git-email
date: 2026-03-25 17:50:00 -0300
categories: [Tutorial, Kernel, Emails]
tags: [tutoriais, softwarelivre]

description: Documentando a descoberta de envios de patches via git-email com o e-mail usp

toc: true
comments: true
---

<div style="text-align: justify;">
Continuando a parte aprendida no Tutorial 5, aqui a única diferença é que usamos o e-mail USP, que não aceita ter apenas um AppPassword vinculado para autenticação. Foi preciso fazer algumas coisas a mais.
\\
Segui o tutorial aparentemente sem problemas até 
```
kw send-patch --send --private --to='<EMAIL-ADDRESS-1>','<EMAIL-ADDRESS-2>' ...
```
que foi onde recorri ao Gemini para configurar o git a não usar STARTTLS para a conexão local, que foi a solução proposta por ele:
```bash
# Configura o git para não usar STARTTLS na conexão local com o proxy
git config --local sendemail.smtpssltoatstart false
git config --local sendemail.smtpencryption ""
```
Depois ocorreu tudo certo!
<hr>
Link do tutorial: <a href="https://flusp.ime.usp.br/git/sending-patches-with-git-and-a-usp-email/">https://flusp.ime.usp.br/git/sending-patches-with-git-and-a-usp-email/</a>
</div>