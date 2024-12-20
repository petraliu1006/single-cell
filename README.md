# Single-cell Annotation

## Python results
### 1. Cell Type Annotation (UMAP Plot)
#### The first UMAP plot (celltypist_cell_label_coarse) displays the clustering of cells with their coarse annotations. The dataset contains a variety of immune and stromal cell types. The key highlights include:

* Immune Cells: There is a substantial presence of T cells (e.g., Tcm/Naive cytotoxic T cells, Tcm/Naive helper T cells), NK cells (CD16+ and CD16-), B cells (B cells, Naive B cells, Small pre-B cells), and macrophage populations (e.g., Classical monocytes, Macrophages).
* Progenitors and Precursors: The dataset includes hematopoietic stem cells/multipotent progenitors (HSC/MPP) and various early erythroid and myeloid precursors (e.g., Early erythroid, Early lymphoid/T lymphoid, DC precursor).
* Specialized Cell Types: Several specialized immune cell populations are annotated, such as Type 17 helper T cells, ILC3, and Mast cells.
* Non-Immune Cells: The presence of epithelial cells and fibroblasts suggests that this dataset might include cells from tissue samples, not just peripheral blood.
* The diversity of cell types suggests a comprehensive sampling, possibly from a heterogeneous tissue environment.

### 2. Confidence Scores (UMAP Plot)
#### The second UMAP plot (celltypist_conf_score_coarse) visualizes the confidence score of the annotations, ranging from 0 to 1 (low to high). Key observations:

* High Confidence Annotations: The majority of cells appear to be annotated with high confidence (score close to 1), indicating reliable identification of cell types.
* Low Confidence Regions: There are some regions with lower confidence scores, which may indicate ambiguous or mixed populations. These could be transitional states or cells that are difficult to classify with the current reference dataset.

### 3. Hierarchical Clustering (Dendrogram)
#### The dendrogram reveals the hierarchical relationships between the annotated cell types:

* Major Lineages: The clustering reflects expected biological lineages. For example:
- Erythroid lineage (Early erythroid, Mid erythroid, Late erythroid) clusters together.
- T cells (Naive cytotoxic, Naive helper) are grouped, and closely related to NK cells.
- Monocyte-derived cells (Classical monocytes, Non-classical monocytes, Macrophages) form another related cluster.
- Distinct Cell Populations: Certain cell types like Mast cells and pDCs (plasmacytoid dendritic cells) appear as more distinct branches, reflecting their unique transcriptomic profiles.

### Overall Interpretation
The dataset appears to be well-annotated with diverse immune cell populations, along with some stromal and progenitor cells. The UMAP visualizations and dendrogram provide a coherent view of cellular diversity and relationships, suggesting that your annotation process was effective in capturing the main cell types and their respective lineages. However, the areas with lower confidence annotations might benefit from further refinement or additional reference datasets for improved classification.


## R results
### 1. UMAP Plot with SingleR Labels
#### The UMAP plot displays the clustering and annotation of cells into various cell types based on SingleR predictions.
* Observations:
* Cells are grouped into distinct clusters representing different cell types such as Astrocytes, T cells, Endothelial cells, and others.
Similar cell types, such as Pro-B cells, Pre-B cells, and B cells, are closely clustered, indicating shared transcriptomic profiles.
Diverse cell types like Epithelial cells, MSCs (Mesenchymal Stem Cells), and Hepatocytes are well-separated, suggesting strong transcriptional differences.
Insight: SingleR successfully labels cells using reference datasets. However, further validation (e.g., marker gene expression) can confirm the annotation accuracy.
### 2. Heatmap of Annotation Scores
#### The heatmap visualizes the confidence scores for cell type assignments across cells, with yellow indicating higher confidence and blue/purple indicating lower scores.
* Observations:
* High confidence in assignments for distinct cell types like Epithelial cells, Fibroblasts, and Astrocytes suggests robust annotations.
Some overlap or lower scores for closely related cell types (e.g., Pre-B cells and Pro-B cells) may indicate shared gene expression profiles or ambiguous annotations.
Insight: High-confidence clusters highlight well-defined cell types, while lower scores might indicate potential misclassification or intermediate cell states.
