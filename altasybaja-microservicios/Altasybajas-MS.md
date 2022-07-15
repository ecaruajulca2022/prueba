# Dar de baja un Microservicio con infraestrucura mediante Argocd

1ro: Approbar y merged el PR

[![Approve-PR.png](prueba/altasybaja-microservicios/Imagenes/Approve-PR.png)]

2do: Verificar en donde vive el microservicio  en este caso solo vive en mx

[![Donde-vive-mx.png](../altasybaja-microservicios/Imagenes/Donde-vive-mx.png)]

3ro. Verificar que cosas tiene como por ejemplo:

secret, bd, agent 

En caso tenga bd:

consultar si se puede eliminar la bd o necesitan que guarde un backup de la bd sino tagear al @bd y luego eliminar del vault.

4to: Ir a la familia del microservicio y verificar que el picoservico tenga marcado una x .

Para eso primero se debe ir al agente en este caso mx-agent

[![Agente.png](https://i.postimg.cc/rsXttCkW/Agente.png)](https://postimg.cc/qhw7PKgM)


[![Familia.png](https://i.postimg.cc/tRNg5Hd8/Familia.png)](https://postimg.cc/mhhRLJ5S)

Luego ir a la familia:

[![Familia-sale.png](https://i.postimg.cc/6qbJmzp4/Familia-sale.png)](https://postimg.cc/Cn8QZGDw)

Si se aprobo el PR deberia estar con una x de color amarillo la familia ms-values/sale/billing-sat-importer-worker

[![Pico-marcado-x.png](https://i.postimg.cc/m2154Td5/Pico-marcado-x.png)](https://postimg.cc/w7HVcYYX)

[![APP-detalles.png](https://i.postimg.cc/5ysYkcz5/APP-detalles.png)](https://postimg.cc/SYzxJvDj)

5to:

 Deshabilitar el “auto enable sync” en la familia para que no vuelva a correr la aplicación.

Tal como se muestra en la imagen:

[![Deshabilitar-el-auto-sync.png](https://i.postimg.cc/gk06LJ9g/Deshabilitar-el-auto-sync.png)](https://postimg.cc/bdKvKqwn)

[![Ingresando-al-Picoservicio.png](https://i.postimg.cc/y8mBVmft/Ingresando-al-Picoservicio.png)](https://postimg.cc/ZW5XHdzx)

[![Aplicaci-n-ms.png](https://i.postimg.cc/Wbjc5Fp7/Aplicaci-n-ms.png)](https://postimg.cc/dDWf10y7)

[![ms.png](https://i.postimg.cc/XYR8gF4j/ms.png)](https://postimg.cc/v4vfY44k)

[![Detele.png](https://i.postimg.cc/jq1JNTsK/Detele.png)](https://postimg.cc/14pthLnY)

[![Delete-ms.png](https://i.postimg.cc/x8LJnkBR/Delete-ms.png)](https://postimg.cc/QKxxqM89)

[![Deleted.png](https://i.postimg.cc/85RNChPj/Deleted.png)](https://postimg.cc/Q9dR4K73)

[![Delete-pico.png](https://i.postimg.cc/KzqQBWYV/Delete-pico.png)](https://postimg.cc/njmvt0BY)

[![Delete-pico2.png](https://i.postimg.cc/P5jctBvz/Delete-pico2.png)](https://postimg.cc/xc6g5pRc)

6to //Eliminar el secret y la bd

****cluster-mx/ms-secrets/sale/billing-sat-importer/postgres****

[![Vault.png](https://i.postimg.cc/2Skw9mBJ/Vault.png)](https://postimg.cc/qzFygPwX)
