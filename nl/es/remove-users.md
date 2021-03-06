---

copyright:

  years: 2018

lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# Eliminación de usuarios
{: #remove}

Cuando elimina un usuario de la cuenta, el usuario deja de poder iniciar una sesión en la consola, cambiar a su cuenta si sigue perteneciendo a otra cuenta y acceder a los recursos de la cuenta.
{:shortdesc}

Solo los propietarios de la cuenta o los usuarios con el siguiente acceso pueden eliminar usuarios de una cuenta:

* Una política de IAM para el servicio de gestión de cuenta de gestión de usuarios con el rol de administrador asignado y debe ser el gestor de organización de Cloud Foundry si el usuario pertenece a una organización de Cloud Foundry.
* Si tiene la infraestructura clásica en su cuenta, un usuario debe tener una política de IAM para el servicio de gestión de cuenta de gestión de usuarios con el rol de administrador asignado, debe ser el gestor de organización de Cloud Foundry si el usuario pertenece a una organización de Cloud Foundry y debe ser un antecesor del usuario en la jerarquía de usuarios de la infraestructura clásica con el permiso de gestión de usuarios de infraestructura clásica asignado.

Para eliminar un usuario de una cuenta, realice estos pasos:

1. En la barra de menús, pulse **Gestionar** &gt; **Acceso (IAM)** y seleccione **Usuarios**.
2. En la fila del usuario que desea eliminar, seleccione **Eliminar usuario** en el menú **Acciones** ![Icono Lista de acciones](../icons/action-menu-icon.svg).
