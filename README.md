# MLOPSII-tp5

## Mini-TP 5 — Aprendizaje federado

Simulación de FedAvg con 5 clientes (2 por ronda, 20 rondas) sobre el dataset `digits`,
comparada contra el entrenamiento centralizado.

| | accuracy | costo |
|---|---|---|
| centralizado | 0.969 | — |
| FedAvg IID | 0.971 | ≈0 |
| FedAvg non-IID | 0.942 | −2.6 puntos, curva inestable |
| + ruido DP σ = 0.05 / 0.1 / 0.2 | 0.955 / 0.932 / 0.888 | −1.6 / −3.9 / −8.3 puntos |

**Qué noté:** federar no cuesta accuracy si los datos de los clientes son parecidos; el costo
aparece cuando cada cliente ve pocas clases (non-IID), y la privacidad formal (ruido) es lo que más
cuesta. Para mi proyecto (Gout), federar sería forzado: las 9 sucursales son de la misma empresa y
el dato ya se centraliza.
