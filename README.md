# MotorTech — Site institucional

Site de divulgação para a MotorTech Serviços Automotivos, oficina mecânica em
Rio das Ostras/RJ. Desenvolvido do zero em HTML, CSS e JavaScript, sem framework
nem biblioteca externa.

![Página inicial do site da MotorTech](assets/preview.png)

## Sobre o projeto

O objetivo do site é converter visitante em atendimento. Por isso não há formulário
de contato: todos os CTAs levam direto ao WhatsApp da oficina, já com a mensagem
inicial preenchida, que é o canal que o cliente de fato usa para agendar. A página
é dividida em seis seções — apresentação, sobre, serviços, diferenciais, localização
(com mapa incorporado) e contato.

## O que este projeto demonstra

**Layout responsivo escrito à mão.** São 10 breakpoints, com CSS Grid para as grades
de serviços e diferenciais e Flexbox para os componentes internos. Os tamanhos de
fonte do topo usam `clamp()` para escalar com a largura da tela sem saltos.

**CSS organizado com custom properties.** A identidade visual (paleta, tipografia e
espaçamentos) vive em variáveis no `:root`, então mudar a cor da marca é editar um
valor, não caçar hexadecimais pelo arquivo.

**Acessibilidade levada a sério.** Link "pular para o conteúdo" para quem navega por
teclado, atributos ARIA nos elementos interativos e o menu mobile mantendo
`aria-expanded` sincronizado com o estado real de aberto/fechado.

**JavaScript mínimo e sem dependências.** Cerca de 30 linhas cuidando do menu mobile,
da sombra do cabeçalho ao rolar e do ano no rodapé — tudo com verificação de
existência dos elementos antes de registrar os eventos.

**SEO local.** Título e descrição escritos para busca por oficina na região, que é
como o cliente realmente chega até uma mecânica.

## Estrutura

```
index.html          página única, dividida em seções
css/style.css       estilos, com a identidade visual em variáveis no :root
js/script.js        menu mobile, sombra do header e ano do rodapé
assets/             logo, favicon e o preview acima
```

## Rodando localmente

Como o site é estático, basta abrir o `index.html` no navegador. Para servir por HTTP
(recomendado, para o mapa e os caminhos se comportarem como em produção):

```bash
python -m http.server 8080
```

Depois acesse http://localhost:8080

## Tecnologias

HTML5 · CSS3 (Grid, Flexbox, custom properties) · JavaScript (ES6+)
