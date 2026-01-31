**Informe Trabajo 2**

**Osvaldo Ceballos**

**Yerko Fuentes**

**Paloma San Martín**

**Respuesta 1**

Al considerar el ejemplo "Rey" y sus atributos como "Figura de Poder en el reino" o "Encargado del Reino" y eliminar el concepto "Hombre" y sumar el de "Mujer". Quedaría como "Mujer encargada del reino" o "Mujer que es la figura de poder en el reino" por ende resultaría "Reina. Considerando esa base, podemos tomar ejemplos como:

Iphone - Apple + Samsung = Galaxy

Air Force One - Nike + Adidas = Adidas Original

Dolce Gusto - Nescafé + Nesspreso = Inissia Blanca

Nescafé Tradición - Nescafé + Juan Valdes = Café Campesino

Restaurant - Comida + Café = Cafeterias

Starbucks - Café + Donuts = Dunking Donnuts

Considerarían la misma lógica del concepto inicial que engloba todo y deriva hacia otro concepto manteniendo la "forma" de lo que representa enviado hacia otra marca.

**Respuesta 2**

"Al comparar los F1-Scores, observamos que el modelo basado en BERT superó al Baseline de TF-IDF (ej. 0.89 vs 0.75). Al inspeccionar los errores, notamos que TF-IDF fallaba consistentemente en frases con negaciones ('No es nada mala') o frases adversativas ('Tiene buenos efectos, pero la historia es terrible'), clasificándolas incorrectamente basándose solo en la presencia de palabras aisladas como 'mala' o 'buenos'. BERT, gracias a su mecanismo de atención, logró capturar correctamente el contexto sintáctico y la verdadera intención de estas críticas."

**Respuesta 3**

- RMSE bajo indica lo preciso de la predicción de evaluación de lo que se quiere predecir (canciones, películas Restaurantes) no necesariamente es preciso con los gustos específicos de la persona. Por ejemplo, si una persona escucha música de muchos géneros, el RMSE va a representar precisión entre lo evaluado y podrá predecir los gustos, pero si tenemos una persona que solo escucha un solo género, se pierde la capacidad de sugerencia, independiente de un error cuadrado bajo.

- Primero es hacer una consulta de referencia, con respecto a los datos.
- Trataría de inducir que se conecte con "amigos".
- Luego aplicaría un ALS sobre las preferencias de los "amigos".
- En el tiempo trataría de ponderar las preferencias ajenas con menor fuerza, debido a que el cold start solo representa el principio contractual del uso de un servicio.

**Respuesta 4**

El sistema de confianza se basa en puntuación, por lo que se genera una "disonancia" entre "No la conozco" o "Nunca la he escuchado" y "No me gusta", por lo que ambas

tienen 0 puntos. Lo que utiliza el modelo ALS es ponderar ese 0 de distinta manera según la cantidad de oyentes que ya posee le canción sin asociarlas al usuario.

- Si la canción se ha reproducido 0 veces, entonces posee baja confianza, pero con un valor 0
- Si se ha reproducido 1000 veces poseemos alta confianza, pero con valor 1

NDCG penaliza el orden: "A diferencia de Precision@K, que es una métrica binaria (¿está el ítem relevante en la lista? Sí/No) y le da igual si está en la posición 1 o en la 5, el NDCG (Normalized Discounted Cumulative Gain) valora la posición. Utiliza un descuento logarítmico en el denominador. Si el algoritmo coloca la canción favorita del usuario (relevancia real) en la posición 5, el 'score' que gana es mucho menor que si la hubiera puesto en la posición 1. NDCG entiende que el usuario presta mucha más atención a los primeros resultados."

**Respuesta 5**

**¿por qué un modelo de sentimiento global sería peligroso en estos casos?**

Para un sistema de CRM automatizado, esto es peligroso porque el sistema ignoraría esta reseña (al verla 'Positiva') y no generaría un ticket de soporte. El cliente tiene un problema logístico grave que la empresa pasará por alto por culpa del 'promedio' de sentimiento.

**¿qué riesgo estratégico corre el retailer a largo plazo en términos de descubrimiento de productos y saturación de usuarios?**

El modelo sufre de sesgo de popularidad. Se concentra en la 'cabeza' (head) de la distribución, recomendando los éxitos de ventas a todo el mundo, e ignora la 'Long Tail' (cola larga), que son esos productos de nicho que generan valor específico para usuarios con gustos particulares.

**Evaluación: Compara el Top-10 original vs. el Top-10 re-rankeado para un usuario. ¿Cuántos ítems cambiaron?**

**¿Es sostenible "empujar" productos caros si son levemente menos relevantes?**

No es sostenible si se hace de forma agresiva. Los sistemas de recomendación funcionan gracias a la confianza implícita: el usuario cree que el algoritmo le muestra lo que 'es mejor para él'. Si el usuario percibe que el sitio solo le quiere vender lo más caro (y no lo más relevante), la confianza se rompe y aumenta el Churn Rate (tasa de abandono). La estrategia ideal es un equilibrio sutil: promover productos de alto margen solo cuando la diferencia de relevancia con el producto 'barato' sea mínima, actuando como un 'desempate' y no como una imposición
