# Instrucciones para Publicar en GitHub Pages

## Paso 1: Crear el Repositorio en GitHub

1. Ve a [GitHub.com](https://github.com) e inicia sesión
2. Haz clic en el botón "+" en la esquina superior derecha y selecciona "New repository"
3. Configura tu repositorio:
   - **Repository name**: `salon-real-providencia` (o el nombre que prefieras)
   - **Description**: "Sitio web oficial de Salones Real Providencia"
   - **Public/Private**: Selecciona "Public" (necesario para GitHub Pages gratuito)
   - **NO** marques "Add a README file" (ya lo tenemos)
   - **NO** agregues .gitignore ni licencia (ya los tenemos)
4. Haz clic en "Create repository"

## Paso 2: Conectar tu Repositorio Local con GitHub

Después de crear el repositorio, GitHub te mostrará instrucciones. Usa estas en tu terminal:

```bash
cd C:\Users\foro7\salon-real-providencia
git remote add origin https://github.com/TU-USUARIO/salon-real-providencia.git
git branch -M main
git push -u origin main
```

**Nota**: Reemplaza `TU-USUARIO` con tu nombre de usuario de GitHub.

## Paso 3: Activar GitHub Pages

1. En tu repositorio de GitHub, ve a **Settings** (Configuración)
2. En el menú lateral izquierdo, busca y haz clic en **Pages**
3. En la sección "Build and deployment":
   - **Source**: Selecciona "Deploy from a branch"
   - **Branch**: Selecciona "main" (o "master")
   - **Folder**: Selecciona "/ (root)"
4. Haz clic en **Save** (Guardar)

## Paso 4: Esperar a que se Publique

- GitHub Pages tardará unos minutos en construir y publicar tu sitio
- Verás un mensaje indicando que tu sitio está listo
- Tu sitio estará disponible en: `https://TU-USUARIO.github.io/salon-real-providencia/`

## Paso 5: Configurar el Formulario de Contacto (Opcional)

El formulario de contacto actualmente tiene un ID de placeholder. Para activarlo:

1. Ve a [Formspree.io](https://formspree.io) y crea una cuenta gratuita
2. Crea un nuevo formulario
3. Copia tu Form ID
4. Edita el archivo `index.html` en GitHub:
   - Encuentra la línea que dice: `action="https://formspree.io/f/YOUR_FORM_ID"`
   - Reemplaza `YOUR_FORM_ID` con tu ID real de Formspree
   - Haz commit de los cambios

## Paso 6: Dominio Personalizado (Opcional)

Si quieres usar un dominio personalizado como `www.realprovidencia.com`:

1. En la sección **Pages** de Settings, encontrarás "Custom domain"
2. Ingresa tu dominio personalizado
3. Configura los registros DNS de tu dominio según las instrucciones de GitHub

### Configuración DNS requerida:
```
Tipo: A
Host: @
Valor: 185.199.108.153
       185.199.109.153
       185.199.110.153
       185.199.111.153

Tipo: CNAME
Host: www
Valor: TU-USUARIO.github.io
```

## Actualizar el Sitio Web

Cuando quieras hacer cambios:

```bash
cd C:\Users\foro7\salon-real-providencia
# Hacer tus cambios a los archivos
git add .
git commit -m "Descripción de los cambios"
git push
```

Los cambios aparecerán en tu sitio en unos minutos.

## Solución de Problemas

### El sitio no se muestra correctamente
- Verifica que los archivos estén en la raíz del repositorio
- Asegúrate de que el archivo se llama `index.html` (minúsculas)
- Espera unos minutos más, la primera publicación puede tardar

### Error 404
- Verifica que GitHub Pages esté activado en Settings > Pages
- Verifica que la rama correcta esté seleccionada
- La URL correcta es: `https://TU-USUARIO.github.io/NOMBRE-REPO/`

### Los estilos no se cargan
- Verifica que `styles.css` esté en la misma carpeta que `index.html`
- Revisa que no haya errores de tipeo en los nombres de archivos

## Recursos Adicionales

- [Documentación de GitHub Pages](https://docs.github.com/es/pages)
- [Guía de dominios personalizados](https://docs.github.com/es/pages/configuring-a-custom-domain-for-your-github-pages-site)

---

Si necesitas ayuda, puedes consultar la documentación de GitHub o contactar a soporte técnico.
