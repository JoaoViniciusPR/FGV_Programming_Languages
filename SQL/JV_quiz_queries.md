Sobre o banco de dados "classicmodels", indique as queries para obter as seguintes informações:

- Quantos registros há na tabela "customers"?
    select count(*) from customers 122
    
- Na tabela "customers", quantos clientes ("customerName") têm nome iniciado pela letra "M"?
    select count(*) from customers where customerName like "M%" 14
    
- Na tabela "customers", crie uma saída que concatene nomes e sobrenomes em uma única coluna.
    select concat(contactFirstName," ", contactLastName) as Other from customers
    
- Agora repita a query acima, mas com todas as letras em maiúsculo, e ordene pelo sobrenome.
    select upper(concat(contactFirstName," ", contactLastName)) as Other from customers order by contactLastName
    
- Na tabela "payments", selecione os registros ordenados por volume ("amount") e data de pagamento ("paymentDate")
    select * from payments order by amount ASC, paymentDate ASC
    
- Na tabela "employees", indique quantos nomes de cargos ("jobTitle") únicos existem?
    select count(distinct(jobTitle)) from employees 7
    
- Qual destes cargos ("jobTitle") possuem mais funcionários?
    select count(jobtitle) from employees where jobTitle = "President";
    select count(jobtitle) from employees where jobTitle = "VP Sales";
    select count(jobtitle) from employees where jobTitle = "VP Marketing";
    select count(jobtitle) from employees where jobTitle = "Sales Manager (APAC)";
    select count(jobtitle) from employees where jobTitle = "Sale Manager (EMEA)";
    select count(jobtitle) from employees where jobTitle = "Sales Manager (NA)";
    select count(jobtitle) from employees where jobTitle = "Sales Rep";