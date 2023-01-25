# diagramaDB  
Trabalho individual do Módulo 4 do curso de Desenvolvimento WEB Fullstack em parceria com o Senac-RJ.  
Link para o diagrama: https://drive.google.com/file/d/1gZXL2IBiYZyrdYkZtjSmu23xSUGowcxZ/view?usp=sharing

# Entidades  

### Resilia:  
cnpj_empresa (pk) = INT (14)  
id_curso (fk) = INT (999)  
nome_empresa = VARCHAR (100)  
endereco_web = VARCHAR (150)  
area_atuacao = VARCHAR (50)   

### Curso:  
id_curso (pk) = INT (999)  
ementa = VARCHAR (250)  
duracao_curso = INT (9999)  
preco_padrao = INT (999999)  

### Instituicao:  

id_instituicao (pk) = INT (99999)  
id_curso (fk) = INT (999)  
cpf_facilitador (fk) = INT (11)  
id_turma (fk) = INT (999999)  
nome_instituicao = VARCHAR (100)  
pessoa_coordenadora = VARCHAR (150)  
endereco_instituicao = VARCHAR (250)  

### Aluno:  

cpf_aluno (pk) = VARCHAR (11)  
id_turma (fk) = INT (999999)  
id_instituicao (fk) = INT (99999)  
nome_aluno = VARCHAR (150)  
data_nascimento_aluno = DATE  
presenca_soft = FLOAT  
presenca_hard = FLOAT  
tipo_bolsa = VARCHAR (15)  

### Turma:  

id_turma (pk) = INT (999999)  
cpf_facilitador (fk) = INT (11)  
id_instituicao (fk) = INT (99999)  
cpf_aluno (fk) = INT (11)  
id_curso (fk) = INT (999)  
data_inicio = DATE  
data_conclusao = DATE  
horario = TIME  
turno = VARCHAR (15)  
cod_turma = VARCHAR (15)  

### Facilitador:  

cpf_facilitador (pk)  = INT (11)  
id_curso (fk) = INT (999)  
id_turma (fk) = INT (999999)  
id_instituicao (fk) = INT (99999)  
nome_facilitador = VARCHAR (150)  
data_nascimento_facilitador = DATE  
formacao = VARCHAR (200)  
salario = INT (999999)  
fixo_temporario = VARCHAR (11)  
soft_hard = VARCHAR (4)  
