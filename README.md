# Laboratorio #2 - Implementación de Login en Laravel

## 1. Introducción
Este proyecto implementa un sistema de autenticación de usuarios en Laravel utilizando el paquete `laravel/ui`. Incluye login, registro y recuperación de contraseña, siguiendo la arquitectura MVC (Modelo-Vista-Controlador). El laboratorio representa el primer acercamiento al framework Laravel y su estructura de trabajo.

## 2. Requisitos Previos
- ✅ PHP 8.2 o superior
- ✅ Composer 
- ✅ Servidor web local (WAMP)
- ✅ Base de datos MySQL
- ✅ Node.js y NPM
- ✅ Visual Studio Code

## 3. Instalación y Configuración
Los siguientes comandos fueron ejecutados para configurar el proyecto:
bash
composer require laravel/ui
php artisan ui bootstrap --auth
npm install
npm run dev

## 4. Estructura MVC
Modelos: User.php (gestiona datos de usuarios)
Vistas: login.blade.php, register.blade.php, home.blade.php (con Bootstrap)
Controladores: AuthController, HomeController
Rutas: Definidas en web.php

## 5. Base de Datos
Configuración en archivo .env
Base de datos creada manualmente en phpMyAdmin
Migración ejecutada: php artisan migrate
Tablas creadas: users, password_resets, migrations

## 6. Resultados
El laboratorio fue exitoso. Se logró:
✅ Configurar el entorno de desarrollo con WAMP
✅ Integrar Laravel con autenticación básica
✅ Configurar la base de datos MySQL
✅ Implementar vistas con Bootstrap usando Laravel UI
✅ Ejecutar el servidor en http://localhost:8000

## 7. Dificultades y Soluciones
- Dificultad 1: Versión de PHP incompatible
Problema: Laravel detectaba una versión anterior de PHP (7.4.33) en lugar de la 8.3.14 instalada.
Solución: Modificar los permisos y configuración desde el CMD para que Laravel reconociera la versión correcta.

- Dificultad 2: Políticas de ejecución en PowerShell
Problema: Restricciones de políticas de seguridad impedían ejecutar npm.
Solución: Ejecutar Set-ExecutionPolicy RemoteSigned -Scope CurrentUser.

- Dificultad 3: Incompatibilidades con Windows
Problema: Errores al ejecutar composer run dev debido a scripts incompatibles.
Solución: Modificar el script dev en el archivo composer.json.

- Dificultad 4: Permisos de terminal
Problema: La terminal de Visual Studio Code no tenía los permisos necesarios.
Solución: Alternar entre CMD y la terminal de Visual Studio Code según los errores.

- Dificultad 5: Conflictos de puertos
Problema: Puerto 5173 en uso por Vite.
Solución: Ajustar configuración de puertos, Vite automáticamente usó el puerto 5174.

- Dificultad 6: Base de datos no existía
Problema: Error "Access denied for user 'root'@'localhost'" y base de datos no encontrada.
Solución: Crear la base de datos manualmente en phpMyAdmin y verificar credenciales en .env.

## 8. Referencias
Documentación oficial de Laravel
Stack Overflow - Soluciones a errores específicos
Inteligencia Artificial - Asistencia en resolución de problemas

## 9. Desarrollado por:
Nombre: Luis Calderón
Curso: Ingeniería Web
Instructor: Ing. Irina Fong
Universidad: Universidad Tecnológica de Panamá

## 10. Fecha de Ejecución
Laboratorio realizado: 28 de septiembre de 2025
Fecha de entrega: 29 de septiembre de 2025