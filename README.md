# 🎮 Mcicons API

> [!IMPORTANT]
> **Obtén iconos de Minecraft directamente** 🚀
> 
> La API sirve la imagen directamente, perfecta para usar en etiquetas `<img>`.
> - **Base URL:** https://api.lulali20.com/Mcicons/
> - **Sin autenticación requerida**
> - **Respuestas rápidas y directas**
> 
> ¡Gracias por usar Mcicons-api! 💙

## ✨ Características

- ⚡ Acceso instantáneo a iconos de Minecraft
- 🖼️ Imágenes servidas directamente
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
> img.src = 'https://api.lulali20.com/Mcicons/items/diamond.png';
> ```

### Uso en Python

```python
import requests

url = 'https://api.lulali20.com/Mcicons/items/diamond'
r = requests.get(url)

# La imagen se devuelve directamente
print(r.status_code)  # → 200

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
https://api.lulali20.com/Mcicons/items/diamond.png
https://api.lulali20.com/Mcicons/blocks/stone.png
https://api.lulali20.com/Mcicons/diamond.png
```

### Respuesta

La API devuelve la imagen directamente con `Content-Type: image/png` o `image/webp`.

```
Status: 200 OK
Content-Type: image/png
Content-Length: [tamaño en bytes]
```

## ⚠️ Códigos de Error

| Código | Significado |
|--------|------------|
| **200** | ✅ Éxito. Imagen servida directamente |
| **404** | ❌ Ícono no encontrado |
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
