<!-- Anotações das aulas -->
# 🚀 Começando

## <font color="E76161"> __SCSS__ </font>
O <font color="#025464"> __SCSS__ </font> é semelhante ao css, porém, ele faz coisas que o CSS não faz. <br />
<font color="8BACAA">
〰️ Usa a extensão de arquivo __``.scss``__ <br />
〰️ Semelhante ao css, com __super poderes__
</font>
_______________________________________________________________
## <font color="E76161"> __SASS__ </font>

O <font color="#025464"> __SASS__ </font> suporta todos os recursos do SCSS, então amboa podem fazer a mesma coisa. A diferença é que o SASS tem a sintaxe recuada. <br />
Isso quer dizer que, ele não usa chaves e ponto e vírgula, ele usa "espaço" no lugar disso. <br />

<font color="8BACAA">

〰️ Usa a ectensão de arquivo __``.sass``__ <br />
〰️ Suporta todos os __recursos__ do __``SCSS``__ <br />
〰️ A __sintaxe recuada__ era a sintaxe original do __SASS__ <br />
〰️ Usa __espaço__ ao invés de chaves e **ponto e vírgula**

</font>
<br />
<br />

## <font color="F45050"> *Diferença dos códigos* </font>
### Bloco de códigos
__``CSS``__
```
body {
   font: 100% Helvetica, sans-serif;
   color: #333
}
```
<br />

__``SCSS``__
```
$font-stack: Helvetica, sans-serif;
$primary-color: #333;

body {
   font: 100% @font-stack;
   color: $primary-color;
}
```
<br />

__``SASS``__
```
$font-stack: Helvetica, sans-serif
$primary-color: #333

body {
   font: 100% @font-stack
   color: $primary-color
}
```

# Aninhamento
### Código html
```
<body>
   <div class="container">
      <div class="esquerdo">
         <div class="texto">
            ⬅️Sass
         </div>
      </div>
      <div class="direito">
         <div class="texto">
            Sass ➡️
         </div>
      </div>
   </div>
</body>
```

### Código SCSS
```
body {
   margin: 0;
   padding: 0;
}

.container {
   height: 100vh;
   display: flex;
   .esquerdo {
      width: 50%;
      background-color: blueviolet;
      .texto {
         margin-top: 40%;
         text-align: center;
         font-size: 150px;
         color: aquamarine;
      }
   }
   .direito {
      width: 50%;
      background-color: aquamarine;
   .texto {
      margin-top: 40%;
      text-align: center;
      font-size: 150px;
      color: blueviolet;
      }
   }
}
```

# Variáveis
```
$cor-prncipal: #DB005B;
$cor-secundaria: #025464;
```

# Função
### Código
```
@mixin reset { <!-- Cria função -->
   margin: 0;
   padding: 0;
}

body {
   @include reset; <!-- Chama função -->
}
```
<br />

### Parâmetros
```
<!-- Passa parâmetros denttro do () -->
@mixin cor-e-texto ($cor-de-fundo, $cor-do-texto) {
   width: 50%;
   background-color: $cor-de-fundo;
   .texto {
      margin-top: 40%;
      text-align: center;
      font-size: 150px;
      color: $cor-do-texto;
   }
}

.container {
   height: 100vh;
   display: flex;
   .esquerdo {
      @include cor-e-texto($cor-prncipal, $cor-secundaria);
   }
   .direito {
      @include cor-e-texto($cor-secundaria, $cor-prncipal);
   }
}

```


<!-- <font color="8BACAA"></font> -->