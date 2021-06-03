# A Cascata (cascading)

A escolha do browser de qual regra aplicar, caso haja muitas regras para o mesmo elemento.

* Seu estilo é lido de cima para baixo

É levado em consideração 3 fatores

1. Origem do estilo
2. Especificidade
3. Importância

### Origem do estilo

inline > tag style > tag link

O mais forte é (inline):
<h1 style="color: green">Título</h1>

O segundo mais forte é (tag style):
<style>
    h1 {
        color: red;
    }
</style>

O terceiro mais forte é (tag link):
```css
h1 {
    color: blue;
}
```
Se forem origens iguais, sempre prevalecerá a de baixo, seguindo a idéia do efeito de cascata.

### Especificidade

É um cálculo matemático, onde, cada tipo de seletor e origem do estilo possuem valores a serem considerados.

### Valores

0. Universal selector, combinators e negation pseudo-class (:not())
1. Element type selector e pseudo-elements (::before, ::after)
10. Classes e atrribute selectors ([type="radio"])
100. ID selector
1000. Inline

HTML:
                                (Inline = Valor 1000)
<h1 class="title" id="my-title" style="color: orange">Titulo</h1>


```css
/* ID selector = Valor 100 */
#my-title {
    color: gray;
}

/* Classes e atributte selectors = Valor 10 */
.title {
    color: red;
}

/* Element type selector e pseudo-elements = Valor 1 */
h1 {
    color: blue
}

/* Universal selector = Valor 0 */
* {
    color: green;
}

/* Posso somar valores, aumentando a força, juntando classes, ids, etc. Se o valor ultrapassar o proximo nivel da cascata, ele que será aplicado na página */

```

# A regra important

* Cuidado, evitar o uso;
* Não é considerada uma boa prática;
* Quebra o fluxo natural da cascata;

Não se deve usar, apenas em caso de emergência, pois ela substituirá absolutamente tudo. Somente quando eu não conseguir modificar algo sem ele.