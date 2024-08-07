# Blocos HTML para sistema SGCD
O documento aborda blocos HTML para as páginas da Unesp que usam o sistema SGCD


## Criação de título com linha azul:
```
<h3 span="" style="color:#000"><b>[Título]</b></h3>
<div span="" style="background-color:#009FE0; padding-bottom:5px; margin-bottom:15px;" ></div>
```

## Código para Imagem-botão:
```
<a href="[Link de redirecionamento]" onclick="window.location.href=this.href; window.scrollTo(0, 0); return false;">
    <img 
    title="[Título do botão]" 
    onmouseover="this.src='[ "Link" da imagem para o mouseover ]';" 
    onmouseout="this.src='[ "Link" da imagem para o mouseout ]';" 
    usemap="[Link de redirecionamento]" 
    src="[ "Link" da imagem para o mouseout ]" 
    alt="[Título do botão]" width="100%" height="300">
</a>
```

## Código para Bandeiras EN e ES

```
<p style="text-align: right;">
    <a href="[Link do redirecionamento da página em Inglês]" target="_blank">
        <img 
            style="margin-top: 0px; margin-bottom: 0px;" 
            title="English" 
            onmouseover="this.src='https://www2.unesp.br/Home/propg/2023_idioma_eng-pb.png';" 
            onmouseout="this.src='https://www2.unesp.br/Home/propg/2023_idioma_eng.png';" 
            usemap="[Link do redirecionamento da página em Inglês]" 
            src="https://www2.unesp.br/Home/propg/2023_idioma_eng.png" 
            alt="English" 
            width="64" 
            height="64"
        >
    </a>
    <a href="[Link do redirecionamento da página em Espanhol]" target="_blank">
        <img 
            style="margin-top: 0px; margin-bottom: 0px; margin-left: 16px;" 
            title="Idioma Castelhano" 
            onmouseover="this.src='https://www2.unesp.br/Home/propg/2023_idioma_esp-pb.png';" 
            onmouseout="this.src='https://www2.unesp.br/Home/propg/2023_idioma_esp.png';" 
            usemap="[Link do redirecionamento da página em Espanhol]" 
            src="https://www2.unesp.br/Home/propg/2023_idioma_esp.png" 
            alt="Idioma Castelhano" 
            width="64" 
            height="64"
        >
    </a>
</p>

```

## Código para Carrossel de imagens


```
<!-- Caso queira aumentar o tamanho de suas imagens e a opção do SGCD não estiver te satisfazendo, aumente o valor dos pixels de "max-width" abaixo -->

<div style="position: relative; width: 80%; max-width: 1000px; margin: auto; overflow: hidden;">
    
    
        <div id="meuSlides" style="display: flex; transition: transform 0.5s ease;">
            
            
            <!-- É aqui embaixo que você mudará a sua imagem. Lembre-se de ter adicionado sua imagem no banco de imagens -->
            <!-- OBS.: Para melhor experiência de usuário e evitar imagens distorcidas, garanta que todas as imagens tenham as mesmas dimensões -->
            
            <img src="[Caminho do banco de imagens até a imagem1]" style="width: 100%;" alt="[Nome da imagem 1]">
            <img src="[Caminho do banco de imagens até a imagem2]" style="width: 100%;" alt="[Nome da imagem 2]">
            <img src="[Caminho do banco de imagens até a imagem3]" style="width: 100%;" alt="[Nome da imagem 3]">
            
            
        </div>
        
        <!-- NÃO ALTERAR NADA ABAIXO DESSA LINHA -->
        
        <button onclick="(function() { const slides = document.getElementById('meuSlides'); const totalSlides = slides.children.length; let currentSlide = parseInt(slides.getAttribute('data-current-slide')) || 0; currentSlide = (currentSlide - 1 + totalSlides) % totalSlides; slides.setAttribute('data-current-slide', currentSlide); slides.style.transform = 'translateX(' + (-currentSlide * 100) + '%)'; })()" style="position: absolute; top: 50%; left: 0; transform: translateY(-50%); background-color: rgba(0,0,0,0.5); color: white; border: none; padding: 10px; cursor: pointer;">&#10094;</button>
        <button onclick="(function() { const slides = document.getElementById('meuSlides'); const totalSlides = slides.children.length; let currentSlide = parseInt(slides.getAttribute('data-current-slide')) || 0; currentSlide = (currentSlide + 1) % totalSlides; slides.setAttribute('data-current-slide', currentSlide); slides.style.transform = 'translateX(' + (-currentSlide * 100) + '%)'; })()" style="position: absolute; top: 50%; right: 0; transform: translateY(-50%); background-color: rgba(0,0,0,0.5); color: white; border: none; padding: 10px; cursor: pointer;">&#10095;</button>
        
        <!-- NÃO ALTERAR NADA ACIMA DESSA LINHA -->
    </div>


```


## Código para Carrossel de Imagens que mudam com o tempo

```
<!-- Caso queira aumentar o tamanho de suas imagens e a opção do SGCD não estiver te satisfazendo, aumente o valor dos pixels de "max-width" abaixo -->

    <div id="carousel" style="position: relative; width: 80%; max-width: 600px; margin: auto; overflow: hidden;">


        <div id="slides" style="display: flex; transition: transform 0.5s ease;" data-current-slide="0">

            <!-- É aqui embaixo que você mudará a sua imagem. Lembre-se de ter adicionado sua imagem no banco de imagens -->
            <!-- OBS.: Para melhor experiência de usuário e evitar imagens distorcidas, garanta que todas as imagens tenham o mesmo tamanho -->

            <img onload="(function() { setInterval(function() { const slides = document.getElementById('slides'); const totalSlides = slides.children.length; let currentSlide = parseInt(slides.getAttribute('data-current-slide')) || 0; currentSlide = (currentSlide + 1) % totalSlides; slides.setAttribute('data-current-slide', currentSlide); slides.style.transform = 'translateX(' + (-currentSlide * 100) + '%)'; }, 3000); })()" 
            
                 src="[Caminho do banco de imagens até a imagem 1]" style="width: 100%;" alt="[Nome da imagem 1]" >
            <img src="[Caminho do banco de imagens até a imagem 2]" style="width: 100%;" alt="[Nome da imagem 2]" >
            <img src="[Caminho do banco de imagens até a imagem 3]" style="width: 100%;" alt="[Nome da imagem 3]" >
            
            
            <!-- Insira novas imagens copiando o mesma linha acima, alterando apenas o nome da imagem em "src" e em "alt". Exemplo:
            
            <img src="Home/Pos-Graduacao44/programasdepos/geocienciasemeioambiente/quintoevento.png" style="width: 100%;" alt="Quinto evento" >
            
            -->
            
            <!-- Insira novas imagens abaixo desse comentário -->  
            
        
        
            
            <!-- Insira novas imagens acima desse comentário -->
        </div>


 <!-- NÃO ALTERAR NADA ABAIXO DESSA LINHA -->

        <button onclick="(function() { const slides = document.getElementById('slides'); const totalSlides = slides.children.length; let currentSlide = parseInt(slides.getAttribute('data-current-slide')) || 0; currentSlide = (currentSlide - 1 + totalSlides) % totalSlides; slides.setAttribute('data-current-slide', currentSlide); slides.style.transform = 'translateX(' + (-currentSlide * 100) + '%)'; })()" style="position: absolute; top: 50%; left: 0; transform: translateY(-50%); background-color: rgba(0,0,0,0.5); color: white; border: none; padding: 10px; cursor: pointer;">&#10094;</button>
        <button onclick="(function() { const slides = document.getElementById('slides'); const totalSlides = slides.children.length; let currentSlide = parseInt(slides.getAttribute('data-current-slide')) || 0; currentSlide = (currentSlide + 1) % totalSlides; slides.setAttribute('data-current-slide', currentSlide); slides.style.transform = 'translateX(' + (-currentSlide * 100) + '%)'; })()" style="position: absolute; top: 50%; right: 0; transform: translateY(-50%); background-color: rgba(0,0,0,0.5); color: white; border: none; padding: 10px; cursor: pointer;">&#10095;</button>


<!-- NÃO ALTERAR NADA ACIMA DESSA LINHA -->
    </div>




```
