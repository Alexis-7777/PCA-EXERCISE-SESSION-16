# How many worlds? UN countries through PCA and clustering

**Main finding:** two clusters provide the clearest statistical separation; four offer a useful descriptive view with weaker separation.

## Answers to the six research questions

### 1. Can the world be meaningfully divided into only two clusters?

**Yes as a coarse statistical summary, but not as two homogeneous categories called “developed” and “developing”.** The preferred two-group model separates 60 countries/territories with greater health and social disadvantage from 138 with better average outcomes. The second cluster remains very diverse: Malaysia, China, Cuba, Japan and the United States share it. Two clusters capture only 48.40% of dispersion in the retained PCA space, leaving substantial within-group differences.

### 2. How many clusters do the elbow and other metrics suggest?

**k=2 is the best-supported statistical choice for the main ten-indicator model.** The largest elbow bend is at two and its silhouette is 0.442, versus 0.283 for three and 0.284 for four. The inertia reduction is 48.40% from one to two, 18.88% from two to three, and 15.20% from three to four, followed by smaller gains. There is no strong second elbow establishing four. The PCA plots show overlapping groups rather than four isolated clouds.

We therefore retain k=2 as our preferred model and use k=4 as a richer descriptive comparison. Selection is sensitive to which variables define development: a separate model using only the four class indicators favors k=3 by silhouette. Log GDP and complete-case checks continue to favor k=2 for the ten-indicator approach.

### 3. How much structure do two clusters capture compared with the preferred number?

Our preferred number is two, so that literal comparison is identical. For a meaningful richer alternative, compare two with four:

| Measure | k=2, preferred | k=4, descriptive alternative |
|---|---:|---:|
| Within-cluster sum of squares in retained PCA space | 952.34 | 655.10 |
| PCA-space dispersion represented by cluster centers | 48.40% | 64.51% |
| Full ten-variable standardized dispersion represented | 45.15% | 60.56% |
| Mean silhouette | 0.442 | 0.284 |

Four clusters capture **16.10 percentage points** more PCA-space dispersion and reduce remaining within-cluster sum of squares by **31.21%** relative to two. This is a real gain in descriptive resolution, but adding clusters mechanically improves fit. The weaker silhouette indicates less distinct groups. These percentages are `1 − within-cluster SS / total SS`, not prediction accuracy, a fraction of countries correctly classified, or PCA explained variance.

### 4. Does this support Factfulness's argument for four or more groups?

**It supports the warning against simplistic binary labels, but it does not establish four or more natural clusters.** Four groups expose differences hidden in the broad two-group model, while separation metrics prefer two. Gapminder's four income levels describe people and households along an income spectrum. Our model groups equally weighted countries/territories using several indicators, including GDP per person. It cannot validate those household income bands or describe within-country inequality. This distinction follows [Gapminder's explanation of income levels](https://www.gapminder.org/fw/income-levels/).

### 5. What does PCA tell us about the variables that differentiate countries?

Five components retain **93.22%** of standardized variance. Two retain only **69.62%**, so clustering only the plotted two would discard too much information.

| Component | Variance explained | Cumulative |
|---|---:|---:|
| PC1 | 58.39% | 58.39% |
| PC2 | 11.23% | 69.62% |
| PC3 | 10.81% | 80.43% |
| PC4 | 7.83% | 88.26% |
| PC5 | 4.96% | 93.22% |

PC1 contrasts longer life expectancy and greater contraception use with high infant mortality, fertility and illiteracy. Its largest absolute coefficients are female life expectancy (+0.394), infant mortality (−0.389), male life expectancy (+0.381) and fertility (−0.372). Their squared contributions are about 15.5%, 15.1%, 14.5% and 13.8% of PC1, respectively.

PC2 is dominated by female economic activity (+0.845, about 71.4% of its squared coefficients), followed by male economic activity (+0.439). PC3 gives substantial weight to GDP (+0.512), male illiteracy (+0.433) and female illiteracy (+0.412), with economic activity also contributing. PCA therefore reveals several dimensions rather than a single income ranking. Signs can flip without changing the analysis. PCA usefully halves the number of dimensions, but it does not remove missingness bias or guarantee natural clusters.

### 6. How do representative countries explain the clusters?

### Preferred model: two clusters

**Group 1: greater health and social disadvantage (60 countries/territories). Representative: Haiti.** Haiti has GDP per person of $386, female life expectancy of 56.0 years, and infant mortality of 82 per 1,000. These are close to the cluster medians of $381, 53.7 years and 86. Haiti's fertility of 4.6 is below the group median of 5.45, showing that a representative need not match every indicator. Its 57.8% female illiteracy is close to the group median of 58.2%. Many members are African countries, but Haiti, India and Pakistan also belong here. That geographic mixture shows why the model should not be interpreted as a continent label.

**Group 2: better average health and social outcomes, with varied incomes (138 countries/territories). Representative: Malaysia.** Malaysia has GDP per person of $4,313, female life expectancy of 74.3 years and infant mortality of 11, compared with medians of $3,248, 75.3 years and 17. Its fertility of 3.24 and female illiteracy of 21.9% exceed the cluster medians of 2.31 and 9.0%, so it is not typical on every dimension. Malaysia is the closest fully observed country to this centroid, yet the same cluster includes China, Brazil, Cuba, Japan and the United States. Calling all of these places uniformly “developed” would conceal substantial differences. In the historical file, China has GDP per person of $582 and Japan $41,718, despite sharing this broad group.

### More detailed comparison: four clusters

| Group | Size | Representative | Cluster GDP median (US$) | Female life expectancy median (years) | Infant mortality median (per 1,000) | Female economic activity median (%) |
|---|---:|---|---:|---:|---:|---:|
| 1 | 51 | Togo | 355 | 52.2 | 92 | 49.0 |
| 2 | 32 | Nicaragua | 1,655 | 70.3 | 39 | 26.1 |
| 3 | 84 | Trinidad and Tobago | 2,442 | 74.4 | 19 | 51.1 |
| 4 | 31 | United States | 23,530 | 80.2 | 6 | 51.5 |

**Group 1: lowest income and weakest health outcomes.** Togo's GDP per person of $322, female life expectancy of 51.5 years and infant mortality of 86 are close to the group medians. Its fertility of 6.08 and female illiteracy of 63% are also consistent with the group's high fertility and illiteracy. Haiti, Laos and Bangladesh appear alongside many African countries, so shared measured conditions cross geographic boundaries. Togo's economic activity is not especially low, which illustrates that participation alone is not a measure of prosperity.

**Group 2: intermediate health outcomes and lower female economic activity.** Nicaragua's female life expectancy of 70.6 years and infant mortality of 44 resemble the group medians of 70.3 and 39. Female economic activity is 33.4%, compared with the group's 26.1% and roughly 49–52% in the other groups. Its GDP per person of $464 is well below the group median, so it represents the combined profile better than the income level. Saudi Arabia is also in this group despite much higher GDP ($6,583): its low female economic activity (6.9%), high fertility (5.9), and high female illiteracy (49.8%) help explain the assignment. The data establish similarity on the indicators, not a common cause.

**Group 3: relatively good health and literacy with a broad income range.** Trinidad and Tobago has female life expectancy of 76.2 years, infant mortality of 14 and female illiteracy of 3%, compared with group medians of 74.4, 19 and 4.7%. Its GDP of $4,083 exceeds the group median of $2,442. China, Brazil and Cuba are also members. Cuba's female life expectancy of 78 years and infant mortality of 9 sit alongside GDP of $1,983, illustrating that health and GDP need not move in lockstep.

**Group 4: highest income and longest lives.** The United States has GDP per person of $26,037, female life expectancy of 80.1 years and infant mortality of 7, close to medians of $23,530, 80.2 and 6. Its female economic activity of 59.3% is above the group's 51.5%. Japan and many Western European countries join this cluster, but so do territories such as Puerto Rico and Réunion. Literacy is observed for only 11 of its 31 members: do not infer that this group is less literate than group 3 from the incomplete literacy medians.

All six representatives have observed values for all ten model inputs. They are selected by distance in the full five-component space, not by appearance on the two-dimensional plot. Cluster names describe this sample and are not official classifications or Gapminder income levels.

## Data preparation and method

- Source: [the assigned UN.csv](https://raw.githubusercontent.com/manoelgadi/PSDMA/refs/heads/main/datasets/UN.csv). Its schema matches [UN98, compiled around 1998](https://vincentarelbundock.github.io/Rdatasets/doc/carData/UN98.html). This is historical evidence, not a 2026 country ranking.
- Start with 207 rows and 12 numerical indicators. Preserve `country` and `region` only as descriptive fields. No duplicate countries or rows occur.
- Drop the two education indicators because each lacks 131/207 values (63.29%). The feature exclusion threshold is over 40% missingness. Retain the other ten indicators, whose missingness ranges from 2.90% to 30.43% in the original file.
- Exclude nine rows with more than five of those ten indicators missing: Andorra, Dominica, East Timor, Gaza Strip, Liechtenstein, Monaco, Tuvalu, Virgin Islands and Western Sahara. Analyze 198 rows. Original spellings remain in the CSV.
- Median-impute 224 of 1,980 retained cells (11.31%). Flag, retain and document outliers using 1.5 × IQR on observed retained values. Unusual values are relevant observations rather than established errors. Keep raw measurements and imputation counts separately.
- Standardize all ten model variables to mean zero and population standard deviation one. Fit full PCA, retain the first five components, and do not whiten them. Fit K-Means for k=1–8 using 50 initializations and seed 42.
- Calculate silhouette and inertia in all five retained PCs. Use the first two PCs only for visualization. Label clusters in ascending order of observed median GDP for readability, without changing their membership.
- Select each representative as the closest fully observed member to the centroid in the retained PCA space. Interpret observed cluster medians and report their observation counts.

## Robustness and limitations

Log GDP still favors two clusters (silhouette 0.460), with ARI 0.979 against the main two-group partition. Among 97 complete cases, k=2 again has the best silhouette (0.431), and its assignments agree with the main model on those same rows (ARI 1.000). Four-group assignments change more: ARI 0.541 for log GDP and 0.637 for complete cases. These ARIs compare partitions, not accuracy against ground truth.

Using only the four class indicators favors three groups, showing that “how many worlds” depends on what we measure. Ten random seeds with 50 starts reproduce the two-group partition exactly; the four-group ARI ranges from about 0.972 to 1.000. Stable initializations do not establish real-world validity.

Median imputation can artificially pull observations toward the middle. The education exclusions narrow the meaning of development, although literacy remains included. Missingness is unlikely to be random, and complete cases are a selected sample. The source itself imputed some literacy observations. Correlated male/female health and literacy measures effectively give those themes repeated influence. GDP has a long upper tail. K-Means assumes Euclidean geometry and works best for roughly spherical groups. Historical country averages cannot establish causes, capture inequality within countries, or assign people to Gapminder income levels. Each country/territory counts once regardless of population.


## Visual evidence

![PCA explained variance](figures/03_pca_variance.png)

![Elbow and silhouette](figures/05_cluster_selection.png)

![Two versus four clusters](figures/06_pca_clusters.png)

![Representative countries](figures/07_representative_countries.png)

## Open and reproduce

### Google Colab

1. Open [Google Colab](https://colab.research.google.com/) and upload `UN_PCA_Clustering.ipynb`.
2. Select **Runtime → Run all**. The notebook reads a local `UN.csv` if available, otherwise downloads the assigned URL automatically.
3. Review the saved outputs, answers and country discussion. The notebook creates `figures/` and `results/` in the current runtime. Download outputs you want to keep before the Colab runtime ends.

For the exact submitted snapshot, upload the included `UN.csv` before running. The notebook prints its SHA-256. The remote dataset may change, so the included snapshot is the reproducible reference. The saved narrative describes this snapshot and should be revisited if the data or methods are changed.

### Local Python

Use Python 3.12. From this repository folder:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python analysis.py
```

On Windows, activate with `.venv\Scripts\activate`. The requirements record the versions used for the submitted analysis. Colab normally supplies the core analysis packages; its versions may produce tiny numerical differences. `analysis.py` reproduces the calculations, charts and result tables. All of that code is also included directly in the notebook, which can run independently.

