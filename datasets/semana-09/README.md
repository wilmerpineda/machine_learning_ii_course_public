# Datos · Semana 9

Submuestra reproducible de **Human Activity Recognition Using Smartphones**.
Contiene 3.600 ventanas: 20 por cada combinacion de 30 participantes y seis
actividades. Las 561 variables de tiempo y frecuencia ya estaban normalizadas
por los autores del conjunto.

## Archivos

- `har_features.npz`: matriz `X` en `float32`, forma `(3600, 561)`.
- `har_metadata.csv`: identificador, participante, actividad y particion original.
- `feature_names.txt`: nombres originales de las 561 columnas.
- `manifest.json`: procedencia, hash, licencia y protocolo de muestreo.

Las etiquetas no intervienen en el ajuste de PCA, t-SNE o UMAP. Se usan despues
para auditar si el mapa refleja actividad, participante o ambos.

## Fuente y licencia

Reyes-Ortiz, J., Anguita, D., Ghio, A., Oneto, L. y Parra, X. (2013).
*Human Activity Recognition Using Smartphones*. UCI Machine Learning Repository.
DOI: <https://doi.org/10.24432/C54S4K>. Licencia CC BY 4.0.

La preparacion se reproduce con:

```powershell
python scripts/prepare_week9_data.py --source "$env:TEMP\uci_har_240.zip"
```

