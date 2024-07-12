- https://docs.google.com/document/d/1QKjn2hNTKZLEOXJQbMcw8Pqj1VCCyXok7VNJh51EdCs/edit#

| score               |
| ------------------- |
| 3: strong accept    |
| 2: accept           |
| 1: weak accept      |
| 0: borderline paper |
| -1: weak reject     |
| -2: reject          |
| -3: strong reject   |


**Overall evaluation.*** Please provide a detailed review, including a justification for your scores. Both the score and the review text are required.

I'd like to thank the authors for their interesting submission!

The authors provide a new framework and implementation to include fairness regularization terms ("fairrets") in Pytorch. They provide examples of how different group fairness metrics can be mapped onto said "fairrets" to include these during model training as an additional loss term, thereby optimizing for fairness besides just performance.

The authors provide an interesting new contribution and especially the flexibility of the approach to represent a wide array of metrics is promising. The goal of developing a library around the approach is a welcome addition, providing practical use of the findings. Given that the development of different fairness processing techniques is still an ongoing field of research, the work is relevant to the EWAF academic field. The work is clearly written, although the authors could more clearly differentiate between the fairness definition and the regularization term in the discussion of the experimental results, as one may wish to explore different regularization terms, but should probably not "optimize" the fairness definition. Using the term "fairrets" exclusively here to refer to the intersection of both, may weaken this distinction. A nuanced discussion of the framework, in regards to its strengths and weaknesses and its relation to other techniques of fairness processing was lacking and would have been a nice addition to the work. Maybe the authors can elaborate on these aspects at the conference.

In the Experiments section, the authors may want to change their wording around the baseline condition, which is currently labelled as "Unfair". This wrongly suggests, that the alternative conditions are "fair". Using terminology such as "baseline", "naive" or "fairness unaware" may be more suitable here.

In Figure 2 and Appendix B the authors refer to confidence ellipses which seem not to be present in the figure (also when comparing it to its equivalent in the full paper). The figure should be updated to include confidence ellipses.


**Confidential remarks for the program committee.** If you wish to add any remarks intended only for PC members please write them below. These remarks will only be seen by the PC members having access to reviews for this submission. They will not be sent to the authors. This field is optional.