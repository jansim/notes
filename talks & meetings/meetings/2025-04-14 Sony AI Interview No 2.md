---
creation date: 2025-04-14 12:48
---

## Preparations
- https://viso.ai/computer-vision/bias-detection/
- human centric CV
	- more "loaded" / interpretation going on
- f1 score: harmonic mean of precision and recall (2 * (precision * recall / (precision + recall) ) )
- segmentation / bounding boxes
	- intersection over union: area of overlap over area of union (i.e. total area)
		- threshold IoU at different values
		- = Jaccard Index
		- mean IoU -> average over all classes
		- dice coefficient -> similar to IoU slightly different formula
		- 1 perfect; 0 awful
	- average precision (A)
		- summarizes precision recall curve
		- mean average precision (mAP)
			- AP across different classes
	- often reported at different thresholds mAP@0.5 ...
	- Rand Index
		- measure agreement
		- adjusted => correct for chance
- semantic segmentation
- instance segmentation
	- track an instance of an object
- panoptic segmentation = semantic + instance
- human foreground segmentation e.g. zoom bg
- human part segmentation
- crowd segmentation -> many people
- general image segmentation e.g. medical
- pose estimation
	- find body parts and "connect" them
	- useful for e.g. activity recognition, animation, driver monitoring
	- Percentage of Correct Parts (PCP)
		- is the position of the limb within threshold % of the ground truth based on actual limb size
	- Percentage of Correct Keypoints
		- position within threshold?
		- threshold often based on size (e.g. head) or torso
- **datasets**
	- Sony paper
		- CelebAMask-HQ
			- https://github.com/switchablenorms/CelebAMask-HQ
		- FFHQ Aging
			- https://github.com/royorel/FFHQ-Aging-Dataset
			- FFHQ
				- https://github.com/NVlabs/ffhq-dataset
				- NVIDIA from Flickr (license often CC BY)
		- CFD: https://www.chicagofaces.org/
			- CFD-India
		- Labeled Faces in the Wild (LFW)
	- Imagenet: 14MIL images now, central for CV
	- COCO (Common Objects in Context)
	- CelebFaces Attributes (CelebA)
	- Problematic / deprecated datasets
		- MegaFace -> used commercially despite license; used for e.g. surveillance tach
		- LAION-5B (full -> CP!)
		- Brainwash dataset -> no consent
- **ethics**
	- bias in race, gender, age, or body type
	- bias in labelling
		- labellers are not diverse
		- labellers project onto labels
- **comparisons**
	- saliency based image cropping
	- face verification: same person in two images?
	- gender / smile classification accuracy
- **potential things affecting stuff**
	- how does the mask affect score? (based on model)
	- how do the dlib points affect score? (based on model)
	- effect of averaging procedure?
	- labels: personal identification (i.e. someone identifies as X/Y)
	- effect of age?
	- effect of facial hair?
	- effect of lighting?
	- effect of Instagram filters?
## Follwup HR Meeting (2025-05-08)

### Questions

- Timing: July - September
- Salary:
	- 7000 - 8000 CHF?
		- 7000 = 84000
		- 8000 = 96000
	- Aktuell: 5100€ 
- What to say:
	- Really excited about internship
	- Delaying PhD graduation
	- Cost of moving / potentially paying double accomodation
	- Essentially PostDoc already (esp. by september)
- Housing: Tips? Resources?
	- Support for moving
- Vacation days?
	- I will need to take a few days off due to prior work commitments (external teaching)
	- Is this OK with company policy?
- Transportation
- Cross-border commuter?
- 



- 

