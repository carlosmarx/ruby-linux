# Instalação do Ruby e Rails passo a passo

Este tutorial foi feito baseado na versão 14.04 LTS do Ubuntu, mas funciona em outras distros baseadas no debian. 

## 1º Atualize seu apt-get

Para isso, digite o seguinte comando no terminal:

		sudo apt-get update

## 2º Configurando o terminal.

Abra seu terminal, vá até o menu 'Editar > Preferências do Perfil > Título e comando' e marque a opção
'Executar comando como shell da sessão', feito isso, podemos continuar.

## 3º Instalando o Curl(Às vezes, não sei o porquê, ele não vem instalado)

Apenas digite:
		
		sudo apt-get install curl

## 4º Instalando RVM (Ruby Version Manager)

Com o RVM você pode instalar várias versões diferentes do ruby, e alterar de acordo com a sua necessidade.
	
		curl -sSL http://get.rvm.io | bash

## 5º Instalando uma versão do Ruby e definindo como padrão

Entre com os comandos:

		rvm install 2.2.0

Logo em seguida, para deixa-lo como default:

		rvm use ruby-2.2.0 default

No final disso, o comando abaixo já deverá funcionar:

		ruby -v
		ruby 2.2.0p0 (2014-12-25 revision 49005) [x86_64-linux]

## 6º Instalando o Rails
		
		gem update --system	
		gem install rails

## 7º Crie e teste sua primeira aplicação

Você pode testar o rails criando sua primeira aplicação.

		rails new nome_do_app

Feito isso, navegue até a pasta do seu projeto e rode o comando:

		bundle install

Logo após, inicie o servidor e acesse o seu navegador para ver sua aplicação funcionando.

		rails s

O servidor, por padrão, roda na porta 3000, então entre no seu navegador e digite o endereço abaixo para ver sua aplicação rodando:
	
		localhost:3000

## Observações

A aplicação está rodando com o sqlite3, que já vem como padrão, caso não especifiquemos outro, recomendo a instalação de outro banco de dados mais robusto para colocar a sua aplicação em produção, MySQL ou Postgresql, por exemplo.
Você também precisará de um editor de texto, ou uma IDE, o que melhor lhe convier.


### OPCIONAL

### Instalando MySQL

		sudo apt-get install mysql-client libmysqld-dev

Logo após:
		
		gem install mysql2

### Instalando o PostgreSQL

		sudo apt-get install postgresql-9.3 libpq-dev

Então:
		
		gem install pg

## Instalando o Sublime-text

Um dos editores de texto mais usados para desenvolvimento web, e na minha opinião, um dos melhores.
		
		sudo add-apt-repository ppa:webupd8team/sublime-text-3 

Depois:
	
		sudo apt-get update

E para finalizar:
		
		sudo apt-get install sublime-text-installer