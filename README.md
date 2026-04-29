# 🎮 Mcicons API

> [!IMPORTANT]
> **Obtén iconos de Minecraft directamente** 🚀
> 
> La API devuelve una redirección 302 directa a la imagen, perfecta para usar en etiquetas `<img>`.
> - **Base URL:** https://api.lulali20.com/Mcicons/
> - **Sin autenticación requerida**
> - **Respuestas rápidas y directas**
> 
> ¡Gracias por usar Mcicons-api! 💙

## ✨ Características

- ⚡ Acceso instantáneo a iconos de Minecraft
- 🖼️ Redirección directa (302) a imágenes
- 📦 Uso directo en etiquetas `<img>`
- 🔧 Compatible con cualquier lenguaje de programación
- 🌐 Fácil de integrar en tus proyectos

## 🚀 Guía de Uso Rápida

### Uso directo en HTML

```html
<img src="https://api.lulali20.com/Mcicons/items/diamond" alt="Diamond">
```

### Uso en JavaScript

```javascript
// Crear una imagen dinámicamente
const img = document.createElement('img');
img.src = 'https://api.lulali20.com/Mcicons/items/diamond';
img.alt = 'Diamond';
document.body.appendChild(img);
```

> [!TIP]
> Puedes usar async/await para verificar que la imagen cargó correctamente:
> ```javascript
> const img = new Image();
> img.onload = () => console.log('Imagen cargada');
> img.onerror = () => console.error('Imagen no encontrada');
> img.src = 'https://api.lulali20.com/Mcicons/items/diamond';
> ```

### Uso en Python

```python
import requests

url = 'https://api.lulali20.com/Mcicons/items/diamond'
r = requests.get(url, allow_redirects=True)

# Obtener la URL final de la imagen
print(r.url)  # → URL final de la imagen

# Guardar la imagen
with open('diamond.png', 'wb') as f:
    f.write(r.content)
```

## 📡 API Reference

### Endpoint Principal

Obtén el ícono de cualquier ítem o bloque de Minecraft.

**GET** `https://api.lulali20.com/Mcicons/{categoria}/{icon_id}`  
**GET** `https://api.lulali20.com/Mcicons/{icon_id}`

### Parámetros

| Parámetro | Tipo | Descripción | Estado |
|-----------|------|-------------|--------|
| `categoria` | string | Categoría del ícono (ej: `blocks`, `items`) | Opcional |
| `icon_id` | string | Identificador del ícono (ej: `diamond`) | **Requerido** |

### Ejemplos de URLs

```
https://api.lulali20.com/Mcicons/items/diamond
https://api.lulali20.com/Mcicons/blocks/stone
https://api.lulali20.com/Mcicons/diamond
```

### Respuesta

La API devuelve un redirect **302** directo a la URL de la imagen.

```
Status: 302 Found
Location: [URL de la imagen]
```

> [!WARNING]
> Asegúrate de usar `allow_redirects=True` en librerías como `requests` (Python) para seguir automáticamente la redirección.

## ⚠️ Códigos de Error

| Código | Significado |
|--------|------------|
| **302** | ✅ Éxito. Redirección a la URL de la imagen |
| **404** | ❌ Ícono no encontrado en la base de datos |
| **500** | ❌ Error interno del servidor |

## 🧊 Demo en Vivo

Prueba la API directamente:

```html
<select id="category">
  <option value="items">Items</option>
  <option value="blocks">Blocks</option>
</select>
<input type="text" id="iconId" placeholder="ej: diamond" value="diamond">
<button onclick="loadIcon()">Cargar Ícono</button>
<img id="result" alt="Preview">

<script>
function loadIcon() {
  const category = document.getElementById('category').value;
  const iconId = document.getElementById('iconId').value;
  const url = `https://api.lulali20.com/Mcicons/${category}/${iconId}`;
  document.getElementById('result').src = url;
}
</script>
```

## 💡 Casos de Uso

- 🎮 Wikis de Minecraft
- 🛍️ Tiendas online de gaming
- 📱 Aplicaciones móviles de Minecraft
- 🎨 Generadores de contenido
- 📊 Dashboards y paneles de administración

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Para contribuir:

1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

> [!NOTE]
> Por favor, asegúrate de que tus cambios pasen los tests antes de enviar un PR.

## 🆘 Soporte

Si encuentras algún problema o tienes preguntas:
- 📧 Abre un [issue](https://github.com/LuLaLi20/Mcicons-api/issues)
- 💬 Visita la [documentación oficial](https://api.lulali20.com/documentacion/Mcicons)

---

¡Esperamos que disfrutes usando Mcicons-api! 🎉

## By LuLaLi20
