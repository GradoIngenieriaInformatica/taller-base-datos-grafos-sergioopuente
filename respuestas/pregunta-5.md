MATCH (p:Persona)-[:AMIGO_DE]->(a:Persona)-[:PARTICIPA_EN]->(proyAmigo:Proyecto)
WHERE NOT (p)-[:PARTICIPA_EN]->(proyAmigo)
RETURN DISTINCT p.nombre AS persona, 
       a.nombre AS amigo, 
       proyAmigo.nombre AS proyectoDelAmigo
       