---
title:  Teste Alonso-Gallego-Honey
---

### Este questionário serve para identificar seu estilo preferido de aprendizagem. Não existem respostas corretas nem erradas. Será útil desde que você seja sincero nas respostas.

### Marque as afirmativas mais adequadas a seu estilo de vida:

{% assign n=1 %}

{%- for pergunta in site.data.questionario.perguntas -%}
1. <input type="checkbox" id="ponto{{n}}"><label> {{pergunta}}</label>{% assign n=n | plus: 1 %}
{% endfor %}

<button type="button" id='calcular' class='btn' onclick="analisar()">Ver resultado</button>

<div id="result"></div>
<div id="canvasdiv" hidden><canvas id="myChart" width="200" height="200"></canvas></div>

<button type="button" id='limpar' class='btn' onclick="limpar()" hidden>Recomeçar</button>


<script src="{{site.baseurl}}/js/chart.js"></script>
{% include scripts.html %}

---

## Autores: Catalina M. Alonso, Domingo J. Gallego e Peter Honey

### Tradução e adaptação: Evelise Maria Labatut Portilho
### revisão: Luiz T. F. Eleno

## Para saber mais:

1. Catalina M. Alonso, Domingo J. Gallego, Peter Honey, **Los Estilos de Aprendizaje: procedimientos de diagnostico y mejora.** Ediciones Mensajero, 7ª ed. Bilbao, 1995. <a type="button" class='btn' href="{{site.baseurl}}/assets/EstilosLibro.pdf">PDF</a>
2. Daniela Melaré Vieira Barros, **A Teoria dos Estilos de Aprendizagem: convergência com as tecnologias digitais.** Revista SER: Saber, Educação e Reflexão 1(2) 2008. <a type="button" class='btn' href="{{site.baseurl}}/assets/70-228-1-PB 2.pdf">PDF</a>

---

© {{ site.time | date: '%Y' }} [{{site.desenvolvedor}}]({{site.devurl}}){: target='_blank'}
