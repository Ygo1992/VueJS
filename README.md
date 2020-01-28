# VueJS
Repositório destinado ao estudo de VueJS com o curso https://www.udemy.com/course/vue-js-guia-completo/

## Computed Properties vs Methods vs Watchers
<strong>Computed Properties:</strong> só será reavaliada (recarregada) caso algum objeto utilizado dentro dela seja atualizado, logo, é indicada para a maioria dos casos.<br>
<strong>Methods:</strong> A qualquer renderização, na atualização de qualquer propriedade / objeto o método é reexecutado, mesmo que o método não utilize a propriedade alterada.<br>
<strong>Watchers:</strong> Similar a Computed Properties, no entanto é indicado para operações assíncronas, além disso funciona como um <em>set</em> já a Computed Propertie como <em>get</em><br> pois é obrigatório utilizar <em>return</em>
