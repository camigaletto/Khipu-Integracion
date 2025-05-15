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


## 📸 Capturas del proceso de integración con Khipu

### 🖥️ Paso 1: Inicio del flujo
> El usuario accede a `/` y ve la interfaz principal con el botón “Pagar 
con Khipu”.
<img width="761" alt="paso1khipu" src="https://github.com/user-attachments/assets/2acc3637-6973-41c6-8d0a-42fc75bf350b" />


---

### 🧾 Paso 2: Llamada a la API para crear el pago
> Desde Flask, se ejecuta un `POST` a `/v3/payments` usando la API Key y 
se genera un link de pago.
![Paso 
2](https://github.com/camigaletto/Khipu-Integracion/raw/main/static/img/paso2khipu.png)

---

### 🏦 Paso 3: Redirección al entorno de pago (DemoBank)
> El usuario es redirigido automáticamente a la interfaz de Khipu para 
elegir su banco.
![Paso 
3](https://github.com/camigaletto/Khipu-Integracion/raw/main/static/img/paso3khipu.png)

---

### 🔐 Paso 4: Inicio de sesión en el banco
> Se ingresan credenciales simuladas proporcionadas por Khipu para el 
entorno de pruebas.
![Paso 
4](https://github.com/camigaletto/Khipu-Integracion/raw/main/static/img/paso4khipu.png)

---

### 📲 Paso 5: Autorización del pago
> Se utiliza un token de validación (clave dinámica) para confirmar la 
operación.
![Paso 
5](https://github.com/camigaletto/Khipu-Integracion/raw/main/static/img/paso5khipu.png)

---

### ✅ Paso 6: Confirmación del pago exitoso
> El sistema muestra una pantalla de éxito y redirige automáticamente a 
`/success`.
![Paso 
6](https://github.com/camigaletto/Khipu-Integracion/raw/main/static/img/paso6khipu.png)

---

### 🧾 Paso 7: Comprobante por correo
> Khipu envía automáticamente un correo con el comprobante de pago.
![Paso 
7](https://github.com/camigaletto/Khipu-Integracion/raw/main/static/img/paso7khipu.png)

















