![][image1]

**The Gene Pathway Analysis Dashboard**

HackBio internship 2024\_Stage 4

![][image2]

**Welcome to the Gene Pathway Analysis Dashboard\!**

**Contributors:** Nourhan Elhifnawy (@Hifnawy), Hana Mazroua (@Mazroua).

Dashboard on Shiny: https://labd.shinyapps.io/Gene/

**Introduction:**

The provided R code establishes a Shiny application for functional enrichment analysis and KEGG pathway visualization based on a list of genes. With the help of Shiny, ggplot2, TCGAbiolinks, KEGGREST, and SummarizedExperiment, the application provides an intuitive user interface for investigating biological processes related to genes, cellular elements, molecular activities, and related pathways.

**Explanation:**

The first section loads the necessary libraries. The “Shiny” library is mainly for creating dynamic websites. The “ggplot2” makes data visualizations that are aesthetically pleasing. The “TCGAbiolinks” provides TCGA data access and analysis. Also, “KEGGREST” is for interfacing with the KEGG pathway database, and the “SummarizedExperiment” is for managing structured gene expression data.

The “parse\_enrichment\_results” In order to extract useful information from the results of enrichment analyses, this function is essential. It carries out the following duties:

1. **Input validation:** which prevents errors by determining whether the input result is null or empty.  
2. **Data Parsing:** Uses regular expressions to extract GO keywords and FDR values from the outcome texts.  
3.  **Data Filtering:** Eliminates entries that have non-positive or missing FDR values.  
4.  **Data Sorting:** To make understanding easier, the findings are sorted by ascending FDR.

**For the User Interface (UI)**: 

The user interface (UI) component specifies the user interface and layout of the program. It is comprised of the Gene Pathway Analysis Tab, which includes "Sidebar," which allows users to input genes as text or by uploading a CSV file; the Main Panel, which displays analysis results including plots and textual interpretations; and the Navigation Bar, which offers a clear structure with tabs for different sections. The Home Tab greets users and explains the app's functionality. User interactions, data processing, and result generation are handled by the server logic. 

**Key steps:**

• **Gene List Handling:** This function pulls the gene list from a file uploaded or input by the user.  
• **Enrichment Analysis:** For biological processes, cellular components, and molecular activities, enrichment analysis is carried out using TCGAanalyze\_EAcomplete.  
• **KEGG Pathway Analysis:** A method for determining KEGG pathways connected to input genes.  
• **Processing of the Results:** Takes pertinent data out of the enrichment results and puts it in reactive values.  
• **Visualization and textual Interpretation:** to elucidate the stories and their relevance.

**The application offers several advantages**:

In conclusion, the analysis process becomes easier and accessible to people with different degrees of technical expertise due to this Shiny-based interface. It offers information on molecular functions, cellular components, biological processes, and KEGG pathways connected to the input genes. Moreover, the program makes use of TCGA data to offer insightful information on biological processes connected to genes.

[image1]: <data:image/png;base64,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>

[image2]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAFAAAAAyCAYAAADLLVz8AAAD+0lEQVR4Xu2ay2vWQBTFi4LiE12IK3FTEKGCoCCISxeioH+AiGu7FATdVbFuBIsvirVa7MuqWC22+gniQqwbS+kb3EjBWrAoigq+0XOlKem5SZpkJpkssvhBe2bunXvPTJp8+VrV+Wj8r9DaO7Z7497GqjS0941133gwOunliqLj4fgujrdFW9/YIV4vhGmpmePjgviDXi75hZN7jc6AeqGrMrEHC9aCCs9LC3Id4MLSgs3fz/nTgJp+YhPOI98+6dnrn+f5CTUwD0xOvQdOfjXnzROnBgrY8T9sSlywAV85X95U4Yi+Z9EFbM5CIOYa53DAlFwCKwMGcgen6TCbFEZD+8slHO8C8c7bTTXoAjYqDLnsOdYFUstcUbgDfeQJtsGfi2E0XyPrXe0eqpbf/ePY0Vo2i0HMFn8MTu442CRjNysTmzE+wOvaBj3MePXMK44n2gANHWMTGBTU783nMcabhw1/ymMM5hzlemzgX2Pegs33htfw5LTgNG3ghqKAiXUSJ8+aPOaBsUsyB5tSx2NRSC1cX1paekZW+3OrxYQjZx4vRpFfODgKzL/IeZKCHP//jKDhHTyGy3Tb7Dpzl09asBEnuf4o5EmFc3gogRbajpPxlhP6Ep+TU8txJni54+om4G6+HD2e5b48sGmvsZlbOc6PElzTOft8F6DLhtWz7holFAE+CVmcPlsooQiwcaWBCWHjSgMTwsaVBiZA7oxsXGlgAvBY8ZuN85Axnu8aJbgEBjWxaQweZa5znEuU4AqYs5PNCqMjw+9VkqIEF+DkXWGTFgImNnAeFyghT+SGgY+Kv9icuEisvFzlvHmihDw43fxiBZthimwGr5MHSsganJo33LwtcFl/4PWyRglZgganuGnbYIPe8bpZooQsaLwzuIobzRpc0lZfs4WhBNtwY3nD9dhGCbaQt9rcjCtQzyKuzxZKsEFLz8g6bsI1qGkp12kDJdiAiy8KXKcNlGBKV2WihgsvCk3dQ4m+KYyDEkyRZzEuvCjgI+Mo12uKEkzhoosG12uKEkzhgsMI+rqQ54TBcUleRnCsKUowhQv209o79oPnx431w3GU4zvPjxubBiWYwgUL8ib52v3h9TyX4bgg8FFtkuMYeQYN+8zNc01Rgik4ZZ+8YvHzZx6PgpsNIo6BfnBTu+2Ln+ZxU5RgA5y4E6zFgc0KIqmBwqmm/mUw8jjrNlCCS9isINIYmCVKcAmbFURpYARsVhClgRGwWUGUBkaAu/Y3NowpDYxAzGHDGNxNBzjOJUpwCQx6zoYxeER6xnEuUYJLcLra2DAGl/kFjnOJElxy98mrBb8vvnxrcC3HuUQJrmHDGJ7vGiUUgbB/9+B5ReAfB+C1hdor6T4AAAAASUVORK5CYII=>