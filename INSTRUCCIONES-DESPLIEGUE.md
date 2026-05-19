# 🚀 Cómo Hacer Funcionar los Pagos REALES

## ¡No te preocupes! Es muy fácil, solo sigue estos pasos:

---

## Paso 1: Crear cuenta en Vercel (GRATIS)

1. Ve a **https://vercel.com**
2. Haz clic en **"Sign Up"**
3. Registrate con tu cuenta de **GitHub** (si no tienes, créala gratis en github.com)

---

## Paso 2: Subir tu proyecto a GitHub

### Si NO sabes usar GitHub, aquí te explico:

1. Ve a **https://github.com** e inicia sesión
2. Haz clic en el botón verde **"New"** (arriba a la izquierda)
3. Ponle un nombre a tu proyecto, por ejemplo: `sistema-pagos`
4. Haz clic en **"Create repository"**

### Ahora sube los archivos:

**Opción A - Subir archivos manualmente (Más fácil):**
1. En tu nuevo repositorio, haz clic en **"uploading an existing file"**
2. Arrastra TODOS los archivos de tu proyecto
3. Haz clic en **"Commit changes"**

**Opción B - Usar Git (Si sabes usar la terminal):**
```bash
git init
git add .
git commit -m "Sistema de pagos multi-procesador"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/sistema-pagos.git
git push -u origin main
```

---

## Paso 3: Conectar GitHub con Vercel

1. En **https://vercel.com** haz clic en **"Add New..."** → **"Project"**
2. Verás una lista de tus repositorios de GitHub
3. Busca `sistema-pagos` (o como lo hayas llamado)
4. Haz clic en **"Import"**

---

## Paso 4: Configurar las Variables de Entorno (CLAVES SECRETAS)

**¡MUY IMPORTANTE!** Aquí es donde pones tus credenciales de PayPal, Stripe, etc.

1. En la página de configuración de Vercel, busca la sección **"Environment Variables"**
2. Agrega estas variables (solo las que vayas a usar):

### Para PayPal:
- **Name:** `PAYPAL_CLIENT_ID`
- **Value:** Tu Client ID de PayPal Sandbox (ejemplo: `AV...`)

- **Name:** `PAYPAL_CLIENT_SECRET`  
- **Value:** Tu Client Secret de PayPal Sandbox (ejemplo: `EL...`)

### Para Stripe:
- **Name:** `STRIPE_SECRET_KEY`
- **Value:** Tu clave secreta de Stripe (ejemplo: `sk_test_...`)

### ⚠️ IMPORTANTE:
- Asegúrate de seleccionar **"Production"**, **"Preview"** y **"Development"** para cada variable
- Usa credenciales de **SANDBOX/TEST**, NO de producción

---

## Paso 5: Desplegar (Deploy)

1. Después de agregar las variables, haz clic en **"Deploy"**
2. Vercel comenzará a construir tu aplicación (toma 1-2 minutos)
3. Cuando termine, te dará una URL como: `https://tu-proyecto.vercel.app`

---

## Paso 6: ¡Probar que funciona!

1. Abre la URL que te dio Vercel
2. Ve a **"Configuración APIs"**
3. **NO LLENES NADA** - Las credenciales ya están en el backend
4. Ve a **"Pago"**
5. Ingresa los datos de una tarjeta de prueba:
   ```
   4532123456789010 12/25 123 JUAN PEREZ
   ```
6. Ingresa un monto (ejemplo: `10.00`)
7. Haz clic en **"Procesar Pago"**

### ✅ Si funciona verás:
- **PayPal:** Pago autorizado (REAL)
- **Stripe:** Pago procesado (REAL)

---

## 🎯 Resumen Ultra-Simple:

1. ✅ Crear cuenta en Vercel (con GitHub)
2. ✅ Subir tu código a GitHub  
3. ✅ Conectar GitHub con Vercel
4. ✅ Poner tus claves secretas en "Environment Variables"
5. ✅ Dar click en "Deploy"
6. ✅ ¡Listo! Ya tienes pagos REALES funcionando

---

## ❓ Si algo no funciona:

### Error: "SERVER_ERROR" o "Error al conectar"
- Verifica que pusiste las variables de entorno correctamente
- Asegúrate de que las credenciales sean de **Sandbox** (no Live)
- Ve a Vercel → tu proyecto → Settings → Environment Variables

### Error: "invalid_client" (PayPal)
- Las credenciales de PayPal son incorrectas
- Ve a developer.paypal.com y verifica que estés en modo **Sandbox**
- Copia de nuevo el Client ID y Secret

### La página no carga
- Espera 1-2 minutos después del deploy
- Vercel puede tomar tiempo en la primera carga
- Refresca la página (F5)

---

## 📞 Necesitas más ayuda?

- Documentación de Vercel: https://vercel.com/docs
- PayPal Sandbox: https://developer.paypal.com/dashboard
- Stripe Test Keys: https://dashboard.stripe.com/test/apikeys

---

## 🔒 Seguridad:

✅ **Sí es seguro:** Las claves secretas están en el servidor de Vercel, NO en el navegador
✅ **Sí puedes compartir:** La URL de Vercel es pública, pero nadie puede ver tus claves
✅ **Sí es gratis:** Vercel es gratis para proyectos personales

❌ **NO hagas:** No subas tus claves secretas a GitHub (Vercel las maneja)
❌ **NO uses:** No uses credenciales de producción (Live), solo Sandbox

---

¡Eso es todo! Ahora tienes un sistema de pagos REAL funcionando 🎉
