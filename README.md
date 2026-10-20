# mesaonce-hub-directory

Directorio **firmado** con la dirección vigente del hub de MesaOnce.

Si una caja pasa 10 minutos sin alcanzar el hub, descarga `hub-directory.json` y verifica la firma
Ed25519 con la clave pública que trae su instalador. Después se muda a la primera dirección que
la reconoce. Este repo no tiene secretos: sin la clave privada del hub, nadie puede firmar
un directorio válido, y la caja rechaza cualquier versión igual o anterior a la que ya aceptó.

Para publicar una dirección nueva, sigue el runbook RUN-031 §6 del repo de MesaOnce: firma
dentro del contenedor del hub con `DIR_VERSION` mayor a la actual, haz commit aquí y push.
