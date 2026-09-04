# Política de Seguridad — DevDomain Studio

## Directrices de Seguridad del Proyecto
DevDomain Studio implementa las siguientes prácticas de seguridad:

1. **Sanitización y Mitigación XSS**:
   - Todas las entradas del usuario y las respuestas de APIs externas (GitHub REST API, DNS over HTTPS) son rigurosamente sanitizadas con escape de caracteres HTML antes de cualquier inserción en el DOM.
2. **Validación RFC de Dominios**:
   - Todos los subdominios son filtrados y validados contra los estándares RFC de nombres de host (solo minúsculas `a-z`, dígitos `0-9` y guiones `-`).
3. **Ausencia de Secretos**:
   - El código es 100% cliente estático. No requiere, almacena ni expone tokens personales de acceso (PAT), claves de API ni contraseñas.
4. **Protección de Enlaces Externos**:
   - Todos los enlaces salientes contienen `rel="noopener noreferrer"` para evitar ataques de window opener.
5. **Privacidad**:
   - Se incluyen directivas `robots noindex, nofollow` para proteger el panel privado del usuario en GitHub Pages.

## Reporte de Vulnerabilidades
Si detectas alguna vulnerabilidad o vector de riesgo en este proyecto, por favor crea un issue privado o contacta al mantenedor del repositorio en GitHub: [@FrankUsqAbant](https://github.com/FrankUsqAbant).
