Desafio proposto por: https://medium.com/@meigarom/o-projeto-de-data-engineering-para-o-seu-portf%C3%B3lio-c186c7191823

## Introdução
Recapitulando, a forma mais simples e direta para entrar na área de Data Science, seja através do primeiro emprego ou da migração de carreira, é construir um Portfólio de Projetos Matador.
Um portfólio de projetos Matador prova que você é tão capaz de solucionar desafios de negócio quanto os Data Scientist que já atuam profissionalmente nas empresas.
Existem 5 tipos de projetos que compõe o portfólio matador: Projetos de Insights, Projetos de Data Engineering, Projetos de Machine Learning, Projetos End to End e Projetos de Data Science.
Se você quer saber mais sobre os outros tipos de projetos, assista esse vídeo do canal “Seja Um Data Scientist” https://youtu.be/LJrK4B7bNWA.
Nesse outro post, https://bit.ly/2yO5mth, você encontra detalhes sobre o Projeto de Insights.
Leia esse post até o final, e descubra detalhes sobre como construir um projeto do tipo Data Engineering para o seu Portfólio.
Projeto Número 02: O Projeto de Data Engineering:
O objetivo do projeto de Data Engineering é coletar e organizar dados. Isso mesmo, você precisa ser capaz de acessar fontes distintas de dados, coletar essas informações e armazenar em um local de fácil acesso e que seja escalável.
Mas Meigarom, porquê eu preciso saber coletar e organizar os dados? Esse não é o trabalho de um Data Engineering?
A resposta para essa pergunta é simples. Muitas empresas ainda não tem os seus dados estruturados e o time de Data Engineering não está completo, portanto, para construir seus modelos de Machine Learning você vai precisar conseguir seus próprios dados. Além disso, com essa habilidade você se torna um Data Scientist independente, você não precisa esperar que os dados estejam organizados para você desenvolver o seu trabalho.
Nenhuma empresa quer contratar um profissional dependente, pense nisso.
O Projeto de Data Engineering cobre 3 passos do roadmap de resolução de problemas em Data Science, sendo esses: Coleta de Dados, Limpeza de Dados e Exploração de Dados.
Se você cumprir esses 3 passos, você criará um solução para coletar e organizar os dados. E para te ajudar a cumprir esses 3 passos, eu vou criar um desafio fictício de uma empresa imaginária para simular um contexto mais real, no qual a solução do problema começa com a coleta e o armazenando dos dados.
Para um Projeto de Data Engineering, eu sugiro que você crie uma solução para a empresa Book Club.
Disclaimer: O Contexto a seguir, é completamente fictício, a empresa, o contexto e os dados, existem somente na minha imaginação.
## Contexto do Desafio:
A Book Club é uma Startup de troca de livros. O modelo de negócio funciona com base na troca de livros pelos usuários, cada livro cadastrado pelo usuário, dá o direito à uma troca, porém o usuário também pode comprar o livro, caso ele não queira oferecer outro livro em troca.
Umas das ferramentas mais importantes para que esse modelo de negócio rentabilize, é a recomendação. Uma excelente recomendação aumenta o volume de trocas e vendas no site.
Você é um Data Scientist contrato pela empresa para construir um Sistema de Recomendação que impulsione o volume de trocas e vendas entre os usuários. Porém, a Book Club não coleta e nem armazena os livros enviados pelos usuários.
Os livros para troca, são enviados pelos próprios usuários através de um botão “Fazer Upload”, eles ficam visíveis no site, junto com suas estrelas, que representam o quanto os usuários gostaram ou não do livro, porém a Startup não coleta e nem armazena esses dados em um banco de dados.
Logo, antes de construir um sistema de recomendação, você precisa coletar e armazenar os dados do site. Portanto seu primeiro trabalho como um Data Scientist será coletar e armazenar os seguintes dados:
O nome do livro.
A categoria do livro.
O número de estrelas que o livro recebeu.
O preço do livro.
Se o livro está em Estoque ou não.
Os Dados do desafio:
Os dados para serem coletados e armazenados, estão disponíveis neste site. http://books.toscrape.com/
Esse site foi desenvolvido e disponibilizado especialmente para praticar web scraping. Não existe nenhum tipo de problema legal ao fazer a coleta de dados.
Como solucionar esse desafio?
Esse é um desafio de Data Engineering. Ele é bem mais complicado do que parece, mas é um ótimo exercício para você desenvolver habilidades de Programação e Engenharia de Softwares para criar pipeline de dados.
Eu vou deixar aqui um roteiro para você se orientar, ele pode ser modificado da forma que você preferir ou simplesmente ignorado. Provavelmente, você já tem um roteiro de resolução melhor para abordar esse desafio.
E o mais importante, tenha paciência, criar uma solução leva tempo, assuma uma postura resiliente e nunca desista, afinal você quer ser um Data Scientist e ganhar um ótimo salário, não quer?
## Roteiro Sugerido para a Resolução:
Esse é o roteiro de resolução do desafio que eu sugiro:
Faça o web scraper, necessariamente, utilizando a linguagem Python.
Utiliza a biblioteca Selenium do Python para navegar entre os links das categorias e as páginas.
Utiliza a biblioteca BeautifulSoup do Python para coletar os dados das páginas HTML.
Instale no seu computador e configure um banco de dados Postgres.
Crie uma tabela para armazenar os dados.
Agende seu script para rodar todos os dias em um horário específico. ( Não tem problema armazenar dados repetidos, já que o site não tem atualizações diárias )
Garanta que seu script saiba lidar com possíveis erros e não pare de funcionar por qualquer problema ( internet lenta, página não encontrada, objeto não carregado, etc ).
Salve seu projeto em um repositório público Github ou Bitbucket.
Escreva o README com todos os passos necessários, para que outras pessoas consigam usar sua solução.
Tornar sua solução Profissionalmente Respeitada:
Crie sua solução modularizada. O Script em Python deve salvar um arquivo csv em alguma pasta da sua máquina e então outro script em bash, deve fazer a inserção dos dados no banco de dados.
Sincronize esse dois script ( Python para coletar e salvar os dados e o Bash script para inserir no banco Postgres ).
Faça o gerenciamento desses jobs utilizando o Airflow ( Framework de gerenciamento de Jobs ). Um script só pode rodar, quando o outro terminar.
Paraleliza seu script de coleta. Crie workers que trabalham em paralelo, cada um coleta e armazena os dados dos livros de uma página.
