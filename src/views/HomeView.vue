<script setup>
const produtos = [
  {
  id: 1,
  titulo: 'Jurassic Park',
  autor: 'Michael Crichton',
  preco: 58.00,
  capa: '/imagens/jurassic-park.jpg'
}, 
{
  id: 2,
  titulo: 'Orgulho e Preconceito',
  autor: 'Jane Austen',
  preco: 51.00,
  capa: '/imagens/orgulho-e-preconceito.jpg'
},
{
  id: 3,
  titulo: 'O morro dos ventos uivantes',
  autor: 'Emily Bronte',
  preco: 44.90,
  capa: '/imagens/o-morro.jpg'
},
{
  id: 4,
  titulo: 'Capitães de areia',
  autor: 'Jorge Amado',
  preco: 36.70,
  capa: '/imagens/capitaes.jpg'
},
{
  id: 5,
  titulo: "Olhos d'água",
  autor: 'Conceição Evaristo',
  preco: 24.50,
  capa: '/imagens/olhos.jpg'
},
{
  id: 6,
  titulo: 'Uma correnteza sufocante',
  autor: 'Allison Saft',
  preco: 27.00,
  capa: '/imagens/correnteza.jpg'
}
]
</script>

<template>
  <header>
    <div>
    <span><a href="#">EL BANCO</a></span>
    <p>Apreço a leitura</p>
    </div>

    <div>
    <i class="fa-solid fa-magnifying-glass"></i> <input type="search"> 
    </div>

    <nav>
    <ul>
      <li>Termos</li>
      <li>Equipe</li>
      <li>Envio</li>
      <li>Devoluções</li>
    </ul>
    </nav>

<ul class="icones">
  <li><i class="fa-solid fa-cart-shopping"></i></li>
  <li><i class="fa-solid fa-heart"></i></li>
  <li> <i class="fa-solid fa-user"></i></li>
</ul>
  </header>

  <main>
   <section class="banner">
    <div>
    <p class="esp">Livro destaque</p>

    <h2>blablabla</h2>
    <p>Descrição do livro</p>
    <button>Acessar página do livro</button>
    </div>

    <img src="/imagens/scott-pilgrim-1.jpg" alt="">
   </section>

   <section class="info">
    <div>Frete grátis para SC</div>
    <div>Livros recomendados</div>
    <div class="a">Mais vendidos</div>
   </section>
   
   <section class="produtos">
    <h2>Lançamentos</h2>

    <div class="livros" v-for="livro in produtos" :key="livro.id">
      <img :src="livro.capa">

      <h3>{{ livro.titulo }}</h3>
      <p class="autor">{{ livro.autor }}</p>
      <p class="preco">R${{ livro.preco }}</p>

      <button>Comprar</button>
    </div>
   </section>
  </main>

  <footer>
    <div>
      <p>EL BANCO</p>
      <ul>
        <li> <a href="">A</a> </li>
        <li> <a href="">B</a> </li>
        <li> <a href="">C</a> </li>

      </ul>
    </div>

    <div>
      <p>Contato</p>
      <p>(47) 4004-5263</p>
      <p>contato@elbank.com</p>
    </div>
  </footer>


</template>

<style scoped>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap');

/* geral */
p, h1, h2, span, li, button, div {
  font-family: "Montserrat", sans-serif;
}

/*header*/
header{
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 15px 190px;
  border-bottom: 1px solid #cccccc;
}

header div{
  display: flex;
  gap: 15px;
  align-items: center;
}

header span{
  border-right: 2px solid #c21a1a;
  padding: 5px 15px;
  font-family: "Montserrat", sans-serif;
  font-weight: bold;
}

header span a{
  color: black;
  text-decoration: none;
}


header ul{
  display: flex;
  gap: 10px;
  list-style: none;
}

ul.icones{
  font-size: 1.5rem;
  gap: 30px;
}

nav ul{
  gap: 20px;
}

/* banner */

.banner{
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2vw 10vw;
}

.banner img{
  width: 18vw;
}

.banner p.esp{
color: #c21a1a;
border: 2px solid #c21a1a;
border-radius: 5px;
padding: 10px;
margin: 2vw 0;
}

.banner h2{
font-size: 4rem;
font-weight: bold;
margin: 2vw 0;
}

.banner p{
  font-size: 1.5rem;
  margin: 2vw 0;
}

.banner button{
  background: #c21a1a;
  border: none;
  border-radius: 5px;
  color: white;
  padding: 20px;
  font-size: 1.5rem;
}

/* info */

.info {
  display: flex;
  justify-content: space-around;
  padding: 20px;
  border-top: 1px solid #cccccc;
  border-bottom: 1px solid #cccccc;
}

.info div{
  flex: 1;
  text-align: center;
  padding: 10px;
   border-right: 2px solid #c21a1a;
   font-size: 1.5rem;
}

.info div.a{
  border: none;
}

/* footer */

footer{
  display: flex;
  justify-content: space-between;
  padding: 2vw 10vw;
    background: #c21a1a;
}

footer p, footer li{
  font-family: 1.5rem;
  color: white;
  margin: 10px;
}
</style>
