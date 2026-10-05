# Agenda Eletrônica em PHP com PDO e MySQL

Sistema de gerenciamento de contatos e usuários desenvolvido em PHP com orientação a objetos e PDO, utilizando banco de dados MySQL e interface responsiva baseada no template AdminLTE.

## Sobre o Projeto

A Agenda Eletrônica é uma aplicação web completa que permite o cadastro, a listagem, a edição e a exclusão (CRUD) de contatos, além de um sistema de autenticação de usuários com controle de acesso por sessões.

O projeto foi construído focando em boas práticas de desenvolvimento web, incluindo separação modular de leiaute com include_once, proteção contra SQL Injection através de Prepared Statements do PDO e manipulação de upload de arquivos de imagem.

## Funcionalidades

### Autenticação e Segurança
- Login e registro de usuários com controle de acesso por sessão.
- Proteção contra SQL Injection utilizando consultas preparadas (prepare e bindValue) com a extensão PDO.
- Tratamento de exceções na conexão com o banco de dados via blocos try/catch.

### Gerenciamento de Contatos (CRUD)
- Cadastro de contatos com dados pessoais e upload de imagem de perfil.
- Listagem dinâmica de contatos cadastrados integrada ao DataTables para busca, paginação e ordenação.
- Edição de contatos com preservação da imagem existente caso uma nova foto não seja enviada.
- Exclusão de registros do banco de dados e remoção do arquivo de imagem do servidor via comando unlink.

### Gerenciamento de Uploads
- Validação das extensões de imagem permitidas (jpg, jpeg, png, gif).
- Geração de identificadores únicos para arquivos via uniqid para evitar sobreposição de nomes.
- Armazenamento organizado no diretório de imagens do servidor.

## Tecnologias Utilizadas

- Backend: PHP
- Banco de Dados: MySQL / MariaDB
- Driver de Conexão: PHP Data Objects (PDO)
- Frontend: HTML5, CSS3, JavaScript, jQuery, Bootstrap, AdminLTE Template
- Recurso Adicional: DataTables

## Estrutura de Diretórios

| Diretório / Arquivo | Descrição |
| :--- | :--- |

| **config/conexao.php** | Configuração e inicialização da conexão PDO com o banco de dados. |

| **dist/** | Arquivos estáticos do AdminLTE (folhas de estilo CSS e scripts JS). |

| **plugins/** | Bibliotecas de terceiros (jQuery, DataTables, FontAwesome). |

| **img/cont/** | Armazenamento das fotos de perfil dos contatos enviadas via upload. |

| **paginas/includes/** | Módulos reutilizáveis de leiaute (topo.php, menu.php, rodape.php). |

| **paginas/conteudo/cadastro_contato.php** | Formulário de cadastro de novos contatos. |

| **paginas/conteudo/listagem_contatos.php** | Tabela dinâmica de exibição dos contatos cadastrados. |

| **paginas/conteudo/update_contato.php** | Formulário e processamento de edição de dados. |

| **paginas/conteudo/deletar_contato.php** | Lógica de remoção de registros e exclusão física da foto. |

| **paginas/conteudo/perfil.php** | Interface de edição de dados e foto do usuário logado. |

| **index.php** | Tela de login e autenticação de usuários. |

| **home.php** | Painel principal (dashboard) com carregamento modular. |

| **logout.php** | Encerramento seguro da sessão do usuário. |

| **README.md** | Documentação explicativa do repositório. |

## Como Executar o Projeto

1. Pré-requisitos:
   - Servidor web local instalado (como XAMPP, WAMP ou Apache/PHP no Linux).
   - PHP 7.4 ou superior com extensão pdo_mysql habilitada.
   - Banco de dados MySQL ou MariaDB.

2. Instalação e Configuração:
   - Baixe ou clone os arquivos na pasta pública do seu servidor web (exemplo: /var/www/html/agendaPhp ou C:/xampp/htdocs/agendaPhp).
   - Crie o banco de dados no MySQL e execute a estrutura das tabelas para usuários e contatos.
   - Configure as credenciais de acesso no arquivo config/conexao.php.
   - Ajuste as permissões de escrita para a pasta de imagens em ambientes Linux.
   - Acesse a aplicação pelo navegador no endereço http://localhost/agendaPhp/

## Licença

Este projeto foi desenvolvido para fins educacionais e demonstração de desenvolvimento web com PHP, PDO e MySQL.
