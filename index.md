---
title:  Teste Alonso-Gallego-Honey
---

## Autores: Catalina M. Alonso, Domingo J. Gallego e Peter Honey

### Tradução e adaptação: Evelise Maria Labatut Portilho

#### Este questionário está sendo aplicado para identificar seu estilo preferido de aprendizagem. Não existem respostas corretas nem erradas. Será útil desde que seja sincero em respostas. O questionário é anônimo.

##### Marque as afirmativas mais adequadas a seu estilo de vida:

{% assign n=1 %}

{%- for pergunta in site.data.questionario.perguntas -%}
1. <input type="checkbox" id="ponto{{n}}"><label> {{pergunta}}</label>{% assign n=n | plus: 1 %}
{% endfor %}

<button type="butt;on" id='calcular' class='btn' onclick="analisar()">Ver resultado</button>
<div id="result"></div>
<button type="button" id='limpar' class='btn' onclick="limpar()" hidden>Recomeçar</button>

{% include scripts.html %}

---

© {{ site.time | date: '%Y' }} [{{site.desenvolvedor}}]({{site.devurl}}){: target='_blank'}
