MATCH (a:Persona)-[:AMIGO_DE*2]->(b:Persona)
WHERE NOT (a)-[:AMIGO_DE]->(b) AND a <> b
RETURN a.nombre, b.nombre
