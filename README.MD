1. Título do projeto:

- ConectaONG

2. Descrição do projeto:

- O ConectaONG é uma plataforma que tem o objetivo de conectar, de forma simples, usuários às ONGS de Fortaleza, apresentando suas necessidades de voluntários, itens e canais de contato. Com o ConectaONG, em poucos segundos qualquer pessoa poderá acessar informações da ONG escolhida, como endereço, voluntários necessários, itens em falta e formas de contato. Da mesma forma, as ONGS poderão se cadastrar e atualizar suas informações de maneira prática.

3. Problema solucionado

- As informações a cerca das ONGS são extremamente escassas e o problema fica ainda maior quando queremos saber as necessidades delas. O problema que foi solucinado é justamente essa dificuldade para encontramos informações sobre as ONGS. Criamos uma forma de ter informações sobre diversas ONGS tudo em um só lugar.

4. Lista de funcionalidades principais

- Cadastro e login
- Adição de novas ongs
- Alteração nas informações da ONGS como endereço, necessidades, fontes de contatos
- Opção de busca por texto

5. Status de implementação (completo, parcial)

- Parcial -> O ideal seria a compra de um domínio para vincular ao site

6. Screenshots das telas principais:

- Tela inicial: ![home](docs/images/home.png)
- Tela de login: ![login](docs/images/login.png)
- Tela de registro: ![register](docs/images/register.png)
- Tela de criação/edição de ong: ![edit/createong](docs/images/edit_createong.png)
- Tela de informações da ong: ![ong](docs/images/ong.png)
- Tela de ongs: ![ongs](docs/images/ongs.png)
- Tela de usuários: ![ongs](docs/images/users.png)

7. Linguagens de programação

- Typescript

8. Frameworks e bibliotecas

- Frameworks: Next.js e tailwind
- Libs: react, shadcn, zod, next-auth, bcrypt, prisma, cloudinary

9. Banco de dados

- Banco de dados: MongoDB
- Banco de imagens: Cloudinary

10. Ferramentas de desenvolvimento

- Vs code

11. Visão geral da arquitetura implementada

- Client-server

12. Componentes principais

- Header, Footer, Home, ong, Login, Registrar-se, usuários, ongs

13. Integrações realizadas

- Integração com o MongoDB para o banco de dados
- Integração com o Cloudinary para o banco de imagens

14. Pré-requisitos:

- Vs code instalado na maquina
- 1 GB de armazenamento livre na maquina

15. Passo a passo para instalação

- Abra o vs code e digite no terminal: git clone https://github.com/Jocelitoo/Projeto-Aplicado-Multiplataforma---Etapa-2.git

- Entre a pasta do projeto digitando no terminal: cd Projeto-Aplicado-Multiplataforma---Etapa-2/frontend_backend

- Instale as dependências digitando no terminal: -> npm i

- Na raiz do projeto crie o arquivo .env com os dados abaixo:

DATABASE_URL="mongodb+srv://juninhoclimeres_db_user:TI54Nb3NEMnxZ0OP@cluster0.8lt5zpv.mongodb.net/trabalho"

NEXTAUTH_SECRET='dbbdb5e7-8f4a-493c-8499-69c67c0f33fc5b7e0a9a-128a-47a2-8ed2-d834cb7c699a'
NEXTAUTH_URL="http://localhost:3000/"

NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME="dmryfrj0w"
NEXT_PUBLIC_CLOUDINARY_API_KEY="321569514144799"
CLOUDINARY_API_SECRET="3Fibmu15z7Oy9xlYVVr-EH_m28E"

NEXT_PUBLIC_BASE_URL = 'http://localhost:3000'

- Inicialize o prisma client -> npx prisma generate

- Execute o projeto -> npm run dev

- Acesse o projeto rodando na maquina: http://localhost:3000/

16. URL de acesso:

- https://conectaong.vercel.app/

17. Credenciais de teste:

- email: admin@outlook.com / senha: 12345678
- email teste@outlook.com / senha: 12345678

18. Definição específica do público-alvo

- Proprietários de ONGS que buscam mais visibilidade e voluntários/doadores de ONGS que buscam uma forma simples de ter acesso à informações sobre as ONGS.

19. Resumo do processo de validação

Por meio de uma ligação pelo wpp, foi apresentado o intuito do sistema para a Rosineide. Depois disso, questionamos se ela aceitaria analisar o sistema e retornar com seu feedback e a resposta foi sim. Assim, foi enviado para ela o link do projeto hospedado na Vercel. Após o feedback dela, fizemos algumas alterações no sistema

20. Principais feedbacks recebidos

- O público alvo achou o sistema muito interessante pois em um só lugar era possível ter acesso à informações de várias ongs de maneira fácil e intuitiva. Por conta da lógica do código, ao criar uma ONG, o usuário precisava sair da conta e entrar novamente para o sistema trazer a ONG vinculada a ele. O público alvo não gostou disso e reportou

21. Ajustes implementados

- Os dados da ONG estavam sendo puxados através do nextauth que retornava a ONG do usuário que havia feito o login, porém em caso de edição ou criação o processo de login não era feito, a consequência disso era que o sistema não retornava a ONG criada/atualizada. Então, foi alterado a lógica do código para pegar a ONG vinculada ao usuário diretamente através do prisma quando a página fosse carragada, e não quando o usuário fazia login

22. Integrantes da equipe e seus papéis:

- Italo -> Responsável pela página principal (Home)
- Daniel -> Responsável pelos formulários de login / registro
- Neto -> Responsável por configurar o banco de dados com o prisma
- Jocelito -> Responsável pelas requisições feitas pelo Server Actions
- Kaio -> Responsável por criar a página que traz informações sobre a ONG e garantir a otimização do site
- Juliana -> Responsável por verificar a responsividade e corrigir erros
