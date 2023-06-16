# revisao 
- os basicos crud
- store procedure
- fazer transactions, rollback, commi e savepoint
- hot backup
- cold backup
- backup incremental 
- backup full
- restore
- dado x metadado
- view normal e materialized
- transactions
- autocommit, savepoint, rollback e commit

## hot backup
conhecido como backup online/dinâmico
> kaaka

## cold backup
conhecido como backup offline/estático <br></br>
backup quando a aplicação/database não ta rodando e não pode ser acessada por ninguém

> Desvantagens:
> - ninguém pode mexer
<br></br>
> Vantagens:
> - melhora a segurança dos dados
> - consistência dos dados (ja que ta desligado, nao tem nenhuma operação acontecendo, evitando dados corrompidos ou então não gravados durante o backup)

## backup incremental
de período em período, exemplo: a cada cinco minutos, a cada vinte e quatro horas... Depois do backup incremental o backup full é feito para guardar todos esses conjuntos e depois de um tempo o incremental é apagado(ex: dois dias)<br></br>
nao faz sentindo backup cold ser incremental, normalmente é hot

## backup full
faz sentido o backup ser cold 

## restore 
depois que faz o backup, a gente resgata ele pra ver se ta funcionando

## metadado
estrutura do dado, exemplo -> quando estamos dando select em uma tabela, a tabela é um metadado. Estrutura de sistemas (tabelas internas)
> a tabela USER_TABLES é uma meta-tabela que possui informações a respeito das tabelas criadas pelos usuários. 

## views
comando: create view as select tal tal tal
ou: create materialized view *nome* as tal tal<br></br>
a diferença é que a view materialized vai criar uma copia do select que usamos e dixa pronto pra quando precisar, e ai é feito o refresh, são indicados para dados que são apenas consultados.<br></br>
Já a view normal realiza uma consulta (query) em tempo de execução

## transactions


# links uteis
https://storware.eu/blog/pros-and-cons-of-cold-backup-and-hot-backup-comparison/
