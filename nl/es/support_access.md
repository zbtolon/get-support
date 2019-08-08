---

copyright:

  years: 2018,2019

lastupdated: "2019-07-25"

keywords: access to cases, get access for cases, assign cases, watchlist

subcollection: get-support

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Asignación de acceso de usuario para trabajar con casos de soporte
{: #access}

De forma predeterminada, los usuarios de una cuenta no tienen acceso para crear, actualizar, buscar o ver casos. Como propietario de la cuenta, debe proporcionar acceso a los usuarios mediante la asignación de una política de acceso de Identity and Access Management (IAM). Utilice el servicio de gestión de cuentas del Centro de soporte para asignar a los usuarios acceso para trabajar con casos de soporte. 
{:shortdesc}

Cuando crea un caso, puede dar a otros usuarios acceso total a dicho caso añadiendo su correo electrónico en el campo **Añadir otra persona a este caso**. Los usuarios que añada tendrán acceso para ver, editar y actualizar solo ese caso en la cuenta. Además, recibirán notificaciones cuando se actualice el caso.
{: tip}

Cuando se otorga acceso a un usuario asignando un rol en el servicio de centro de soporte permite a los usuarios ver, editar o crear casos de uso, pero es posible que no puedan ver todos los casos de una cuenta. Si el propietario de la cuenta establece el valor de visibilidad de la lista de usuarios en restringido, los usuarios solo verán los casos que hayan creado ellos mismos. Para asegurarse de que un usuario siempre pueda ver o editar todos los casos de la cuenta, debe asignar una segunda política de acceso con el rol de visor en el servicio de gestión de usuarios. 

Para los usuarios de la infraestructura clásica, los permisos para asignar acceso a casos de soporte están ahora disponibles en [grupos de acceso de permisos migrados de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#predefined). Los grupos de acceso de permisos migrados incluyen la política de IAM sobre el servicio de gestión de usuarios con el rol de visor asignado.
{: note}

## Creación de un grupo de acceso para trabajar con casos
{: #creating-access-group}

Para agilizar el proceso de asignación de accesos, puede aprovechar la función de asignar una política a los usuarios mediante los grupos de acceso. Complete los pasos siguientes para crear un grupo de acceso con acceso al servicio del centro de soporte:

1. En la barra de menús, vaya a **Gestionar** &gt; **Acceso (IAM)**, seleccione **Grupos de acceso** y pulse **Crear**. 
2. Indique un nombre de grupo de acceso y una descripción y pulse **Crear**. 
3. Pulse **Políticas de acceso** > **Asignar acceso**.
4. Seleccione **Asignar acceso a servicios de gestión de cuentas**.
5. Seleccione **Centro de soporte**.
6. Seleccione el rol Visor, Editor o Administrador, en función del tipo de acceso que desea que tenga este grupo, y pulse **Asignar**. En la tabla siguiente, se indican las acciones incluidas en cada rol para trabajar con los casos.

| Rol | Acción | 
|--------|---------------|
|Visor  | Ver y buscar casos |
|Editor | Ver, buscar, crear y actualizar casos|
|Administrador | Ver, buscar, crear y actualizar casos; gestionar roles del centro de soporte para otros usuarios|
{: caption="Tabla 1. Roles y acciones para el servicio del Centro de soporte" caption-side="top"}

De forma predeterminada, los usuarios con un rol de servicio del centro de soporte pueden acceder únicamente a casos de soporte que tengan asignados, a menos que se cumpla una de las condiciones siguientes:

* El propietario de la cuenta ha establecido la visibilidad de la lista de usuarios en Vista no restringida.
* El usuario tiene asignado un rol del servicio de gestión de cuentas de gestión de usuarios.


Si desea asegurarse de que los usuarios pueden ver todos los casos de soporte en la cuenta, también puede añadir una política con el rol de visor para el servicio de gestión de usuarios al grupo de acceso:

1. Pulse **Políticas de acceso** > **Asignar acceso**.
2. Seleccione **Asignar acceso a servicios de gestión de cuentas**.
3. Seleccione **Gestión de usuarios**.
4. Seleccione **Visor** y pulse **Asignar**.


## Adición de usuarios a su cuenta grupo de acceso de gestión de casos
{: #add-user-access-group} 

Tras crear el grupo de acceso, realice los pasos siguientes para añadir usuarios:

1. En el separador **Usuarios** del grupo de acceso, pulse **Añadir usuarios**.
2. Seleccione el usuario que desee añadir y pulse **Añadir a grupo**.

## Cómo otorgar acceso a los casos a usuarios individuales 

Utilizar los grupos de acceso para asignar los servicios de gestión de usuarios y centro de soporte es a forma más eficaz de asignar acceso, pero también puede asignar los mismos permisos a usuarios individuales. 

1. Pulse **Gestionar** &gt; **Acceso (IAM)** y seleccione **Usuarios**. 
2. Pulse **Políticas de acceso** > **Asignar acceso**.
3. Seleccione **Asignar acceso a servicios de gestión de cuentas**.
4. Seleccione **Centro de soporte**.
5. Seleccione el rol **Visor**, **Editor** o **Administrador**, en función del tipo de acceso que desea que tenga este grupo, y pulse **Asignar**.
6. Si desea que el usuario pueda ver a los demás usuarios de la cuenta, asígnele el rol de visor de gestión de usuarios. 
