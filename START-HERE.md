# Trois parcours hors ligne · Three offline paths · Tres recorridos sin conexión

Ces parcours utilisent des données synthétiques. Aucun ne demande une clé TypeSafe ou ne mesure la qualité du modèle. Choisissez le mécanisme que vous voulez essayer, puis ouvrez une issue dans le dépôt concerné avec une commande reproductible et le résultat observé.

These paths use synthetic data. None requires a TypeSafe key or measures model quality. Choose the mechanism you want to try, then open an issue in the relevant repository with a reproducible command and observed result.

Estos recorridos usan datos sintéticos. Ninguno requiere una clave de TypeSafe ni mide la calidad del modelo. Elija el mecanismo que quiera probar y abra una incidencia en el repositorio correspondiente con un comando reproducible y el resultado observado.

| Parcours / Path / Recorrido | Ce que vous verrez / What you will see / Qué verá | Commande / Command / Comando |
| --- | --- | --- |
| [DecisionPacks](https://github.com/gbesse/decisionpacks) | Décision bornée et trace de règles / Finite decision and rule trace / Decisión acotada y traza de reglas | `npm run demo` |
| [Jev Pairs](https://github.com/gbesse/jev-pairs) | Volume de paires et pertes du filtrage / Pair volume and blocking losses / Volumen de pares y pérdidas del filtrado | `PYTHONPATH=src python3 -m examples.blocking_audit` |
| [Unity Jev Behavior](https://github.com/gbesse/unity-jev-behavior) | Réponse HTTP authentifiée d’une passerelle locale / Authenticated response from a local gateway / Respuesta autenticada de una pasarela local | `cd gateway && npm ci && npm run demo:fixture` |

Clonez d'abord le dépôt choisi et exécutez la commande à sa racine. Pour Unity, la commande démarre uniquement la passerelle synthétique ; le nœud Behavior doit être vérifié dans l’éditeur Unity.

Clone the chosen repository first and run its command from the repository root. For Unity, the command starts only the synthetic gateway; verify the Behavior node in the Unity editor.

Clone primero el repositorio elegido y ejecute el comando desde su raíz. En Unity, el comando inicia solo la pasarela sintética; compruebe el nodo Behavior en el editor de Unity.
