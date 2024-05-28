Oii, aqui é o Tieppo, escrevi algumas coisas pra se caso estiverem perdidos ok?!

# RODAR O PROJETO
se tiver o node instalado ignore a próxima linha:
- pra rodar o projeto você precisa ter o node instalado na sua máquina, ele é um runtime(basicamente um executor de código), pra ter ele é só instalar por aqui https://nodejs.org/en, ele é necessário visto que as dependências são construidas em cima dele

- depois basta entrar na pasta do projeto com um terminal(pode ser o do vscode também) e executar os comandos:
- npm install
- npm run dev

agora é só abrir o navegador e digitar localhost:3000 (por padrão roda na porta 3000, quando executar o npm run dev ele vai informar a porta caso troque)



# O PROJETO RODA MAS NÃO TO ENTENDENDO NADA
- eu sei que parece muita informação e geralmente não é nada parecido com o que foi visto de linguagem até aqui, tem muitas pastas, arquivos diferentes e etc, vou te dar um macete, o projeto já foi configurado por mim, então vai eliminar uns 60% do que ta vendo, ignore tudo o que eu não colocar aqui em baixo, o projeto foi construido nisso:

/pages
/components
/public

a pasta pages tem arquivos que serão as páginas, o index sempre vai ser a primeira página e o restante serão páginas onde você poderá navegar, imagine que o .vue é o .html, logo eu explico mais sobre ele, tudo o que estiver dentro da pasta components são pedaços das páginas, por exemplo, o navbar.vue é um arquivo que cria o menu de navegação que fica em cima da página, eu importo ele no index.vue colocando dentro do html uma tag com o mesmo nome do arquivo que está la em components, que seria o <navbar />, basicamente é isso, parece muita coisa mas no fundo é só html, javascript e css :)

no vue, diferente dos frameworks que eu utilizo, você escreve a lógica como no html, então a linguagem de programação vai estar dentro da tag <script>, eu particularmente separo mas o processo é mais complexo, pra facilitar deixei no mesmo arquivo, então sempre vai ter o html depois o js e caso tenha, o css em seguida, eu utilizei o tailwind por ser mais rápido e prático pra mim, mas configurei o projeto pra poderem escrever o css normalmente

Acredito que é isso, boa sorte e qualquer coisa me chama que eu ajudo a entender(vale pra qualquer um que ler), assim como você provavelmente se encontra perdido eu também estive, gostaria muito de ter alguém pra tirar minhas dúvidas, por isso estou disposto a fazer o mesmo, e não se incomode com o "eu não sei nada, tenho vergonha de perguntar", eu também não sabia nada e continuo aprendendo
