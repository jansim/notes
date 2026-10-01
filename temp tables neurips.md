







EqOddsDiff

|                              | Full Corpus* | Open<br>(all)* | Open<br>(large)* | Open<br>(small)* | [ABCFair](https://openreview.net/forum?id=ByknnPI5Km) | [AIF360](https://doi.org/10.1147/JRD.2019.2942287) | [Friedler](https://doi.org/10.1145/3287560.3287589) | "Typical 3" |
| ---------------------------- | ------------ | -------------- | ---------------- | ---------------- | ----------------------------------------------------- | -------------------------------------------------- | --------------------------------------------------- | ----------- |
| DisparateImpactRemover (pre) | ️✓           | ️✓             | ️✓               | ️✓               | ✓                                                     |                                                    | ️✓                                                  |             |
| LFR (pre)                    | ️✓           | ️✓             | ️✓               | ️✓               | ️                                                     | ️✓                                                 | ️✓                                                  | ️✓          |
| GridSearchReduction (in)     | ️✓           | ️✓             | ️✓               | ️✓               | ️✓                                                    | ️✓                                                 | ️✓                                                  | ️✓          |
| AdversarialDebiasing (in)    | ️✓           | ️✓             | ️✓               | ️✓               | ️✓                                                    | ️✓                                                 | ️✓                                                  | ️✓          |
| MetaFairClassifier (in)      | ️✓           | ️✓             | ️✓               |                  | ️✓                                                    | ️✓                                                 | ️✓                                                  | ️✓          |
| GerryFairClassifier (in)     | ️✓           | ️✓             | ️✓               | ️✓               | ️✓                                                    | ️✓                                                 |                                                     |             |
| CalibratedEqOdds (post)      | ️✓           | ️✓             | ️✓               | ✓                | ✓                                                     |                                                    |                                                     |             |
| **No. of Datasets**          | 44           | 32             | 16               | 5                | 7                                                     | 7                                                  | 5                                                   | 3           |

Both

|                              | Full Corpus* | Open<br>(all)* | Open<br>(large)* | Open<br>(small)* | [ABCFair](https://openreview.net/forum?id=ByknnPI5Km) | [AIF360](https://doi.org/10.1147/JRD.2019.2942287) | [Friedler](https://doi.org/10.1145/3287560.3287589) | "Typical 3" |
| ---------------------------- | ------------ | -------------- | ---------------- | ---------------- | ----------------------------------------------------- | -------------------------------------------------- | --------------------------------------------------- | ----------- |
| DisparateImpactRemover (pre) | ️✓ / ✓       | ️✓ / ✓         | ️✓ / ✓           | ️✓ / ✓           | ✓ / ✓                                                 | X / ✓                                              | ️✓ / ✓                                              | X / X       |
| LFR (pre)                    | ️✓ / ✓       | ️✓ / ✓         | ️✓ / ✓           | ️✓ / ✓           | X / X️                                                | ️✓ / ✓                                             | ️✓ / ✓                                              | ️✓ / ✓      |
| GridSearchReduction (in)     | ️✓ / ✓       | ️✓ / ✓         | ️✓ / ✓           | ️✓ / ✓           | ️✓ / ✓                                                | ️✓ / ✓                                             | ️✓ / ✓                                              | ️✓ / ✓      |
| AdversarialDebiasing (in)    | ️✓ / ✓       | ️✓ / ✓         | ️✓ / ✓           | ️✓ / ✓           | ️✓ / ✓                                                | ️✓ / ✓                                             | ️✓ / ✓                                              | ️✓ / ✓      |
| MetaFairClassifier (in)      | ️✓ / ✓       | ️✓ / ✓         | ️✓ / ✓           | X / ✓            | ️✓ / ✓                                                | ️✓ / ✓                                             | ️✓ / ✓                                              | ️✓ / ✓      |
| GerryFairClassifier (in)     | ️✓ / ✓       | ️✓ / ✓         | ️✓ / ✓           | ️✓ / ✓           | ️✓ / ✓                                                | ️✓ / ✓                                             | X / X                                               | X / X       |
| CalibratedEqOdds (post)      | ️✓ / ✓       | ️✓ / ✓         | ️✓ / ✓           | ✓ / ✓            | ✓ / ✓                                                 | X / X                                              | X / X                                               | X / X       |
| **No. of Datasets**          | 44           | 32             | 16               | 5                | 7                                                     | 7                                                  | 5                                                   | 3           |

Emoji Version


|                              | Full Corpus* | Open<br>(all)* | Open<br>(large)* | Open<br>(small)* | [ABCFair](https://openreview.net/forum?id=ByknnPI5Km)ᵃ | [AIF360](https://doi.org/10.1147/JRD.2019.2942287)ᵇ | [Friedler](https://doi.org/10.1145/3287560.3287589) | "Typical 3" |
| ---------------------------- | ------------ | -------------- | ---------------- | ---------------- | ------------------------------------------------------ | --------------------------------------------------- | --------------------------------------------------- | ----------- |
| DisparateImpactRemover (pre) | ️✅️ / ✅️     | ️✅️ / ✅️       | ️✅️ / ✅️         | ️✅️ / ✅️         | ✅️ / ✅️                                                | ❌️ / ✅️                                             | ️✅️ / ✅️                                            | ❌️ / ❌️     |
| LFR (pre)                    | ️✅️ / ✅️     | ️✅️ / ✅️       | ️✅️ / ✅️         | ️✅️ / ✅️         | ❌️ / ❌️️                                               | ️✅️ / ✅️                                            | ️✅️ / ✅️                                            | ️✅️ / ✅️    |
| GridSearchReduction (in)     | ️✅️ / ✅️     | ️✅️ / ✅️       | ️✅️ / ✅️         | ️✅️ / ✅️         | ️✅️ / ✅️                                               | ️✅️ / ✅️                                            | ️✅️ / ✅️                                            | ️✅️ / ✅️    |
| AdversarialDebiasing (in)    | ️✅️ / ✅️     | ️✅️ / ✅️       | ️✅️ / ✅️         | ️✅️ / ✅️         | ️✅️ / ✅️                                               | ️✅️ / ✅️                                            | ️✅️ / ✅️                                            | ️✅️ / ✅️    |
| MetaFairClassifier (in)      | ️✅️ / ✅️     | ️✅️ / ✅️       | ️✅️ / ✅️         | ❌️ / ✅️          | ️✅️ / ✅️                                               | ️✅️ / ✅️                                            | ️✅️ / ✅️                                            | ️✅️ / ✅️    |
| GerryFairClassifier (in)     | ️✅️ / ✅️     | ️✅️ / ✅️       | ️✅️ / ✅️         | ️✅️ / ✅️         | ️✅️ / ✅️                                               | ️✅️ / ✅️                                            | ❌️ / ❌️                                             | ❌️ / ❌️     |
| CalibratedEqOdds (post)      | ️✅️ / ✅️     | ️✅️ / ✅️       | ️✅️ / ✅️         | ✅️ / ✅️          | ✅️ / ✅️                                                | ❌️ / ❌️                                             | ❌️ / ❌️                                             | ❌️ / ❌️     |
| **No. of Datasets**          | 44           | 32             | 16               | 5                | 5                                                      | 7                                                   | 5                                                   | 3           |



| Library                                                  | Main Focus                           | # Datasets (# covered by FairGround) | # Fairness Methods | Meta-Features Available | Collections Available |
| -------------------------------------------------------- | ------------------------------------ | ------------------------------------ | ------------------ | ----------------------- | --------------------- |
| [ABCFair](https://openreview.net/forum?id=ByknnPI5Km)    | data,<br><br>methods,<br><br>metrics | 7 (5)                                | 10                 | X                       | X                     |
| [Aequitas Flow](http://jmlr.org/papers/v25/24-0677.html) | methods,<br><br>metrics, guides      | 11 (11)                              | 10                 | X                       | X                     |
| [AIF360](https://doi.org/10.1147/JRD.2019.2942287)       | methods,<br><br>metrics              | 8 (8)                                | 15                 | X                       | X                     |
| [Fairlearn](http://jmlr.org/papers/v24/23-0389.html)     | methods, metrics, guides             | 6 (4)                                | 6                  | X                       | X                     |
| FairGround (ours)                                        | data                                 | 44                                   | 7*                 | ✓                       | ✓                     |


Emoji Version


| Library                                                  | Main Focus                           | # Datasets (# covered by FairGround) | # Fairness Methods | Meta-Features Available | Collections Available |
| -------------------------------------------------------- | ------------------------------------ | ------------------------------------ | ------------------ | ----------------------- | --------------------- |
| [ABCFair](https://openreview.net/forum?id=ByknnPI5Km)    | data,<br><br>methods,<br><br>metrics | 7 (5)                                | 10                 | ❌️                      | ❌️                    |
| [Aequitas Flow](http://jmlr.org/papers/v25/24-0677.html) | methods,<br><br>metrics, guides      | 11 (11)                              | 10                 | ❌️                      | ❌️                    |
| [AIF360](https://doi.org/10.1147/JRD.2019.2942287)       | methods,<br><br>metrics              | 8 (8)                                | 15                 | ❌️                      | ❌️                    |
| [Fairlearn](http://jmlr.org/papers/v24/23-0389.html)     | methods, metrics, guides             | 6 (4)                                | 6                  | ❌️                      | ❌️                    |
| FairGround (ours)                                        | data                                 | 44                                   | 7*                 | ✅️                      | ✅️                    |
