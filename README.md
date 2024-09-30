# ChangepointDetection FeatureImportance
## Random Forest Regression
The dataset $(X, y_{\text{low}}, y_{\text{up}})$ is split into two subsets: $(X, y_{\text{low}})$ and $(X, y_{\text{up}})$. Before training, all rows containing infinity values in either $y_{\text{low}}$ or $y_{\text{up}}$ are removed.

We then proceed as follows:
1. Train separate Random Forest models for $(X, y_{\text{low}})$ and $(X, y_{\text{up}})$.
2. Compute feature importance for both models.
3. Calculate the final feature importance by averaging the importances from the Random Forest models for $y_{\text{low}}$ and $y_{\text{up}}$.

![Feature Importance](figs/RF_Regression/ATAC_JV_adipose.png)
![Feature Importance](figs/RF_Regression/CTCF_TDH_ENCODE.png)
![Feature Importance](figs/RF_Regression/detailed.png)
![Feature Importance](figs/RF_Regression/H3K27ac-H3K4me3_TDHAM_BP.png)
![Feature Importance](figs/RF_Regression/H3K27ac_TDH_some.png)
![Feature Importance](figs/RF_Regression/H3K27me3_RL_cancer.png)
![Feature Importance](figs/RF_Regression/H3K27me3_TDH_some.png)
![Feature Importance](figs/RF_Regression/H3K36me3_AM_immune.png)
![Feature Importance](figs/RF_Regression/H3K36me3_TDH_ENCODE.png)
![Feature Importance](figs/RF_Regression/H3K36me3_TDH_immune.png)
![Feature Importance](figs/RF_Regression/H3K36me3_TDH_other.png)
![Feature Importance](figs/RF_Regression/H3K4me1_TDH_BP.png)
![Feature Importance](figs/RF_Regression/H3K4me3_PGP_immune.png)
![Feature Importance](figs/RF_Regression/H3K4me3_TDH_ENCODE.png)
![Feature Importance](figs/RF_Regression/H3K4me3_XJ_immune.png)
![Feature Importance](figs/RF_Regression/H3K9me3_TDH_BP.png)
![Feature Importance](figs/RF_Regression/systematic.png)

## Random Forest Classification
The dataset `(X, y_low, y_up)` is divided into two classes: `(X, y_low)` and `(X, y_up)`. Prior to training, any rows that contain infinity values in either `y_low` or `y_up` are removed.

The following steps are taken:
1. Train Random Forest classifiers separately on `(X, y_low)` and `(X, y_up)`.
2. Disregard the feature importance from `y_low` and `y_up` since they are not technically features in interval regression.

![Feature Importance](figs/RF_Classification/ATAC_JV_adipose.png)
![Feature Importance](figs/RF_Classification/CTCF_TDH_ENCODE.png)
![Feature Importance](figs/RF_Classification/detailed.png)
![Feature Importance](figs/RF_Classification/H3K27ac-H3K4me3_TDHAM_BP.png)
![Feature Importance](figs/RF_Classification/H3K27ac_TDH_some.png)
![Feature Importance](figs/RF_Classification/H3K27me3_RL_cancer.png)
![Feature Importance](figs/RF_Classification/H3K27me3_TDH_some.png)
![Feature Importance](figs/RF_Classification/H3K36me3_AM_immune.png)
![Feature Importance](figs/RF_Classification/H3K36me3_TDH_ENCODE.png)
![Feature Importance](figs/RF_Classification/H3K36me3_TDH_immune.png)
![Feature Importance](figs/RF_Classification/H3K36me3_TDH_other.png)
![Feature Importance](figs/RF_Classification/H3K4me1_TDH_BP.png)
![Feature Importance](figs/RF_Classification/H3K4me3_PGP_immune.png)
![Feature Importance](figs/RF_Classification/H3K4me3_TDH_ENCODE.png)
![Feature Importance](figs/RF_Classification/H3K4me3_XJ_immune.png)
![Feature Importance](figs/RF_Classification/H3K9me3_TDH_BP.png)
![Feature Importance](figs/RF_Classification/systematic.png)
