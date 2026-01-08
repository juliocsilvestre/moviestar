# 🎬 MovieStar

Sistema web de avaliação e crítica de filmes desenvolvido em PHP puro com arquitetura MVC.

## 📋 Sobre o Projeto

O MovieStar é uma plataforma onde usuários podem:

- Cadastrar e gerenciar filmes
- Escrever reviews e avaliar filmes com notas
- Visualizar filmes por categorias (Ação, Comédia, etc.)
- Gerenciar perfil de usuário
- Buscar filmes no catálogo

## 🚀 Tecnologias Utilizadas

- **PHP** - Linguagem de programação do backend
- **MySQL** - Banco de dados relacional
- **PDO** - Interface de acesso ao banco de dados
- **HTML/CSS** - Estrutura e estilização das páginas
- **Bootstrap/CSS personalizado** - Framework CSS
- **Arquitetura MVC** - Padrão de organização do código
  - Models: Representação das entidades (Movie, User, Review, Message)
  - DAO (Data Access Object): Camada de acesso aos dados
  - Views: Templates de apresentação

## 📁 Estrutura do Projeto

```
moviestar/
├── css/                    # Arquivos de estilo
├── dao/                    # Data Access Objects
│   ├── MovieDAO.php
│   ├── ReviewDAO.php
│   └── UserDAO.php
├── img/                    # Imagens do sistema
│   ├── movies/            # Capas dos filmes
│   └── users/             # Fotos dos usuários
├── models/                 # Classes de modelo
│   ├── Movie.php
│   ├── User.php
│   ├── Review.php
│   └── Message.php
├── templates/              # Templates reutilizáveis
│   ├── header.php
│   ├── footer.php
│   ├── movie_card.php
│   └── user_review.php
├── auth.php               # Página de autenticação
├── auth_process.php       # Processamento de login/registro
├── dashboard.php          # Dashboard do usuário
├── db.php                 # Configuração do banco de dados
├── globals.php            # Variáveis globais
├── index.php              # Página inicial
├── movie.php              # Detalhes do filme
├── movie_process.php      # Processamento de filmes
├── newmovie.php           # Cadastro de novo filme
├── editmovie.php          # Edição de filme
├── profile.php            # Perfil do usuário
├── editprofile.php        # Edição de perfil
├── review_process.php     # Processamento de reviews
├── search.php             # Busca de filmes
└── user_process.php       # Processamento de usuários
```

## 🔧 Pré-requisitos

- PHP 7.4 ou superior
- MySQL 5.7 ou superior
- Servidor web (Apache/XAMPP/WAMP/LAMP)
- Extensões PHP: PDO, pdo_mysql

## ⚙️ Como Rodar o Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/juliocsilvestre/moviestar.git
cd moviestar
```

### 2. Configure o banco de dados

Crie um banco de dados MySQL chamado `moviestar`:

```sql
CREATE DATABASE moviestar;
```

### 3. Configure a conexão com o banco

Edite o arquivo `db.php` com suas credenciais do MySQL:

```php
$db_name = "moviestar";
$db_host = "localhost";
$db_user = "root";        // Seu usuário MySQL
$db_pass = "";            // Sua senha MySQL
```

### 4. Importe as tabelas do banco de dados

Execute o script SQL para criar as tabelas necessárias (users, movies, reviews).

### 5. Configure o servidor web

**Opção A: Usando XAMPP/WAMP**

- Copie a pasta do projeto para `htdocs` (XAMPP) ou `www` (WAMP)
- Inicie o Apache e MySQL
- Acesse: `http://localhost/moviestar`

**Opção B: Usando PHP Built-in Server**

```bash
php -S localhost:8000
```

- Acesse: `http://localhost:8000`

### 6. Crie as pastas de upload (se necessário)

Certifique-se de que as pastas de imagens têm permissão de escrita:

```bash
chmod 777 img/movies
chmod 777 img/users
```

## 📝 Funcionalidades

- ✅ Sistema de autenticação (login/registro)
- ✅ CRUD completo de filmes
- ✅ Sistema de avaliações e reviews
- ✅ Upload de imagens (capa do filme e foto do usuário)
- ✅ Categorização de filmes
- ✅ Sistema de busca
- ✅ Cálculo automático de rating médio
- ✅ Dashboard personalizado do usuário
- ✅ Sistema de mensagens (feedback)

## 👤 Autor

**Júlio César Silvestre**

- GitHub: [@juliocsilvestre](https://github.com/juliocsilvestre)
- Email: jcss.silvestre@gmail.com

## 📄 Licença

Este projeto está sob a licença MIT.

---

⭐ Se este projeto foi útil para você, deixe uma estrela no repositório!
