# Respostinhas...🎯 Para quem esse Oscar vai?

* Quantos Oscars Natalie Portman ganhou? 🏆

R: 1

Q:
```sql
select count(*) from indicados_ao_oscar where nome_do_indicado like "%Natalie Portman%" and vencedor = "true";
```

---

* Amy Adams já ganhou algum Oscar? 🎭

R: Não, nenhum.

Q:
```sql
 select nome_do_indicado, vencedor from indicados_ao_oscar where nome_do_indicado like "%Amy Adams%";
```

---

* A série de filmes Toy Story ganhou um Oscar em quais anos? 👢
R: Já, o Toy Story 3 e 4 nos anos de 2011 e 2020

Q:
```sql
 select * from indicados_ao_oscar where nome_do_filme like "%toy story%" and vencedor = "true";
```

---

* A partir de que ano que a categoria "Actress" deixa de existir? 🎀

R: A partir de 1976 não há dados de Actress.

Q:
```sql
select ano_cerimonia, categoria from indicados_ao_oscar where categoria = "Actress" order by ano_cerimonia desc limit 1;
```

---

* Quem ganhou o primeiro Oscar para Melhor Atriz? Em que ano? 👠

R: Janet Gaynor

Q:
```sql
 SELECT * FROM indicados_ao_oscar WHERE categoria= "ACTRESS" AND vencedor = "true" limit 1;
```

---

* Na campo "Vencedor", altere todos os valores com "true" para 1 e todos os valores "false" para 0. 📌

R: Feito

Q:
```sql
UPDATE indicados_ao_oscar
SET vencedor = "1"
WHERE vencedor = "true";

UPDATE indicados_ao_oscar
SET vencedor = "0"
WHERE vencedor = "false";
```

---

* Em qual edição do Oscar "Crash" concorreu ao Oscar? 📸

R: 78

Q:
```sql
select * from indicados_ao_oscar where nome_do_filme like "Crash";
```

---

* O filme Central do Brasil aparece no Oscar? ⚽

R: Aparece duas vezes mas não ganhou nenhuma.

Q:
```sql
select * from indicados_ao_oscar where nome_do_filme = "central station";
```

---

