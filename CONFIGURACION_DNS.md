# Configuración DNS para salon-real-providencia.invitados.org

## Estado del Proyecto

✅ **Repositorio creado**: https://github.com/ArturoCruzArm/salon-real-providencia
✅ **GitHub Pages activado**: Configurado en rama `master`
✅ **Dominio personalizado**: salon-real-providencia.invitados.org

## Configuración DNS Requerida

Para que el dominio `salon-real-providencia.invitados.org` apunte a tu sitio de GitHub Pages, necesitas configurar los siguientes registros DNS en tu proveedor de dominios (donde gestionas `invitados.org`).

### Opción 1: CNAME (Recomendada para subdominios)

```
Tipo:  CNAME
Host:  salon-real-providencia
Valor: arturoCruzArm.github.io
TTL:   3600 (o automático)
```

### Opción 2: Registros A + CNAME (Alternativa)

Si la opción CNAME no funciona, usa estos registros A:

```
Tipo:  A
Host:  salon-real-providencia
Valor: 185.199.108.153
TTL:   3600

Tipo:  A
Host:  salon-real-providencia
Valor: 185.199.109.153
TTL:   3600

Tipo:  A
Host:  salon-real-providencia
Valor: 185.199.110.153
TTL:   3600

Tipo:  A
Host:  salon-real-providencia
Valor: 185.199.111.153
TTL:   3600
```

## Pasos para Configurar el DNS

### 1. Accede al Panel de Control de tu Dominio

Ingresa al panel de control donde gestionas el dominio `invitados.org`. Esto puede ser:
- GoDaddy
- Namecheap
- Cloudflare
- Google Domains
- Otro proveedor de DNS

### 2. Busca la Sección de DNS

Busca una sección llamada:
- "DNS Management"
- "Administración de DNS"
- "Zone File"
- "DNS Records"

### 3. Agrega el Registro CNAME

Crea un nuevo registro con estos valores:

| Campo | Valor |
|-------|-------|
| Tipo | CNAME |
| Nombre/Host | salon-real-providencia |
| Valor/Apunta a | arturoCruzArm.github.io |
| TTL | 3600 o Automático |

**Nota**: Algunos proveedores pueden pedirte que incluyas el punto al final: `arturoCruzArm.github.io.`

### 4. Guarda los Cambios

Guarda la configuración DNS.

### 5. Espera la Propagación

- La propagación DNS puede tardar entre **5 minutos y 48 horas**
- Normalmente toma entre 15-30 minutos
- Puedes verificar el estado en: https://www.whatsmydns.net/#CNAME/salon-real-providencia.invitados.org

## Verificación

### Verificar DNS

Usa estos comandos para verificar la configuración:

```bash
# Verificar registro CNAME
nslookup salon-real-providencia.invitados.org

# O con dig (en Linux/Mac)
dig salon-real-providencia.invitados.org
```

Deberías ver que apunta a `arturoCruzArm.github.io`.

### Verificar GitHub Pages

1. Ve a: https://github.com/ArturoCruzArm/salon-real-providencia/settings/pages
2. Deberías ver:
   - ✅ Your site is published at `http://salon-real-providencia.invitados.org/`
   - El dominio personalizado configurado

### Habilitar HTTPS (Recomendado)

Una vez que el DNS esté propagado:

1. Ve a: https://github.com/ArturoCruzArm/salon-real-providencia/settings/pages
2. Espera a que aparezca la opción "Enforce HTTPS"
3. Márcala para habilitar HTTPS
4. Tu sitio estará en: `https://salon-real-providencia.invitados.org/`

**Nota**: HTTPS puede tardar hasta 24 horas en activarse después de que el DNS esté configurado.

## Ejemplos por Proveedor

### Cloudflare

1. Ve a tu dominio en Cloudflare
2. Clic en "DNS"
3. Clic en "Add record"
4. Tipo: CNAME
5. Name: salon-real-providencia
6. Target: arturoCruzArm.github.io
7. Proxy status: DNS only (nube gris, NO naranja)
8. Guardar

### GoDaddy

1. Ve a "My Products"
2. Clic en "DNS" junto a tu dominio
3. Clic en "Add"
4. Tipo: CNAME
5. Host: salon-real-providencia
6. Apunta a: arturoCruzArm.github.io
7. TTL: 1 hora
8. Guardar

### Google Domains

1. Ve a "DNS" en el menú lateral
2. Scroll hasta "Custom resource records"
3. Name: salon-real-providencia
4. Type: CNAME
5. TTL: 1h
6. Data: arturoCruzArm.github.io
7. Añadir

## Solución de Problemas

### El sitio no carga después de 48 horas

1. Verifica que el registro CNAME esté correcto
2. Asegúrate de que no haya otros registros conflictivos para `salon-real-providencia`
3. Si usas Cloudflare, desactiva el proxy (nube gris)

### Error "CNAME already exists"

Si ya existe un registro para `salon-real-providencia`, elimínalo primero y luego crea el nuevo.

### Error 404

- Espera a que se complete el build de GitHub Pages
- Verifica en: https://github.com/ArturoCruzArm/salon-real-providencia/actions

### HTTPS no se activa

- Espera 24 horas después de que el DNS esté configurado
- Asegúrate de que el DNS esté correctamente propagado
- El certificado SSL se emite automáticamente por GitHub

## URLs del Proyecto

- **Repositorio**: https://github.com/ArturoCruzArm/salon-real-providencia
- **Configuración Pages**: https://github.com/ArturoCruzArm/salon-real-providencia/settings/pages
- **URL del sitio**: http://salon-real-providencia.invitados.org/
- **URL con HTTPS** (después de configurar): https://salon-real-providencia.invitados.org/

## Contacto de Soporte

Si tienes problemas:
1. Verifica la documentación de tu proveedor de DNS
2. Consulta: https://docs.github.com/es/pages/configuring-a-custom-domain-for-your-github-pages-site
3. Contacta al soporte de tu proveedor de dominios

---

**Fecha de configuración**: 2 de enero de 2026
**Configurado por**: Claude Code con GitHub CLI
