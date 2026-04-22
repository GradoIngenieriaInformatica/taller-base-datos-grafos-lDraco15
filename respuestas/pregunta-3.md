MATCH (p:Persona)-[:AMIGO_DE]->(amigo)
WITH p, count(amigo) AS total
WHERE total > 1
RETURN p.nombre, total
