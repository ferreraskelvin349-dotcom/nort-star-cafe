# North Star Cafe Fire TV — AutoBuild

Este proyecto genera un APK firmado en GitHub Actions sin Android Studio.

## Uso rápido
1. Cree un repositorio privado en GitHub.
2. Suba TODO el contenido de esta carpeta a la raíz del repositorio.
3. Abra la pestaña **Actions**.
4. Abra **Build North Star Fire TV APK**.
5. Pulse **Run workflow**.
6. Cuando termine en verde, abra la ejecución y descargue el artifact **NorthStarCafe-FireTV-APK**.
7. Descomprima el artifact; encontrará `NorthStarCafe-FireTV-v1.0.0.apk`.
8. Suba ese APK en Amazon Developer en **Upload your app file**.

## IMPORTANTE — NO PIERDA ESTOS ARCHIVOS
`northstar-release.jks` y `keystore.properties` son la firma permanente de la app. Guárdelos de forma privada. Amazon exige conservar la misma firma para futuras actualizaciones.

La app abre:
https://northstarcafemenu.com/?tv=1

Package ID:
com.northstarcafe.tv
