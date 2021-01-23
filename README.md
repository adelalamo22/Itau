# Itau
## Transacciones: 
Es la tabla que mas informacion nos aporta en el modelo.
Como el objetivo es predecir el último trimestre, nos decidimos a juntar los dos datasets de train y test y agrupar por trimestres. 
Hacemos un feature engeniering sacando las lags variables hacia atrás en el tiempo, unos 5 trimestres hacia atrás para
cada una de las variables creadas en el agrupamiento trimestral.

## Comunicaciones:
Hacemos tambien agrupamientos y sacamos las variables hacia atras. 

## Modelo:
Unimos Todos los dataset anteiores ya con su FE realizado. 
Sacamos unas variables Meanencoder "contaminadas" con algo de información del target (Es un concurso...). Previamente hemos comprobado que no comprometen la
integridad del modelo y que este funciona de forma correcta en nuestras pruebas. 
Hacemos un rebalanceo del dataset final ya que este contiene mucha informacion de clientes que no han comprado nuetros productos y esta
introduciendo un sesgo a nuestro modelo. 
Procesamos artesanalmente la prediccion para mandar los datos con el formato solicitado por el cliente.

