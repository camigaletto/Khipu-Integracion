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

## 📸 Capturas del proceso de integración

### 🖥️ Paso 1: Pantalla de inicio
> Página principal con botón "Pagar con Khipu"  
![Paso 1](static/img/paso1khipu.png)

### 💳 Paso 2: Página de Elige como quieres pagar..
> Datos del pagador, monto y motivo del cobro  
![Paso 2](static/img/paso2khipu.png)

### ✅ Paso 3: Pagar con mi banco (DemoBank)  
![Paso 3](static/img/paso3khipu.png)

### ✅ Paso 4: Ingresa a tu banco (Demobank)
> Comppletar RUT, clave  
![Paso 4](static/img/paso4khipu.png)

### 🔧 Paso 5: Autorizacion de Pago   
![Paso 5](static/img/paso5khipu.png)

### 🗂️ Paso 6:LISTO! Transferencia exitosa  
![Paso 6](static/img/paso6khipu.png)


