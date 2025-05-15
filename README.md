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

---

## 📸 Progreso visual del proceso de integración con Khipu

<ul>
  <li>
    <strong>🖥️ Paso 1: Inicio del flujo</strong><br>
    El usuario accede a <code>/</code> y ve la interfaz principal con el botón “Pagar con Khipu”.<br>
    <img src="static/img/paso1khipu.png" alt="Paso 1" width="600">
  </li>
  <li>
    <strong>📄 Paso 2: Llamada a la API para crear el pago</strong><br>
    Desde Flask, se ejecuta un <code>POST</code> a <code>/v3/payments</code> usando la API Key, y se genera el link de pago.<br>
    <img src="static/img/paso2khipu.png" alt="Paso 2" width="600">
  </li>
  <li>
    <strong>🏦 Paso 3: Redirección al entorno de pago (DemoBank)</strong><br>
    El usuario es redirigido a la interfaz de Khipu para elegir su banco.<br>
    <img src="static/img/paso3khipu.png" alt="Paso 3" width="600">
  </li>
  <li>
    <strong>🔐 Paso 4: Inicio de sesión en el banco</strong><br>
    Se ingresan las credenciales de prueba proporcionadas por Khipu.<br>
    <img src="static/img/paso4khipu.png" alt="Paso 4" width="600">
  </li>
  <li>
    <strong>🧾 Paso 5: Autorización del pago</strong><br>
    Se utiliza un token de validación (clave dinámica) para confirmar la operación.<br>
    <img src="static/img/paso5khipu.png" alt="Paso 5" width="600">
  </li>
  <li>
    <strong>✅ Paso 6: Confirmación del pago</strong><br>
    Khipu confirma el pago exitoso y redirige a la vista <code>/success</code>.<br>
    <img src="static/img/paso6khipu.png" alt="Paso 6" width="600">
  </li>
  <li>
    <strong>📧 Paso 7: Comprobante de pago por email</strong><br>
    Se genera automáticamente el comprobante con los detalles de la transacción.<br>
    <img src="static/img/paso7khipu.png" alt="Paso 7" width="600">
  </li>
</ul>


















