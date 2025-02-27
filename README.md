# ProyectoBlancoyNegro

En este proyecto se generara un análisis descriptivo y exploratorio a las acciones de Blanco y Negro S.A, sociedad anónima que administra un club de futbol, que cotiza acciones y diversos instrumentos financieros en la Bolsa de Santiago. Este análisis comprendera una forma de abordar los cambios del precio de las acciones para una eventual toma de decisiones de inversión. 

Se extraeran los datos de https://es.investing.com/equities/blanco-y-negro-historical-data , en un archivo csv. 





![Datos en bruto](https://github.com/user-attachments/assets/f13c837c-f3d5-499e-9821-6ba5b5e892af)




Se realizo una limpieza de datos y se crearon nuevas columnas para facilitar su proyección y lectura en Power BI, como tambien la manipulacion del set de datos en Excel. Se cambio el formato para la correcta lectura en Excel, a traves del asistente de convertidor de columnas y corregir errores de formato de fecha. Las nuevas columnas agregadas fueron variacion, que es el retorno por accion por dia, luego el año, mes y dia, se agregaron gracias a la funcion AÑO, FECHA.




![Datos transformados](https://github.com/user-attachments/assets/944b5892-99a3-47c0-8c3a-eec8271f37a7)




Este set de datos consta de 3697 precio de acciones, que abarcan un periodo de tiempo desde el 12-01-2009 hasta el 11-02-2025.





![inicio](https://github.com/user-attachments/assets/f3062f31-ccab-4967-8042-7ab5417fb8ef)





![final](https://github.com/user-attachments/assets/6ca15bf5-61d3-4381-b4c5-0364477f678b)




Una vez hecha la extracción y limpieza se realiza la exportación a Power Query. En el proceso de transformacion de datos, se realizan  operaciones de calculo de medidas con la funcion DAX, tales como: Precio máximo y minimo, retorno promedio, precios promedio y volumen total de accionens. Esto con el fin de dar un mejor manejo de la información para ser utilizada en la visualización. Tambien se utilizan los formatos correspondientes para cada columna segun sea necesario.





![tabla](https://github.com/user-attachments/assets/7bde054f-3e6b-4197-b17c-b4e719d951b4)





![medidas](https://github.com/user-attachments/assets/1c388536-26c9-4c22-8201-f1bbb4cf7efe)



Luego con la funcion CALENDAR se genero un calendario para poder visualizar y analizar los precios históricos. Se agregaron año, nombre día, mes, numero de semana, trimestres, semestre, etc. Estos son importantes para poder realizar el análisis de los datos ordenados segun el requerimiento de este.




![calendario](https://github.com/user-attachments/assets/10f718f9-43ee-4aae-bedb-0c9102e44e74)




![Calendario 2](https://github.com/user-attachments/assets/3d61c652-5384-495c-825b-7183ba03701c)



Para poder trabajar con los precios de las acciones y los datos de fecha se relaciona la nueva tabla Calendario junto con las fechas del set de datos original.



![Captura de pantalla 2025-02-27 121502](https://github.com/user-attachments/assets/6143028f-0f41-455c-9fa2-219a9696b4f8)




A continuación se procede al proceso de carga en el ambiente de Power BI para visualizar las medidas que se calcularon con anterioridad a traves de distintos graficos. Estos pueden ser segmentados por año para lograr una mejor comprensión. Se visualizan precios promedio por año, retornos promedio por año, volumen total de acciones por año y precios máximos y minimos.




![Presentacion](https://github.com/user-attachments/assets/9aff1be6-f4ae-4120-9eaf-796fcfce9470)




![medidas relevantes](https://github.com/user-attachments/assets/04dd0159-00af-4298-b040-fc769ae40371)




En el grafico de volumen de acciones podemos entender el comportamiento de las Empresas en la emisión de acciones las cuales pueden ser explicadas por diferentes razones. Las empresas pueden emitir un gran número de acciones al principio y luego reducirlas por varias razones estratégicas y financieras:

1. Emisión Inicial de Muchas Acciones
Cuando una empresa sale a bolsa (IPO) o necesita financiamiento, emite acciones para:

Recaudar capital sin endeudarse.
Atraer inversionistas y mejorar su liquidez.
Ampliar su base de accionistas para generar confianza en el mercado.
2. Reducción del Número de Acciones en Circulación
Más adelante, la empresa puede reducir las acciones disponibles en el mercado mediante estrategias como:

🔹 Recompra de Acciones (Buyback)
La empresa compra sus propias acciones, lo que puede:

Aumentar el precio de las acciones (menos oferta, más demanda).
Mejorar indicadores financieros como el beneficio por acción (BPA).
Evitar una posible dilución en caso de futuras emisiones.
🔹 Reverse Split (Consolidación de Acciones)
En ocasiones, las empresas agrupan varias acciones en una sola (ej. 10 acciones → 1 acción) para:

Evitar que el precio caiga demasiado (acciones de centavos pueden ser vistas como poco confiables).
Mantenerse en índices bursátiles que exigen precios mínimos (como el S&P 500 o Nasdaq).
En resumen, las empresas comienzan con muchas acciones para atraer inversionistas y capital, pero después pueden reducirlas para mejorar su rendimiento financiero, mantener su valor y hacer más atractiva su participación en el mercado.






![Medidas 1](https://github.com/user-attachments/assets/b2fc082c-142b-45f2-8dc5-4948c7dcaffc)





A continuación se puede dilucidar como el rendimiento de las acciones se condice con bajadas y subidas de precio. Aunque con matices, ya que en el rendimiento de una accion estan asociados diversos factores, entre ellos el pago de dividendos, el cual aunque disminuya el precio de una accion, el rendimiento pueda aumentar. Tambien dependen de las distintas operaciones que maneje cada poseedor de acciones, desde las basicas: compra y venta, hasta las avanzadas: ventas en corto, opciones, contratos, recompra de acciones, etc.




![Medidas2](https://github.com/user-attachments/assets/2034016f-b517-4f3a-92d6-c61b5d5f976b)




![Medidas3](https://github.com/user-attachments/assets/ffecbc52-4e56-4ba5-9b9a-f029caec893b)



Conclusiones generales:

Los rendimientos de las acciones estan asociadas a diferentes operaciones que se realicen en el mercado, por lo cual aunque exista una relación entre estos rendimientos estos no necesariamente son directamente proporcional, ya que dependen netamente de la operación que se este efectuando sobre el instrumento financiero.

El volumen de cantidad de acciones en el mercado depende de diversos factores, como los ya mencionados. Las empresas cambian la cantidad de acciones en circulación por varias razones estratégicas y financieras. Estas modificaciones pueden ocurrir a través de recompras de acciones, emisiones de nuevas acciones, splits o reverse splits. Las razones principales se podrian explicar por: Recaudar capital, aumentar liquidez, hacer la accion mas accesible, pagar dividendos, mejorar el precio, cumplir con las regulaciones del mercado, etc.

En resumen:
Las empresas aumentan acciones para recaudar fondos, hacer la acción más accesible y aumentar liquidez.
Las empresas reducen acciones para mejorar el precio, evitar dilución y cumplir con regulaciones del mercado.
























