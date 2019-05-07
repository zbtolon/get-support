---

copyright:

  years: 2018,2019

lastupdated: "2019-04-18"

keywords: access to cases, get access for cases, assign cases

subcollection: get-support

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:important: .important}
{:new_window: target="_blank"}

# Asignación de acceso de usuario para trabajar con casos de soporte
{: #access}

De forma predeterminada, los usuarios de una cuenta no tienen acceso para crear, actualizar, buscar o ver casos. Como propietario de la cuenta, debe proporcionar acceso a los usuarios mediante la asignación de una política de acceso de Identity and Access Management (IAM). Utilice el servicio de gestión de cuentas del Centro de soporte para asignar a los usuarios acceso para trabajar con casos de soporte. 
{:shortdesc}

Cuando crea un caso, puede dar a otros usuarios acceso total a dicho caso añadiendo su correo electrónico en el campo **Añadir otra persona a este caso**. Los usuarios que añada tendrán acceso para ver, editar y actualizar solo ese caso en la cuenta. Además, recibirán notificaciones cuando se actualice el caso.
{: tip}

Para los usuarios de la infraestructura clásica, los permisos para asignar acceso a casos de soporte están ahora disponibles en [grupos de acceso de permisos migrados de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#predefined). Los grupos de acceso de permisos migrados incluyen la política de IAM sobre el servicio de gestión de usuarios con el rol de visor asignado.

## Creación de un grupo de acceso para trabajar con casos
{: #creating-access-group}

Para agilizar el proceso de asignación de accesos, puede aprovechar la función de asignar una política a los usuarios mediante los grupos de acceso. Complete los pasos siguientes para crear un grupo de acceso con acceso al servicio del centro de soporte:

1. En la barra de menús, vaya a **Gestionar** &gt; **Acceso (IAM)**, seleccione **Grupos de acceso** y pulse **Crear**. 
2. Indique un nombre de grupo de acceso y una descripción y pulse **Crear**. 
3. Pulse **Políticas de acceso** > **Asignar acceso**.
4. Seleccione **Asignar acceso a servicios de gestión de cuentas**.
5. Seleccione **Centro de soporte**.
6. Seleccione el rol **Visor**, **Editor** o **Administrador**, en función del tipo de acceso que desea que tenga este grupo, y pulse **Asignar**.

Si desea que los usuarios puedan ver a los demás usuarios de la cuenta, añada el rol de visor de gestión de usuarios al grupo de acceso:

1. Pulse **Políticas de acceso** > **Asignar acceso**.
2. Seleccione **Asignar acceso a servicios de gestión de cuentas**.
3. Seleccione **Gestión de usuarios**.
4. Seleccione **Visor** y pulse **Asignar**.

En la tabla siguiente, se indican los permisos incluidos en cada rol para trabajar con los casos.

| Rol | Acción | 
|--------|---------------|
|Visor  | Ver y buscar casos |
|Editor | Ver, buscar, crear y actualizar casos|
|Administrador | Ver, buscar, crear y actualizar casos; gestionar roles del centro de soporte para otros usuarios|
{: caption="Tabla 1. Roles y acciones para el servicio del Centro de soporte" caption-side="top"}

## Adición de usuarios a su cuenta grupo de acceso de gestión de casos
{: #add-user-access-group} 

Ahora que ya ha creado el grupo de acceso, añada usuarios:

1. En el separador **Usuarios** del grupo de acceso, pulse **Añadir usuarios**.
2. Seleccione el usuario que desea añadir al grupo y pulse **Añadir a grupo**.

## Cómo otorgar acceso a los casos a usuarios individuales 

Utilizar los grupos de acceso para asignar los servicios de gestión de usuarios y centro de soporte es a forma más eficaz de asignar acceso, pero también puede asignar los mismos permisos a usuarios individuales. 

1. Pulse **Gestionar** &gt; **Acceso (IAM)** y seleccione **Usuarios**. 
2. Pulse **Políticas de acceso** > **Asignar acceso**.
3. Seleccione **Asignar acceso a servicios de gestión de cuentas**.
4. Seleccione **Centro de soporte**.
5. Seleccione el rol **Visor**, **Editor** o **Administrador**, en función del tipo de acceso que desea que tenga este grupo, y pulse **Asignar**.
6. Si desea que el usuario pueda ver a los demás usuarios de la cuenta, asígnele el rol de visor de gestión de usuarios. 
