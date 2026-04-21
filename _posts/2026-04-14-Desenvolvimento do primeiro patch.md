---
title: Desenvolvimento do 1º Patch
date: 2026-04-19 20:00:00 -0300
categories: [Kernel]
tags: [softwarelivre, kernel]

description: 

toc: true
comments: true
---

<div style="text-align: justify;">
    Ao identificarmos as linhas duplicadas entre os dois arquivos <i>jpeg_v5_0_1.c</i> e <i>jpeg_v5_0_2.c</i>, elaboramos uma solução pegando a função duplicada, colocando-a em um novo arquivo, o qual apelidamos de <i>jpeg_v5_0_interrupt.c</i>, importando-o nos arquivos originais e usando a função nova nas rotinas que a usavam anteriormente.
    <hr>
    Agora precisamos apenas enviar o patch para o CI da disciplina, Marcelo, para ele validar nosso patch, para, logo depois, enviarmos para a lista dos mantenedores dos drivers da gpu, concluindo a 1ª parte da disciplina
</div>