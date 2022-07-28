# Most-Rented-Movies-Sakila-SQL
List in descending order, the most rented movies on Sakila.SQL.
SELECT count(rental.inventory_id) AS N°_Alugueis, inventory.film_id AS ID_Filme, title AS Nome_Filme from rental
INNER JOIN sakila.inventory ON inventory.inventory_id = rental.inventory_id
inner join sakila.film on film.film_id = inventory.film_id
group by 2
order by 1 desc;
