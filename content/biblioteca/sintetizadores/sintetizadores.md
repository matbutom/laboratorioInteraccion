---js
const eleventyNavigation = {
 key: "sintetizadores",
 parent: "maquinas"
}
---

# Sintetizadores

{% for sintetizador in sintetizadores.sintetizadores %}

## {{ sintetizador.marca }} {{ sintetizador.modelo }}

Categorías: {{ sintetizador.categorias | join(", ") }}

Enlaces:
{% for enlace in sintetizador.enlaces %}

- [{{ enlace }}]({{ enlace }})
{% endfor %}

{% endfor %}
