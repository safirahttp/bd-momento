#Momento!

##### A Momento é uma empresa única que faz o melhor que pode para alcançar o melhor da humanidade.

### 1. Inclua suas próprias informações no departamento de tecnologia da empresa.

<code> INSERT INTO funcionarios (funcionario_id, primeiro_nome, sobrenome, email, telefone, dataContratacao, ocupacao_id, salario, departamento_id) VALUES ('Ellen', 'Silva', 'ellen.silva@momento.org', '515.123.8888', '2022-07-08', 9, 4000.00, 6); </code>

### 2. A administração está sem funcionários. Inclua os outros elementos do seu grupo do demoday no departamento de administração.

<code> INSERT INTO funcionarios (funcionario_id, primeiro_nome, sobrenome, email, telefone, dataContratacao, ocupacao_id, salario, departamento_id) VALUES (208, 'Gustavo', 'Amorim', 'gustav.amorims@momento.org', '515.123.8282', '2022-07-08', 3, 3000.00, 1); </code>
<code> INSERT INTO funcionarios (funcionario_id, primeiro_nome, sobrenome, email, telefone, dataContratacao, ocupacao_id, salario, departamento_id) VALUES (209, 'Daniele', 'Simões', 'daniele.simoes@momento.org', '515.123.8383', '2022-07-08', 3, 3000.00, 1); </code>
<code> INSERT INTO funcionarios (funcionario_id, primeiro_nome, sobrenome, email, telefone, dataContratacao, ocupacao_id, salario, departamento_id) VALUES (210, 'Jonathan', 'Ferreira', 'john.ferreira@momento.org', '515.123.8484', '2022-07-08', 3, 3000.00, 1); </code>
<code> INSERT INTO funcionarios (funcionario_id, primeiro_nome, sobrenome, email, telefone, dataContratacao, ocupacao_id, salario, departamento_id) VALUES (211, 'Leonardo','Vinicius', 'leonardo.vinicius@momento.org', '515.123.8585', '2022-07-08', 3, 3000.00, 1); </code>
<code> INSERT INTO funcionarios (funcionario_id, primeiro_nome, sobrenome, email, telefone,dataContratacao, ocupacao_id, salario, departamento_id) VALUES (212, 'Thiago', 'Antenor', 'antenor.thiago@momento.org', '515.123.8686', '2022-07-08', 3, 3000.00, 1); </code>
<code> INSERT INTO funcionarios (funcionario_id, primeiro_nome, sobrenome, email, telefone, dataContratacao, ocupacao_id, salario, departamento_id) VALUES (213, 'Gabriel', 'Marques', 'gab.marques@momento.org', '515.123.8787', '2022-07-08', 3, 3000.00, 1); </code>

### 3. Agora diga, quantos funcionários temos ao total na empresa?

## 47 funcionários.
<code> SELECT COUNT(*) FROM `funcionarios` </code>

### 4. Quantos funcionários temos no departamento de finanças?

## Sâo 6 funcionários no total.
<code> SELECT * FROM `funcionarios` WHERE `departamento_id` = 10; </code>

#### 5. Qual a média salarial do departamento de tecnologia?

## A média salarial do departamento de tecnologia é 5466.66.
<code> SELECT AVG(salario) FROM `funcionarios` WHERE `departamento_id` = 6; </code>

#### 6. Quanto o departamento de Transportes gasta em salários?

## O departamento de transportes gasta 41200.00.
<code> SELECT SUM(salario) FROM `funcionarios` WHERE `departamento_id` = 5; </code>

#### 7. Um novo departamento foi criado. O departamento de inovações. Ele será locado no Brasil. Por favor, adicione-o no banco de dados.

<code> INSERT INTO departamento (departamento_name, posicao_id) VALUES ('Inovações', 5400); </code>

#### 8. Novos Funcionários!
Três novos funcionários foram contratados para o departamento de inovações. Por favor, adicione-os: William Ferreira, casado com Inara Ferreira, possui um filho chamado Gabriel que tem 4 anos e adora brincar com cachorros. Ele será programador.Já a Fernanda Lima, que é casada com o Rodrigo, não possui filhos. Ela vai ocupar a posição de desenvolvedora.  Por último, a Gerente do departamento será Fabiana Raulino. Casada, duas filhas (Maya e Laura). 

O salário de todos eles será a média salarial dos departamentos de administração e finanças. 

## Funcionários
<code> -- William Ferreira

INSERT INTO funcionarios (primeiro_nome, sobrenome, email, telefone, dataContratacao, ocupacao_id, salario, departamento_id) VALUES ('William', 'Ferreira', 'william.ferreira@momento.org', '515.123.8989','2022-07-08', 9, 9000.00, 12); </code>

<code> -- Fernanda Lima

INSERT INTO funcionarios (primeiro_nome, sobrenome, email, telefone, dataContratacao, ocupacao_id, salario, departamento_id) 
VALUES ('Fernanda', 'Lima', 'fernanda.lima@momento.org', '515.123.9090', '2022-07-08', 9, 10000.00, 12); </code>

<code> -- Fabiana Raulino

INSERT INTO funcionarios (primeiro_nome, sobrenome, email, telefone, dataContratacao, ocupacao_id, salario, departamento_id) VALUES ('Fabiana', 'Raulino', 'fabiana.raulino@momento.org', '515.123.9191', '2022-07-08', 7, 20000.00, 12); </code>

## Dependentes

<code> -- Inara Ferreira

INSERT INTO dependentes (primeiro_nome, sobrenome, parentesco, funcionario_id) VALUES ('Inara', 'Ferreira', 'esposa', 218)

-- Gabriel Ferreira

INSERT INTO dependentes (primeiro_nome, sobrenome, parentesco, funcionario_id) VALUES ('Gabriel', 'Ferreira', 'filho', 218) </code>

<code> -- Rodrigo Lima

INSERT INTO dependentes (primeiro_nome, sobrenome, parentesco, funcionario_id) VALUES ('Rodrigo', 'Lima', 'marido', 219) </code>

<code> -- Maya Raulino

INSERT INTO dependentes (primeiro_nome, sobrenome, parentesco, funcionario_id) VALUES ('Maya', 'Raulino', 'filha', 220)

-- Laura Raulino

INSERT INTO dependentes (primeiro_nome, sobrenome, parentesco, funcionario_id) VALUES ('Laura', 'Raulino', 'filha', 220) </code>

#### 9. Informe todas as regiões em que a empresa atua acompanhadas de seus países.

<code> SELECT paises.pais_name AS Pais, regiao.regiao_name FROM paises INNER JOIN regiao WHERE paises.regiao_id = regiao.regiao_id; </code>

#### 10. Joe Sciarra é filho de quem?

## Ele é filho de Ismael Sciarra.
<code> SELECT funcionarios.primeiro_nome, funcionarios.sobrenome FROM dependentes INNER JOIN funcionarios WHERE dependentes.funcionario_id = funcionarios.funcionario_id AND dependentes.primeiro_nome LIKE '%Joe%' AND dependentes.sobrenome LIKE '%Sciarra%'; </code>

#### 11. Jose Manuel possui filhos?

## Jose não possui filhos.
<code> SELECT funcionarios.primeiro_nome, dependentes.primeiro_nome FROM dependentes INNER JOIN funcionarios WHERE dependentes.funcionario_id = funcionarios.funcionario_id AND dependentes.sobrenome LIKE '%Manuel%'; </code>

#### 12. Qual região possui mais países?

## A Europa, com 25 países.
<code> SELECT regiao.regiao_name, COUNT(paises.regiao_id) FROM paises INNER JOIN regiao WHERE regiao.regiao_id = paises.regiao_id; </code>

#### 13. Exiba o nome cada funcionário acompanhado de seus dependentes.

<code> SELECT funcionarios.primeiro_nome, funcionarios.sobrenome, dependentes.primeiro_nome, dependentes.sobrenome FROM funcionarios INNER JOIN dependentes WHERE funcionarios.funcionario_id = dependentes.funcionario_id; </code>

#### 14. Karen Partners possui um cônjuge?

## Sim, Alec Partners.
<code> SELECT dependentes.primeiro_nome, dependentes.sobrenome FROM dependentes INNER JOIN funcionarios WHERE funcionarios.funcionario_id = dependentes.funcionario_id AND funcionarios.primeiro_nome LIKE '%Karen%' AND funcionarios.sobrenome LIKE '%Partners%'; </code>

#### 15. O ID da tabela de países não segue um padrão numérico. Na sua visão, qual o impacto disso no desenvolvimento do banco?

## Nenhum, pois o ID atende aos requisitos da chave primaria e é identificado por siglas, por exemplo: Brasil = BR.

#### 16. Escolha um país para se mudar. Qual seria esse país? Por que escolheria esse país? E o departamento. O que seria? Como seriam seus funcionários?

## Escolheria a Noruega porque lá parece frio, gosto da cultura e das histórias e de vikings, lá tem muitos museus e coisas sobre arte, e eu gosto da língua e do sotaque deles. O departamento seria de adivinhar o dublador, escolheria meus amigos como funcionários, a gente é muito bom nisso.

#### 17. Atualize as informações na tabela para que seu departamento seja criado.

<code> INSERT INTO posicao (endereco, cidade, pais_id) VALUES ('Uranienborg ', 'Noruega', 'NO'); </code>

<code> INSERT INTO departamento (departamento_name, posicao_id) VALUES ('Adivinha', 5401); </code>
