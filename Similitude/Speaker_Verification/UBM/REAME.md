## Construcción de un UBM 

1. Para la feature extraction se uso los MFFC con 20 coeficientes
2. Se empleo los audios de los speakers del VTK courpus con id: 
225
228
229
230
231
233
236
239
240
244
226
227
232
243
254
256
258
259
270
273
3. Se entreno un modelo GMM con [200, 250, 300, 350, 400, 500, 800] componentes y la covariance_type de tipo diagonal, usando 15 iteraciones.
4. Luego de ser entrenadas, se emplean el criterio de información de Akaike para el modelo actual en la entrada X. (BIC) y el Criterio de información bayesiano para el modelo actual en la entrada X. (BIC). para evaluar el número de componentes.
5. Se realiza una GMM-adaptation usando el método Quasi-Bayesian Adaptation(QB), MLLR Adaptation
 https://github.com/mrhuke/GMM-adaptation/blob/master/mllrgmm.py

6. Para el calcula de las distancias se emplea la la divergencia de Kullback-leibler


