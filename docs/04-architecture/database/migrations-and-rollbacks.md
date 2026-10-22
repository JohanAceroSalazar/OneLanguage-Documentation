# Migraciones y rollback

`changelog-master.yaml` incluye DDL, DML, DCL y TCL. Las alteraciones 005–011 reubican autenticación, eliminan tablas obsoletas, agregan metadatos de grabación, restauran permisos, eliminan catálogos de traducción y retiran el permiso `files`. Se observaron rollbacks para la mayoría de cambios; el backfill 010 no declara rollback. Antes de aplicar un cambio: respalde la base, revise el changelog objetivo, pruebe en ambiente aislado y compruebe el rollback asociado. No se ejecutaron scripts en la auditoría.
