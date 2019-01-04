---

copyright:

  years: 2018

lastupdated: "2018-11-28"

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

Las políticas de acceso del Centro de soporte proporcionan a los usuarios acceso para trabajar con casos de soporte. Sin embargo, estas políticas de acceso no proporcionan acceso para que los usuarios vean a otros usuarios en la cuenta. Por lo tanto, si el propietario de una cuenta establece el [**Valor de visibilidad de lista de usuarios**](/docs/iam/userlist.html#userlistview) en **Vista restringida**, es posible que los usuarios que tengan acceso para gestionar casos no puedan acceder a los casos asignados a otros usuarios o al propietario de la cuenta. Para asegurarse de que los usuarios pueden ver todos los casos, debe proporcionar acceso adicional asignando también una política de acceso de IAM para el servicio de gestión de cuentas de gestión de usuarios con el rol de Visor asignado. 

Para otorgar a determinados usuarios acceso completo a determinados casos de la cuenta en lugar de acceso a todos los casos mediante una política de acceso de IAM, añádales al caso introduciendo su correo electrónico cuando cree el caso. Al añadir un usuario a un caso que haya creado, tendrá acceso para ver, editar y actualizar solo ese caso en la cuenta. También recibirá notificaciones cuando haya actualizaciones en el caso.

Para los usuarios de la infraestructura clásica que anteriormente utilizaban permisos de la infraestructura clásica para asignar acceso a casos de soporte, estos permisos están ahora disponibles en [grupos de acceso de permisos migrados de la infraestructura clásica](/docs/iam/infrastructureaccess.html#predefined). Los grupos de acceso de permisos migrados incluyen la política de IAM sobre el servicio de gestión de usuarios con el rol de Visor asignado.

Para asignar a un usuario una política de acceso de IAM sobre un servicio de gestión de cuentas, como el servicio del Centro de soporte o el servicio de gestión de usuarios, siga estos pasos:

1. En la barra de menús, pulse **Gestionar** &gt; **Acceso (IAM)** y seleccione **Usuarios**.
2. Seleccione un usuario de la lista.
3. Pulse **Políticas de acceso**.
4. Pulse **Asignar acceso**.
5. Seleccione **Asignar acceso a servicios de gestión de cuentas**.
6. Seleccione un servicio de la lista. 
5. Seleccione el rol para asignar el acceso deseado.

Consulte la tabla siguiente para ver exactamente los permisos que se incluyen en cada rol.

| Rol | Acción | 
|--------|---------------|
|Visor  | Ver y buscar casos |
|Administrador | Ver, buscar, crear y actualizar casos|
{: caption="Tabla 1. Roles y acciones para el servicio del Centro de soporte" caption-side="top"}

