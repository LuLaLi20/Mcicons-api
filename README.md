# 🎮 Mcicons API

> [!IMPORTANT]
> **Usa la API de Mcicons** 🚀
> 
> ¡Es mucho más cómodo y práctico!
> - **API:** https://api.lulali20.com/Mcicons/
> - **Documentación:** https://api.lulali20.com/documentacion/Mcicons
> - Usar la API me ayuda a mantener y mejorar este proyecto
> 
> ¡Gracias por tu apoyo! 💙

## ✨ Características

- ⚡ Acceso rápido y sencillo a iconos de Minecraft
- 📦 Respuestas en formato JSON
- 🔧 Fácil de integrar en tus proyectos
- 🌐 Compatible con cualquier lenguaje de programación

## 🚀 Guía de Uso

### Instalación

```bash
npm install mcicons-api
```

### Ejemplo básico

```javascript
const mcicons = require('mcicons-api');

// Obtener un ícono
mcicons.getIcon('diamond')
  .then(icon => console.log(icon))
  .catch(err => console.error(err));
```

> [!TIP]
> Puedes usar async/await para un código más limpio:
> ```javascript
> const icon = await mcicons.getIcon('diamond');
> ```

### Endpoints principales

| Endpoint | Descripción |
|----------|-------------|
| `/items` | Obtiene lista de ítems |
| `/blocks` | Obtiene lista de bloques |
| `/icon/:id` | Obtiene un ícono específico |

> [!WARNING]
> Asegúrate de incluir un `User-Agent` en tus requests para evitar limitaciones de rate limit.

## 📚 Documentación Completa

Para más información detallada sobre parámetros, autenticación y ejemplos avanzados, visita la [documentación oficial](https://api.lulali20.com/documentacion/Mcicons)

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Para contribuir:

1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

> [!NOTE]
> Por favor, asegúrate de que tus cambios pasen los tests antes de enviar un PR.

## 📝 Licencia

Este proyecto está bajo la licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 🆘 Soporte

Si encuentras algún problema o tienes preguntas:
- 📧 Abre un [issue](https://github.com/LuLaLi20/Mcicons-api/issues)
- 💬 Consulta la [documentación](https://api.lulali20.com/documentacion/Mcicons)

---

¡Esperamos que disfrutes usando Mcicons-api! 🎉
