# Proyecto QA - CRUD Automatizado con Postman 💻🧪

Este es un proyecto práctico donde se automatiza un flujo completo de operaciones CRUD sobre una API REST usando **Postman**. Incluye pruebas automáticas, uso de variables, ejecución encadenada con el Runner y documentación.

## ✨ ¿Qué incluye?

- [x] Crear usuario (`POST`)
- [x] Consultar usuario por ID (`GET`)
- [x] Actualizar usuario (`PUT`)
- [x] Eliminar usuario (`DELETE`)
- [x] Uso de variables de entorno
- [x] Pruebas automáticas con scripts
- [x] Ejecución completa con el Runner de Postman

## 🔧 Herramientas

- Postman v10+
- API pública: [reqres.in](https://reqres.in)
- JavaScript (scripts de test)
- GitHub

## 📂 Archivo incluido

- `crud-postman-collection.json`: colección completa lista para importar en Postman

## ▶️ ¿Cómo usarlo?

1. Clona o descarga este repositorio
2. Abre Postman
3. Importa la colección `.json`
4. Configura tu entorno con la variable `user_id`
5. Ejecuta las peticiones en orden o usa el Runner
6. ¡Listo!

## 📌 Nota sobre la API

`reqres.in` no persiste los usuarios creados con POST, por lo tanto, en las pruebas GET posteriores puede que el usuario no exista realmente. Los scripts están adaptados para manejar esa situación.

## 👤 Autor

**Cristian Camilo Delgado**  
Desarrollador en formación | QA & Automatización  
📧 [ccdelgado@outlook.es]  
📌 Colombia

