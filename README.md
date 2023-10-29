# Tema-Base-de-Dados-Animais
## Nesta atividade utilizamos os metodos de selecionar itens na tabela, e utilizamos os metodos de criação de dados dentro das tabelas.

# Etapa 1
### 1- Selecione todos os animais
![1- Selecione todos os animais](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/e1405128-d769-49d7-834a-0b18a0f5ff31)


### 2- Selecione todos os animais que pesam menos que 13.1
![2- Selecione todos os animais que pesam menos que 13 1](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/f4204817-d57a-4bdc-9b4c-1fe62393e488)

### 3- Selecione todos nasceram entre fevereiro e dezembro de 2015
![3- Selecione todos nasceram entre fevereiro e dezembro de 2015](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/a6e6520b-ea39-4e23-bcca-27c2d6bcc5ab)


### 4- Selecione todos os animais brancos que pesam menos que 15.0
![4- Selecione todos os animais brancos que pesam menos que 15 0](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/cc4be990-205f-4bb0-b9a2-7eee1aba2de1)

### 5- Selecione nome, cor e peso de todos cujo nome comece com ’B’
![5- Selecione nome, cor e peso de todos cujo nome comece com ’B’](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/e1b456ac-d1b5-4d0e-81ec-0c95046c542e)

### 6- Selecione nome, cor e peso de todos com cor vermelha, amarela, marrom e laranja
![6- Selecione nome, cor e peso de todos com cor vermelha, amarela, marrom e laranja](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/487e078c-fa61-49ca-b554-eb38aa720bec)

### 7- Selecione nome, cor, data de nascimento e peso de todos ordenados pelos mais jovens
![7- Selecione nome, cor, data de nascimento e peso de todos ordenados pelos mais jovens](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/2e37d7c5-3e4e-45d9-b7ae-7712d26c0093)

### 8- Selecione todos os animais cujo nome comece com 'C' e não sejam brancos
![8- Selecione todos os animais cujo nome comece com 'C' e não sejam brancos](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/5d1f5aa7-dbcf-44c8-8bf5-01c75808002a)

### 9- Selecione todos os animais cujo nome contenha 'ba'
![9- Selecione todos os animais cujo nome contenha 'ba'](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/441ad84e-01c2-4617-958d-8165f4009ab6)

### 10- Selecione todos os animais com peso entre 13.0 à 15.0
![10- Selecione todos os animais com peso entre 13 0 à 15 0](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/a3c26078-06d7-4d00-9911-8547e4c80183)

### 11- Selecione todos os animais que o peso não seja maior que 30, com cor amarelo ou roxo e nascidos depois de 2012
![11 - Selecione todos os animais que o peso não seja maior que 30, com cor amarelo ou roxo e nascidos depois de 2012](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/24118d6c-e94c-4d03-bab9-ec9326a71cea)

## 12- (Desafio) Selecione todos os capricornianos
![(Desafio) Selecione todos os capricornianos](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/eb08fc89-a315-4d89-b4f5-8da221a0dee1)


## Nesta etapa iremos criar tabelas que terao relação entre si, sendo criado um modelo de diagrama para mostrar a ligação entre si 

# Etapa 2 

### 1) Crie um banco de dados para armazenar dados de Animais e Espécies. Um animal tem seu nome, data_nasc e peso. Uma espécie tem um nome e uma descrição.
![Animais e especie](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/2f123ffe-501f-419c-85c4-3c643242d57b)
#### Tabela animal
```SQL
CREATE TABLE tab_animal(
id integer PRIMARY KEY auto_increment,
  nome varchar(100),
  data_nasc datetime,
  peso decimal(4,2)
);

INSERT INTO tab_animal(nome, data_nasc, peso)
  VALUES ("Fido", "2018-03-10", 14.4),
         ("Whiskers", "2019-01-05", 5.5),
         ("Bella", "2017-08-20", 25.0),
         ("Simba", "2020-06-12", 12.0),
         ("Luna", "2016-09-08", 7.2),
         ("Rex", "2019-05-15", 18.2),
         ("Luna", "2020-09-20", 10.8),
         ("max", "2017-12-02", 22.1);

select * from tab_animal
```
#### Tabela Especie
```SQL
CREATE TABLE tab_especie(
id integer PRIMARY KEY AUTO_INCREMENT,
  nome varchar(100),
  descricao varcahr(1000));
  
  INSERT INTO tab_especie (nome,descricao)
  VALUES ("Leao","conhecido por ser carnivoro"),
  ("Girafa"," mamíferos terrestres mais altos do planeta"),
  ("Polvo","são conhecidos por sua inteligência notavel no reino dos invertebrados")
```
### 2) Crie um banco de dados para registrar dados de Produtos e Marcas. Um produto deve ter nome, preço de custo, preço de venda, data de validade e marca. Uma marca deve ter, nome, site oficial e telefone.
![produtos e marca](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/c3cbeb5a-f014-4efe-b101-ec0b0e8fe1f8)
#### Tabela Produto
```SQL
CREATE TABLE tab_produtos(
id integer PRIMARY KEY AUTO_INCREMENT,
  nome varchar(20), 
preço_custo decimal (9,2), 
preço_venda decimal (9,2), 
data_validade datetime,
marca varchar (30));

INSERT into tab_produtos (nome,preco_custo,preco_venda,data_validade,marca)
values ("Leite Desnatado",1.50 "por litro",2.99 "por litro","2023-12-15","Parmalat"),
("Queijo Mussarela",8.00 "por kg",15.99 "por kg","2023-11-30","Tirolez"),
("Sabonete Líquido",3.00 "por frasco",5.99 "por frasco","2024-05-10","Dove"),
("Iogurte Natural",2.00 "por unidade",3.49 "por unidade","2023-10-05","Danone"),
("Camiseta Estampada",10.00 "por peça",19.99 "por peça", "N/A","H&M"),
("Pasta de Dentes",2.50 "por tubo",4.99 "por tubo","2023-09-30","Colgate"),
("Barras de Cereal"1.20 "por barra",2.49 "por barra","2024-04-15","Nature Valley"),
("Pão de Forma Integral",2.50 "por pacote",4.99 "por pacote","2023-09-25","Wickbold"),
```
#### Tabela Marcas
```SQL
CREATE table tab_marca(
id integer PRIMARY KEY AUTO_INCREMENT,
  nome varcahr (30),
  site_oficial varcahr (50), 
  telefone int);

INSERT INTO tab_marca (nome,site_oficial,telefone)
values ("TechWorld Electronics","www.techworld-electronics.com","(12)456-7890"),
("EcoGreen Foods","www.ecogreen-foods.com","(11)123-4567"),
("Fashionista Boutique","www.fashionista-boutique.com","(19)654-3210")
```

### 3) Crie um banco de dados para registrar dados de Filmes e Categorias. Um filme tem seu título, sinopse, estudio e categoria. Uma categoria deve ter nome e público alvo.
![Filme e categoria](https://github.com/GabrielChagasAlves/Tema-Base-de-Dados-Animais/assets/125607847/915028d7-d307-4d42-9f1d-96c59667d1eb)
#### Tabela Filmes
```SQL
CREATE TABLE tab_filme(
id integer PRIMARY KEY AUTO_INCREMENT,
  título varchar (20), 
  sinopse varchar (300), 
  estudio varchar (40),
  categoria varchar (40));
  
  INSERT INTO tab_filme (título,sinopse,estudio,categoria)
  values ("A Conspiração Alquímica","Um professor de história descobre um antigo segredo que o leva a uma busca frenética por um tesouro perdido. Ele deve decifrar enigmas alquímicos e enfrentar perigos mortais para desvendar a verdade antes que seja tarde demais.","Mystic Films","Aventura/Mistério"),

  ("A Última Fronteira","Em um futuro distópico, a humanidade busca um novo lar em um planeta distante. Uma equipe de exploradores embarca em uma jornada perigosa através do espaço sideral, enfrentando desafios intergalácticos e revelações surpreendentes.","Galaxy Studios","Ficção Científica/Ação"),

  ("Amor em Paris","Uma história de amor envolvente se desenrola nas ruas pitorescas de Paris, enquanto dois estranhos se encontram e embarcam em uma jornada romântica pela cidade do amor.","Romance Films","Romance/Drama"),

  ("O Mistério do Assassino das Sombras","Um detetive brilhante investiga uma série de assassinatos brutais que deixam uma cidade aterrorizada. Conforme ele se aprofunda no caso, descobre segredos sombrios que o levarão a questionar sua própria sanidade.","DarkMystery Productions","Suspense/Crime"),

("Aventura na Selva Perdida","Um grupo de exploradores se aventura na selva amazônica em busca de uma lendária cidade perdida. Eles enfrentam perigos naturais, animais selvagens e conflitos internos enquanto buscam a descoberta que mudará suas vidas.","JungleQuest Entertainment","Ação/Aventura"),

("O Enigma da Mente","Um neurocientista renomado cria uma máquina que permite a exploração da mente humana. Quando ele voluntariamente entra na mente de um paciente com amnésia, ele descobre segredos profundos e perturbadores que desafiam a compreensão da realidade.","MindScape Films","Científica/Thriller"),

("Desejo Proibido","Em uma pequena cidade, dois amigos de infância reacendem uma paixão proibida que ameaça abalar suas vidas e as relações com suas famílias. Eles lutam contra a pressão social e moral para buscar a felicidade.","Forbidden Love Pictures","Drama/Romance"),

("O Mistério do Antigo Templo","Uma equipe de arqueólogos descobre um antigo templo escondido nas profundezas da selva. Enquanto exploram suas passagens misteriosas, eles desencadeiam forças antigas que ameaçam a humanidade.","ArchaeoAdventure Films","Aventura/Mistério");
```

#### Tabela Categoria
```SQL
CREATE TABLE tab_categoria(
id integer PRIMARY KEY AUTO_INCREMENT,
  nome varchar (20),
  publico_alvo varchar (30));
  
  INSERT INTO tab_categoria ( nome,publico_alvo)
  values ("Ação Espetacular","Entusiastas de filmes de ação, adolescentes e adultos"),
("Romances Encantadores","Românticos incuráveis, casais apaixonados"),
("Mistérios Intrigantes","Amantes de enigmas e fãs de suspense");
```
