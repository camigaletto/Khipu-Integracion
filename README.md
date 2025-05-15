# 💸 Integración de pagos con la API de Khipu

Este proyecto fue desarrollado como parte del proceso de selección para el 
equipo de Khipu.

El objetivo principal fue simular un flujo real de cobro utilizando 
exclusivamente la **API REST v3 de Khipu** en entorno de pruebas 
(**Demobank**), sin intervención manual desde el portal.

Toda la integración fue realizada mediante código utilizando **Python y 
Flask**, generando el cobro a través de una llamada `POST` a 
`/v3/payments` con los datos requeridos. El flujo incluye redirección al 
entorno de pago, confirmación del resultado, y mensajes finales.

✅ Se utilizaron recursos de documentación oficial y herramientas de apoyo 
(como IA), pero toda la implementación fue desarrollada y probada de forma 
autónoma.

---

## 🛠 Tecnologías utilizadas

- Python 3.13  
- Flask  
- requests  
- HTML5 / Markdown  
- Git / GitHub

---

## 📸 Proceso paso a paso de la integración con Khipu

<ul>
  <li>
    <strong>🟣 Paso 1: Inicio del flujo</strong><br>
    El usuario accede a la aplicación y ve el botón “Pagar con Khipu”.<br>
    <img src="static/img/paso1khipu.png" alt="Inicio del flujo" width="600">
  </li>
  <li>
    <strong>🟣 Paso 2: Detalle del pago</strong><br>
    Pantalla de Khipu donde se muestra el monto total a pagar y opciones para iniciar el pago.<br>
    <img src="static/img/paso2khipu.png" alt="Detalle del pago" width="600">
  </li>
  <li>
    <strong>🟣 Paso 3: Selección del banco</strong><br>
    El usuario elige su banco desde la interfaz simplificada de Khipu.<br>
    <img src="static/img/paso3khipu.png" alt="Selección del banco" width="600">
  </li>
  <li>
    <strong>🟣 Paso 4: Ingreso de credenciales</strong><br>
    El usuario ingresa con RUT y clave para simular el acceso bancario en entorno de pruebas.<br>
    <img src="static/img/paso4khipu.png" alt="Ingreso de credenciales" width="600">
  </li>
  <li>
    <strong>🟣 Paso 5: Autorización del pago</strong><br>
    Se simula una clave dinámica (token) para validar la operación.<br>
    <img src="static/img/paso5khipu.png" alt="Autorización del pago" width="600">
  </li>
  <li>
    <strong>🟣 Paso 6: Confirmación visual</strong><br>
    Khipu confirma que la transferencia fue realizada exitosamente.<br>
    <img src="static/img/paso6khipu.png" alt="Confirmación visual" width="600">
  </li>
  <li>
    <strong>🟣 Paso 7: Comprobante de pago</strong><br>
    Se genera el comprobante de pago con todos los datos del cobro y se envía por correo electrónico.<br>
    <img src="static/img/paso7khipu.png" alt="Comprobante de pago" width="600">
  </li>
</ul>

---

## ▶️ Cómo ejecutar el proyecto

```bash
# 1. Cloná el repositorio:
git clone https://github.com/camigaletto/Khipu-Integracion.git
cd Khipu-Integracion

# 2. Activá el entorno virtual:
source env/bin/activate

# 3. Instalá las dependencias:
pip install flask requests

# 4. Ejecutá la aplicación:
python app.py

# 5. Accedé desde tu navegador:
http://localhost:5000
