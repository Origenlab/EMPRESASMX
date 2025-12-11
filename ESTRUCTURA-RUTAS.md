# Estructura de Rutas - EmpresasMX

## 📁 Estructura de Directorios

```
EMPRESASMX/
├── index.html                    # Página principal
├── eventos.html                  # Listado de empresas de eventos
├── eventos/                      # Carpeta para empresas de eventos
│   └── empresa-redeil.html      # Perfil de REDEIL
├── css/
│   └── style.css
└── ...
```

## 🔗 Sistema de Rutas

### Desde index.html (raíz)
- ✅ Eventos → `eventos.html`
- ✅ Categorías → Links internos con `#categorias`
- ✅ Blog → Links internos con `#blog`

### Desde eventos.html (raíz)
- ✅ Inicio → `index.html`
- ✅ Empresas → `eventos/empresa-[nombre].html`
- ✅ Estilos → `css/style.css`

### Desde eventos/empresa-redeil.html (subcarpeta)
- ✅ Logo/Inicio → `../index.html`
- ✅ Eventos (nav) → `../eventos.html`
- ✅ Blog → `../index.html#blog`
- ✅ Estilos → `../css/style.css`
- ✅ Breadcrumb Inicio → `../index.html`
- ✅ Breadcrumb Eventos → `../eventos.html`
- ✅ Footer Eventos → `../eventos.html`
- ✅ Footer Categorías → `../index.html#categorias`
- ✅ Sidebar Eventos → `../eventos.html`

## 📝 Patrón de Rutas Relativas

### Archivos en raíz (index.html, eventos.html)
```html
<a href="eventos.html">Eventos</a>
<a href="eventos/empresa-redeil.html">Ver Perfil</a>
<link rel="stylesheet" href="css/style.css">
```

### Archivos en subcarpeta eventos/ (empresa-*.html)
```html
<a href="../index.html">Inicio</a>
<a href="../eventos.html">Eventos</a>
<link rel="stylesheet" href="../css/style.css">
```

## 🎯 Próximas Empresas

Cuando agregues más empresas de eventos, sigue este patrón:

1. **Crear archivo:** `eventos/empresa-[nombre].html`
2. **En eventos.html:** Link con `eventos/empresa-[nombre].html`
3. **Dentro del perfil:** Usar rutas relativas con `../`

### Ejemplo para nueva empresa "EventosPro":

**En eventos.html:**
```html
<a href="eventos/empresa-eventospro.html" class="btn btn-primary">Ver Perfil</a>
```

**En eventos/empresa-eventospro.html:**
```html
<link rel="stylesheet" href="../css/style.css">
<a href="../index.html">Inicio</a>
<a href="../eventos.html">Eventos</a>
```

## ✅ Verificación Completada

Todos los enlaces han sido actualizados correctamente:
- ✅ index.html → eventos.html
- ✅ eventos.html → eventos/empresa-redeil.html
- ✅ eventos/empresa-redeil.html → rutas relativas con ../

---

**Última actualización:** Noviembre 2025
**Estado:** ✅ Rutas configuradas y funcionando
