# Itau
#1 Transacciones: 
Es la tabla que mas informacion nos aporta en el modelo.
Como el objetivo es predecir el último trimestre, nos decidimos a juntar los dos datasets de train y test y agrupar por trimestres. 
Hacemos un feature engeniering sacando las lags variables hacia atrás en el tiempo, unos 5 trimestres hacia atrás para
cada una de las variables creadas en el agrupamiento trimestral.

#2 Comunicaciones:
Hacemos tambien agrupamientos y sacamos las variables hacia atras. 

#3 Modelo:
Sacamos unas variables Meanencoder "contaminadas" con algo de onformacion del target. Previamente hemos comprobado que no comprometen la
integridad del modleo y que este funciona de forma correcta. 
Unimos Todos los dataset anteiores ya con su FE realizado. 
Hacemos un rebalanceo del dataset ya que este contiene mucha informacion de clientes que no han comprado nuetros productos y esta
introduciendo un sesgo a nuestro modelo. 

