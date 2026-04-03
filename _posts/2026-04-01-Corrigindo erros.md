---
title: Corrigindo erros
date: 2026-04-01 18:00:00 -0300
categories: [Tutorial, Kernel]
tags: [tutoriais, softwarelivre]

description: Resolvendo problemas que causaram problemas de acesso com IP à minha máquina virtual

toc: true
comments: true
---

<div style="text-align: justify;">
Já fazem duas semanas que eu não conseguia mais conectar à máquina virtual via kw ssh, tentamos corrigir isso com vários métodos e etc mas nada estava dando certo, foi ai que tive a brilhante ideia de começar tudo do zero. <br> <hr>
E como foi isso? Deletei todas as pastas dentro do /home/lk_dev e comecei tudo de novo, com a ajuda do Gemini.
<br>
Fui avançando no tutorial, as coisas foram dando certo, que nem tinham ido na primeira vez, fui me tranquilizando. Mas foi logo ai que começaram os mesmos erros, no finalzinho do tutorial 2, nos é pedido para trocar os scripts do launch_vm_qemu e do create_vm_virsh na parte do --kernel, ou no --boot, mudávamos no vmlinuz para o /arch/arm64/.../Image, e era aí que estavam dando os erros. Bastou o gemini me falar para trocar a parte do make localmodconfig para o defconfig que após rodar tudo e fazer todo o procedimento de reinício da VM etc... consegui voltar a acessar a VM mas pelo Image agora!
<br>
NADA ME PARA AGORA, TUTORIAIS 7 E 8 AQUI VOU EU! - E finalizar o tutorial 4 que ficou faltando hehe
</div>