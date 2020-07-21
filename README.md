This repository contains the resultats of the various experiments presented in the article.

Are provided the annotated nearest neighbors of the centroids for:
* -*eur* agent nouns (neighbors_eurANs.csv)
* functional agent nouns (f-relevant-neighbors.csv)
* occasional agent nouns (o-relevant-neighbors.csv)
* behavioral agent nouns (b-relevant-neighbors.csv)

Neighbors are presented in .csv files composed of 7 columns separated by tabulations. Each entry contains:
* the neighbor associated to the part-of-speech label given by the parser (NEIGHBOR)
* its morphological type (MORPH)
* its base part-of-speech when relevant (G.BASE)
* its base semantic type when relevant (S.BASE, among "affixed", "conversion", "compound", "complexe", "simple", "extragram", "undet")
* its exponent when relevant(AFFIX)
* its rank in the neighborhood (RANK)
* its proximity score to the centroid (COS)

Neighbors lists for functional, occasional and behavioral agent nouns centroids contains 4 more columns:
* CENTROID: indicating the centroid to which neighborhood the noun belongs ("f" stands for functional, "o" for occasional, and "b" for behavioral)
* C1, C2 and C3: indicating whether the noun validates (1) or not (0) conditions 1, 2 and 3

Are also given the proximity scores to various centroids of:
* functional seeds (proximity_FITs.txt)
* occasional seeds (proximity_OITs.txt)
* behavioral seeds (proximity_BITs.txt)
* denominal candidates ending in -*eur* (proximity_eurDenom_ANcandidates.txt)
* candidates ending in -*aire* (proximity_aire_ANcandidates.txt)
* candidates ending in -*ant* (proximity_ant_ANcandidates.txt)
* candidates ending in -*ien* (proximity_ien_ANcandidates.txt)
* candidates ending in -*ier* (proximity_ier_ANcandidates.txt)
* candidates ending in -*iste* (proximity_iste_ANcandidates.txt)
* candidates in a converse relation to verbs, but undetermined as regards the orientation of the conversion (proximity_converse_ANcandidates.txt)
* simple nouns candidates (proximity_simple_ANcandidates.txt)

The proxmity files for functional, occasional and behavioral seeds contain 3 columns separated by tabulations. Each entry contains:
* the noun with its part-of-speech label
* the type of agent noun ("F" stands for functional, "O" for occasional, and "B" for behavioral)
* the proximity score of the noun to its centroid (between 0 and 1, dec = .)

The proximity files for agent nouns candidates contain 5 columns separated by tabulations. Each entry contains:
* the candidate (CANDIDATE)
* its proximity score (between 0 and 1, dec = .) to the -*eur* agent nouns centroid (-*eur* ANs)
* its proximity score (between 0 and 1, dec = .) to the general and phasic human nouns centroid (G/P HNs)
* its proximity score (between 0 and 1, dec = .) to the relational human nouns centroid (Rel. HNs)
* its proximity score (between 0 and 1, dec = .) to the demonyms centroid (Demonyms)

Lastly, are provided the clustering of functional, occasional, and behavioral agent noun seeds in the 5 models (FOB_clustering_model\*.txt). These files contain 3 columns separated by tabulations. Each entry contains:
* the functional, occasional or behavioral agent noun (VECTOR)
* the type of agent noun ("F" stands for functional, "O" for occasional, and "B" for behavioral)
* the cluster it was assigned to (1, 2 or 3)
