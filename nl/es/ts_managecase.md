---

copyright:

  years: 2015, 2019

lastupdated: "2019-02-19"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Resolución de problemas para gestionar casos de soporte
{: #Supportcases}

Es posible que encuentre problemas durante la creación y gestión de casos de soporte de {{site.data.keyword.Bluemix}}. En muchos de los casos, puede solucionar estos problemas siguiendo unos sencillos pasos.
{:shortdesc}

## ¿Por qué no puedo crear o editar casos de soporte? 
{: #ts_service_broker}

No se puede crear o editar un caso de soporte de {{site.data.keyword.Bluemix_notm}} y se muestra un mensaje de error que indica que no tiene el acceso adecuado. 
{:shortdesc}

Cuando intenta suprimir un caso, aparece el siguiente mensaje de error:   
{: tsSymptoms}

`Parece que no tiene acceso para crear casos para esta cuenta.`

Los problemas generales relacionados con el acceso y la gestión de casos de soporte pueden deberse a que no dispone de la política de acceso de Identity and Access Management (IAM) para el servicio de gestión de cuentas del Centro de soporte. Se le debe asignar el rol de editor o de administrador en el servicio de gestión de cuentas del centro de soporte para poder crear casos. 
{: tsCauses}

Para resolver el problema, el propietario de la cuenta, un administrador del servicio del centro de soporte o el administrador de todos los servicios de gestión de cuentas puede asignar una política de IAM sobre el centro de soporte para gestionar casos. 
{: tsResolve}

Si es el propietario de la cuenta o un administrador del Centro de soporte, siga los pasos siguientes para crear una política de acceso para trabajar con casos de soporte:

1. Vaya a **Gestionar** &gt; **Acceso (IAM)** y seleccione **Usuarios**.
2. Seleccione un nombre de usuario y pulse **Políticas de acceso**. 
3. Pulse **Asignar acceso**. 
4. Seleccione **Asignar acceso a servicios de gestión de cuentas**. 
5. En el menú **Servicio**, seleccione **Centro de soporte**. 
6. Seleccione un rol para definir el nivel de acceso para el usuario. 


## ¿Por qué no puedo ver todos los casos en la cuenta?
{: #ts_viewcasedetails}

No puede ver todos los casos de la cuenta porque no tiene acceso para ver a todos los usuarios de la cuenta. 
{:shortdesc}

Cuando intenta ver los casos de soporte asociados a la cuenta, no puede ver todos los casos abiertos. 
{: tsSymptoms}

El propietario de la cuenta ha establecido como restringido el [valor de visibilidad de la lista de usuarios](/docs/iam?topic=iam-userlistview#userlistview). Cuando el valor está establecido en restringido, y no tiene una política de acceso adicional para ver los usuarios de la cuenta, no tiene el acceso necesario para ver todos los casos de la cuenta. Solo puede ver los usuarios que ha invitado a la cuenta, aquellos con los que comparte pertenencia a una organización de Cloud Foundry o los que están en su jerarquía de usuarios de la infraestructura clásica. 
{: tsCauses}

Debe tener asignada una política de IAM con al menos el rol de Visor sobre el servicio de gestión de cuentas de gestión de usuarios, además de la política de acceso al servicio de gestión de cuentas del Centro de soporte. Para ver el acceso actual, vaya a **Gestionar** &gt; **Acceso (IAM)** y seleccione su nombre en la página **Usuarios**. Pulse el separador **Políticas de acceso** y revise las políticas asignadas. 
{: tsResolve}

Para solucionar el problema, póngase en contacto con el proveedor de la cuenta y solicite el acceso adecuado. 

## ¿Por qué no encuentro un caso que he creado previamente? 
{: #ts_viewarchivedcase}

No encuentra los casos que ha creado antes de la experiencia de plataforma mejorada de {{site.data.keyword.Bluemix_notm}}. 
{:shortdesc}

En el separador **Gestionar casos** del centro de soporte, no encuentra ningún caso creado antes del 2 de diciembre de 2018. 
{: tsSymptoms}

Los casos abiertos antes del 2 de diciembre de 2018 solo son visibles desde **Ver casos archivados**. 
{: tsCauses}

Para ver los casos, vaya a **Soporte**, seleccione **Gestionar casos** y pulse **Ver casos archivados**.
{: tsResolve} 






