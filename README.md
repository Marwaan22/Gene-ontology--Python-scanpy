# Gene-ontology--Python-scanpy

Script of GO analysis and  creating stress pathway index and visualization


Documentation of the script function 

•   	Import the required module, "genes_ncbi_mus_musculus_proteincoding," which contains a dictionary of mouse protein-coding gene IDs and their c         orresponding symbols.

•	    Download the Gene Ontology Basic OBO file and the NCBI Gene2Go annotation file, which are necessary for GO enrichment analysis.
•	    Create an instance of the GODag class, which represents the Gene Ontology hierarchy.
•	    Create a mapper that maps gene symbols to gene IDs.
•	    Read the Gene2Go file and store annotations in a list of named tuples.
•	    Get namespace2association where the namespace is BP (biological process), MF (molecular function), and CC (cellular component), and association is a dictionary where the key is the NCBI GeneID and the value is a set of GO IDs associated with that gene.
•	    Create an instance of the GOEnrichmentStudyNS class, which performs the GO enrichment analysis.
•	    Extract all the GO terms present in the Gene Ontology hierarchy.
•	    Define a function that takes a list of gene symbols, maps them to gene IDs, and performs GO enrichment analysis on them.
•	    Create a pandas DataFrame to store the GO enrichment results.
•	    Filter out GO terms with less than two genes.
•	    Create a new column in the DataFrame that calculates the percentage of genes in the study that are associated with each GO term.
•	    Merge the term and GO columns to create a new column that combines the term and GO information.
•	    Import the necessary visualization libraries, such as matplotlib and seaborn.
•	    Create a bar plot that shows the percentage of genes associated with each GO term, colored by the significance level of the enrichment analysis.
•	    Label the y-axis with wrapped text to improve readability.
•	defining a list of genes associated with a particular stress pathway, in this case, hypoxia. From GO stress pathways
•	    It then subsets the gene expression data in a provided dataset to only include the genes in the hypoxia gene list.
•	    Next, the script calculates the average expression of the genes in the subset for each sample in the dataset.
•	    It then adds this average expression as a new column in the dataset, with the name "hypoxia”
•	creates a violin plot of the stress index values for each sample, grouped by batch. 
![image](https://user-images.githubusercontent.com/127408032/224358241-90fdea0c-3b35-4190-90be-2dd881760d9f.png)
