---
index: 3
title: 2FA
---
# Autenticación de Dos Factores (2FA)

*   **Las cuentas con contraseña protegen su información con algo que *sabe.***
*   **Las cuentas con 2FA también protegen su información con algo que *tiene.***

Es fácil agregar seguridad adicional a sus cuentas con 2FA y se recomienda para todos.

## Para iniciar sesión con 2FA, configure un segundo dispositivo:

* Un teléfono que puede recibir un código por mensaje de texto SMS;
* Un teléfono con una aplicación de autenticador que ha configurado para generar códigos;
* Un token o clave universal de segundo factor (U2F), como un Yubikey.

Incluso si su contraseña es hackeada o robada, el ladrón no podrá iniciar sesión a menos que también tenga el control del segundo dispositivo, como su teléfono, y los códigos especiales que solo este puede crear.

![image](password_adv2.png)

## Las aplicaciones 2FA son más seguras que los SMS

Los mensajes de texto SMS pueden ser interceptados, y la mayoría de los dispositivos U2F cuestan dinero. La mejor solución para la mayoría de las personas es utilizar una aplicación como [Google Authenticator] (https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2).

El proyecto [Two Factor Auth] (https://twofactorauth.org/) realiza un seguimiento de los servicios y el software que le permiten agregar 2FA.