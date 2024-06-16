# IPSec

IPSec es un protocolo diseñado para poder conectar clientes en una RPV, redes privadasd virtuales, y aplicar cifrados, control de integridad a los datos y autenticacin; IPsec es un  protocolo de nivel de enlace que proporcina seguridad, Capa 3, estandarizado para Ipv4, IPv6.

Se establecen dos tuneles por fases:

Fase 1:

IKE ( autenticación )  la fase 1 de IKE es establecer un túnel seguro que podamos usar para la fase 2 de IKE. Negociación. El par que tenga tráfico que deba protegerse iniciará la negociación de fase 1 de IKE. Los dos pares negociarán sobre los siguientes puntos:

· Hashing : usa un algoritmo hash para verificar la integridad, utilizamos MD5 o SHA (SHA-1 o SHA-2).
· Autenticación : utiliza clave precompartida o certificado digital.
· Grupo DH (Diffie Hellman)
· Vida útil :tiempo que dura el túnel IKE p.ej. 86400 segundos (1 día).
· Cifrado : algoritmo utilizado para el cifrado. Ppr ejemplo: DES , 3DES o AES .

Fase 2:

AH (Cabecera adicional IP, para control integridad, calcula un HASH y MAC clave simetrica, para comprobar en destino), 
ESP (Cifrado, es una etiqueta, encabezado y cola sobre el paquete IP +AH)

Dos posibles modos de uso; trasportel y tunel:

Trasporte, es cabecera AH, 

Tunel, se le etuqeta con IP origen y destino a todo el paquete IP`+AH.

La  diferencia entre los dos es que con el modo de transporte usaremos el encabezado IP original mientras que en el modo túnel usaremos un nuevo encabezado IP . 

IKEv2 admite la autenticación EAP (claves precompartida y certificado digital).


https://harrymaq.medium.com/what-is-ipsec-how-does-it-works-what-are-its-phases-and-modes-965b5523727c



# Cliente Pulse VPN para Linux
cliente VPN pulsesecure en bash shell Linux
