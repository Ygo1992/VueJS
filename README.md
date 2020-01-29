# VueJS
Repositório destinado ao estudo de VueJS com o curso https://www.udemy.com/course/vue-js-guia-completo/

## Utilizando variável e função (definidas no Vue) no HTML
<strong> Entre tags HTML </strong>: Utilizar entre {{ }}. <code>{{ nomeVariavel }}</code> ou <code>{{ nomeFuncao() }}</code><br>
<strong> Em propriedade de tag:</strong> 
<ul>
    <li><code>&#60;a v-bind:href="nomeVariavel"&#62; Link &#60;/a&#62;</code> OU <code>&#60;a :href="nomeVariavel"&#62; Link &#60;/a&#62;</code> para valor mutável;</li>
    <li><code>&#60;span v-text="nomeVariavel"&#62;&#60;/span&#62;</code> para valor imutável;</li>
    <li><code>&#60;button v-on:click="nomeFuncao"&#62;&#60;/button&#62;</code> OU <code>&#60;button @click="nomeFuncao"&#62;&#60;/button&#62;</code> para chamar função</li>
</ul>

<strong>Forçando apenas uma renderização:</strong> Utilizar o <em>v-once</em>, <code>&#60;span v-once="nomeVariavel"&#62;&#60;/span&#62;</code>, assim essa tag só assumirá o primeiro valor de nomeVariavel mesmo que ela sofra modificações<br>
<strong>Usar código HTML via variável VueJS:</strong> Utilizar o <em>v-html</em>, &#60;span v-html="nomeVariavelContendoHTML"&#62;&#60;/span&#62;, assim o trecho HTML da variável será identificado e interpretado pelo navegador<br>
<strong>Two-way data binding:</strong> a variável pode ser atualizada tanto via VueJS quanto via HTML (com input por exemplo), basta utilizar <em>v-model</em>, como <code>&#60;input v-model="nomeVariavel"&#62;</code>

## Computed Properties vs Methods vs Watchers
<strong>Computed Properties:</strong> só será reavaliada (recarregada) caso algum objeto utilizado dentro dela seja atualizado, logo, é indicada para a maioria dos casos.<br>
<strong>Methods:</strong> A qualquer renderização, na atualização de qualquer propriedade / objeto o método é reexecutado, mesmo que o método não utilize a propriedade alterada.<br>
<strong>Watchers:</strong> Similar a Computed Properties, no entanto é indicado para operações assíncronas, além disso funciona como um <em>set</em> já a Computed Propertie como <em>get</em> pois é obrigatório utilizar <em>return</em>
