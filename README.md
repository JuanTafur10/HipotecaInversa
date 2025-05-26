Autores originales:  
Juan Pablo Tafur  
Sebastian Valencia  

Integrantes:  
Juan jose cano giraldo  
Valentina mesa  

Proyecto: Simulador de Hipoteca Inversa

Descripción

Aplicación desarrollada en Python con Kivy que simula una hipoteca inversa, permitiendo calcular el ingreso mensual y la deuda total generada a partir del valor de la vivienda, el número de cuotas, la tasa de interés y otros datos financieros. La herramienta está dirigida a usuarios mayores de 65 años interesados en conocer cómo podrían obtener ingresos usando el valor de su propiedad sin venderla.

Requisitos previos  
Antes de ejecutar la aplicación, asegúrate de tener instalado:

- Python 3.8 o superior
- Kivy, que es la librería usada para construir la interfaz gráfica.

Puedes instalar Kivy usando el gestor de paquetes correspondiente.

Estructura esperada del proyecto

HipotecaInversa/
│
├── src/
│   ├── model/
│   │   └── hipoteca_inversa.py
│   ├── errores/
│   │   └── excepciones.py
│   └── view/
│       └── gui/
│           └── hipoteca_inversa_gui.py
│
└── README.md

Creación de la base de datos y configuración de la conexión

Antes de ejecutar la aplicación, debes tener una base de datos PostgreSQL disponible. Si no tienes una, sigue estos pasos:

1. Instala PostgreSQL en tu equipo o utiliza un servicio en la nube.
2. Crea una nueva base de datos para el proyecto.
3. Crea un usuario y asígnale una contraseña segura.
4. Otorga al usuario permisos sobre la base de datos creada.
5. Toma nota de los siguientes datos: host, nombre de la base de datos, usuario y contraseña.

Configuración del archivo secret_config.py

El archivo secret_config.py contiene las credenciales privadas para la conexión a la base de datos y no debe subirse al repositorio. Para configurarlo:

1. Copia el archivo secret_config_example.py y renómbralo como secret_config.py.
2. Abre secret_config.py y reemplaza los valores de ejemplo por tus datos reales de conexión (host, base de datos, usuario y contraseña).
3. Guarda el archivo.  
Recuerda que este archivo es privado y no debe compartirse.

Pasos para ejecutar la interfaz gráfica (GUI) y el programa

1. Ubícate en la raíz del proyecto  
Abre una terminal o consola y navega hasta la carpeta principal del proyecto. Por ejemplo:  
cd C:\Users\Usuario\Desktop\Hipoteca inversa\HipotecaInversa

2. Ejecuta el archivo de la GUI  
Desde la raíz del proyecto, ejecuta el siguiente comando:  
python src/view/gui/hipoteca_inversa_gui.py

Esto abrirá la ventana de la aplicación con los campos de entrada y el botón para calcular.

**Ejecutar el programa**

Una vez configurada la base de datos y el archivo secret_config.py, simplemente sigue los pasos anteriores para ejecutar el programa desde la terminal.  
La aplicación se conectará automáticamente a la base de datos usando los datos proporcionados en secret_config.py.

¿Qué debe pasar al ejecutarlo?

Se abrirá una ventana con los siguientes campos para ingresar datos:

- Edad del usuario
- Precio de la vivienda
- Porcentaje del valor a financiar
- Número de cuotas
- Tasa de interés mensual

Al presionar el botón "Calcular", se mostrarán:

- El ingreso mensual estimado
- La deuda total generada

Si algún dato está mal ingresado o falta, se mostrará un mensaje de error indicando qué corregir.


