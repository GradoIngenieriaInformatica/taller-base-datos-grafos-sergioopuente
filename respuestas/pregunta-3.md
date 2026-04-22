MATCH (p:Persona)-[:AMIGO_DE]->(a:Persona)
WITH p, count(a) AS numAmigos
WHERE numAmigos >= 1
RETURN p.nombre, numAmigos