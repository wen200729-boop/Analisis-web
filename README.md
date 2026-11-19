# Analisis-web
Analizaremos una base de datos sobre el comportamiento del comercio en linea y la posibilidad de crear fidelidad en una persona.

## Integrantes: 
- Wendy Otalvaro
- Arthur Araujo
- Maria Fernanda González 


## Estructura de los datos

- **Fuente:** [Ecommerce Customer Behavior Dataset – Kaggle](https://www.kaggle.com/datasets/srisyra02/ecommerce-customer-behavior-dataset)
- **Archivo:** `ecommerce-dataset.csv`
- **Tamaño:** 50.000 registros (cada fila es un cliente) y 25 columnas.
- **Variable objetivo:** `Churned` indica si el cliente abandonó la plataforma (1) o permanece (0). El 28,9 % de los clientes abandonó.
- **Tipos de variables:**
  - 5 categóricas: `Gender`, `Country`, `City`, `Signup_Quarter`, `Churned`
  - 7 numéricas discretas: `Login_Frequency`, `Wishlist_Items`, `Total_Purchases`, `Days_Since_Last_Purchase`, `Customer_Service_Calls`, `Product_Reviews_Written`, `Payment_Method_Diversity`
  - 13 numéricas continuas: `Age`, `Membership_Years`, `Session_Duration_Avg`, `Pages_Per_Session`, `Cart_Abandonment_Rate`, `Average_Order_Value`, `Discount_Usage_Rate`, `Returns_Rate`, `Email_Open_Rate`, `Social_Media_Engagement_Score`, `Mobile_App_Usage`, `Lifetime_Value`, `Credit_Balance`
- **Calidad de los datos:** 14 variables tenían valores faltantes (entre 0,3 % y 12 %), había edades imposibles (5 y 200 años), compras negativas y porcentajes mayores a 100 %. No había registros duplicados.

## Diccionario de datos

| Variable | Tipo | Descripción |
|---|---|---|
| `Age` | Numérica continua | Edad del cliente (años) |
| `Gender` | Categórica | Género del cliente (Female, Male, Other) |
| `Country` | Categórica | País de residencia (8 países) |
| `City` | Categórica | Ciudad de residencia (40 ciudades) |
| `Membership_Years` | Numérica continua | Años como miembro de la plataforma |
| `Login_Frequency` | Numérica discreta | Número de inicios de sesión en el periodo |
| `Session_Duration_Avg` | Numérica continua | Duración promedio de cada sesión (minutos) |
| `Pages_Per_Session` | Numérica continua | Páginas visitadas en promedio por sesión |
| `Cart_Abandonment_Rate` | Numérica continua | % de carritos abandonados sin comprar |
| `Wishlist_Items` | Numérica discreta | Productos guardados en la lista de deseos |
| `Total_Purchases` | Numérica discreta | Número total de compras realizadas |
| `Average_Order_Value` | Numérica continua | Valor promedio de cada pedido |
| `Days_Since_Last_Purchase` | Numérica discreta | Días transcurridos desde la última compra |
| `Discount_Usage_Rate` | Numérica continua | % de compras realizadas con descuento |
| `Returns_Rate` | Numérica continua | % de productos devueltos |
| `Email_Open_Rate` | Numérica continua | % de correos de marketing abiertos |
| `Customer_Service_Calls` | Numérica discreta | Número de contactos con servicio al cliente |
| `Product_Reviews_Written` | Numérica discreta | Número de reseñas escritas |
| `Social_Media_Engagement_Score` | Numérica continua | Puntaje de interacción en redes sociales (0–100) |
| `Mobile_App_Usage` | Numérica continua | Uso de la aplicación móvil (horas) |
| `Payment_Method_Diversity` | Numérica discreta | Cantidad de métodos de pago distintos usados (1–5) |
| `Lifetime_Value` | Numérica continua | Valor total que el cliente ha generado (CLV) |
| `Credit_Balance` | Numérica continua | Saldo de crédito disponible en la cuenta |
| `Churned` | Categórica (binaria) | 1 = el cliente abandonó la plataforma, 0 = permanece |
| `Signup_Quarter` | Categórica | Trimestre en que se registró (Q1–Q4) |



## Conclusiones

1. **El abandono es alto y no depende del lugar:** el 28,9 % de los 50.000 clientes abandonó la plataforma, y la tasa es casi igual en los 8 países analizados (27–30 %). Las causas del abandono están en la experiencia del cliente, no en su ubicación ni en su género.


2. **El engagement es el mejor indicador de fidelización:** los clientes que inician sesión con frecuencia, tienen sesiones más largas y visitan más páginas abandonan mucho menos. La tasa de abandono baja de 45,4 % en los clientes de engagement bajo a 18,1 % en los de engagement muy alto.


3. **Los problemas de servicio alejan a los clientes:** a partir del sexto contacto con servicio al cliente, la tasa de abandono se duplica (de 18,6 % a 39,7 %), y llega a más del 50 % con 10 contactos o más. Mejorar la solución de problemas en los primeros contactos podría reducir el abandono.


4. **La empresa está perdiendo a sus clientes más valiosos:** la relación entre valor y abandono tiene forma de U. Los clientes Premium, que más compran y más gastan por pedido, abandonan en un 40 %, casi igual que los de menor valor. Se recomienda crear un programa de beneficios o fidelización para este grupo.


5. **Existen señales de alerta temprana:** los clientes que abandonan más del 70 % de sus carritos y casi no abren correos tienen una tasa de abandono del 69,8 %. Además, hay 9.731 clientes "en riesgo" (sin compras en más de 60 días o con muy pocas visitas) que aún pueden recuperarse con campañas de reactivación.
