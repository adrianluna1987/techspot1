introducción
Este informe detalla el proceso de desarrollo del sitio web para "TechSpot", una tienda de electrónicos en línea. El objetivo fue crear un sitio funcional y atractivo que permita a los usuarios registrarse, iniciar sesión, buscar productos, agregar productos al carrito, y realizar compras. Además, se prestó especial atención a la usabilidad, la experiencia del usuario y la implementación de técnicas de validación de formularios HTML5 para mejorar la precisión y seguridad de los datos.

1. Estructura y Diseño del Sitio Web
1.1. Estructura Inicial
La estructura del sitio web se organizó en una jerarquía de archivos y carpetas para facilitar el mantenimiento:

Copiar código
TechSpot/
├── index.html
├── productos.html
├── detalle_producto.html
├── carrito.html
├── registro.html
├── login.html
├── busqueda.html
├── compra.html
└── css/
    └── styles.css
1.2. Diseño de Páginas Clave
Las principales páginas desarrolladas fueron:

Página de Inicio (index.html): Sirve como portal principal, proporcionando enlaces a otras secciones del sitio, como el catálogo de productos, registro e inicio de sesión.
Catálogo de Productos (productos.html): Muestra una lista de productos con la opción de agregar cada producto al carrito.
Detalle del Producto (detalle_producto.html): Presenta información detallada sobre un producto específico y permite a los usuarios agregarlo al carrito.
Carrito de Compras (carrito.html): Muestra los productos seleccionados por el usuario, con opciones para eliminar productos y proceder al pago.
Páginas de Formularios (registro.html, login.html, busqueda.html, compra.html): Permiten a los usuarios registrarse, iniciar sesión, buscar productos y finalizar compras.
2. Desarrollo de Formularios HTML5
Se desarrollaron varios formularios críticos para la interacción del usuario:

Registro de Usuario: Permite a los usuarios crear una cuenta en el sitio. Se implementó validación HTML5 para asegurar que los datos ingresados (nombre, correo electrónico, y contraseña) sean correctos. Se utilizó JavaScript para verificar que las contraseñas coincidan.

Inicio de Sesión: Facilita la autenticación de los usuarios registrados. La validación asegura que el correo electrónico y la contraseña ingresados sean válidos.

Búsqueda de Productos: Permite a los usuarios buscar productos en el sitio. La validación HTML5 asegura que el término de búsqueda no esté vacío.

Compra: Recopila la información necesaria para completar una transacción, incluyendo nombre, dirección y detalles de la tarjeta de crédito. Se implementaron patrones para validar los formatos de tarjeta de crédito, fecha de expiración y CVV.

3. Implementación de Funcionalidades Clave
3.1. Agregar Productos al Carrito
Se implementó la funcionalidad para agregar productos al carrito desde las páginas de catálogo y detalles del producto. La información del producto (ID, nombre, precio) se almacena en localStorage para simular la persistencia del carrito entre sesiones.

3.2. Manejo del Carrito de Compras
La página del carrito muestra los productos agregados, permitiendo al usuario eliminar productos antes de proceder al pago. Se utilizó localStorage para mantener el estado del carrito y se implementó JavaScript para manipular el DOM, reflejando los cambios en tiempo real.

4. Decisiones de Diseño
4.1. Paleta de Colores y Estilos
Se optó por un esquema de colores oscuros (fondo negro y gris) con texto claro (blanco y gris claro) y acentos en azul para los botones principales. Este esquema fue elegido para crear una apariencia moderna y tecnológica, coherente con la identidad de TechSpot.

4.2. Usabilidad y Navegación
Para mejorar la usabilidad, se añadieron botones de navegación en las páginas de catálogo y carrito, permitiendo a los usuarios regresar a la página de inicio, acceder al carrito de compras, o volver a la página anterior. Esto facilita la navegación entre secciones importantes del sitio.

5. Desafíos Encontrados y Soluciones
5.1. Legibilidad del Texto en el Carrito de Compras
Desafío: Se detectó que el texto en la página del carrito de compras era difícil de leer debido a un bajo contraste entre el texto y el fondo.

Solución: Se actualizó el color del texto a un blanco puro (#ffffff) y se mantuvo un fondo gris oscuro (#333) para asegurar un contraste adecuado. Esto mejoró significativamente la legibilidad.

5.2. Validación de Formularios
Desafío: Garantizar que la validación de formularios sea robusta y amigable para el usuario, especialmente en la verificación de contraseñas y detalles de la tarjeta de crédito.

Solución: Se utilizaron tanto las capacidades de validación nativas de HTML5 como validaciones personalizadas con JavaScript. Esto permitió manejar casos especiales, como asegurar que las contraseñas coincidan y que el formato de la tarjeta de crédito sea correcto.

6. Conclusiones y Recomendaciones
El desarrollo del sitio web de TechSpot ha resultado en un portal funcional, estéticamente coherente, y centrado en la experiencia del usuario. Las decisiones de diseño y la implementación de validaciones adecuadas han mejorado la usabilidad y la seguridad del sitio.

Recomendaciones Futuras:

Implementación de un Backend: Para manejar de manera efectiva el registro de usuarios, inicio de sesión, y el almacenamiento persistente del carrito de compras en una base de datos.
Optimización de la Experiencia Móvil: Adaptar los estilos y la interfaz para asegurar una experiencia fluida en dispositivos móviles.
Integración de Métodos de Pago Reales: Incorporar pasarelas de pago como PayPal o Stripe para habilitar transacciones seguras.
