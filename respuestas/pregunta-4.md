MATCH (p:Persona)-[:TRABAJA_EN]->(e:Empresa)
RETURN p.nombre, count(e) AS numEmpresas
ORDER BY numEmpresas DESC