# hackbio-cancer-internship
# R Shiny: A Basic Introduction
## Authors (@slack): Nourhan Elhifnawy (@Hifnawy). ##

# About R Shiny: 

R Shiny is a widely used package for the R programming language. Shiny is an open-source R package that offers an attractive and robust web framework for developing web applications using (Miller & Shalhout, 2022). With Shiny, users can easily transform their studies into dynamic web apps without knowing any HTML, CSS, or JavaScript. In the life sciences, R shiny is very popular. Shiny can be utilized to make visually attractive dashboards. Turning an analytical pipeline into an interactive web application becomes simple with Shiny (Wickham, 2021). With strong roots in software engineering, it is made up of generic building blocks. R Shiny makes use of R's data analysis and visualization features to provide visually appealing user interfaces. (Wickham, 2021). The two primary parts of shiny applications are the user interface (UI) function and the server function. UI function specifies the visual design and elements of the user interface. While the server function manages the calculations and logic underlying your application. Through the communication between the two services, users can interactively examine data and obtain real-time insights. Moreover, R Shiny is compatible with other R packages, including dplyr for data manipulation and ggplot2 for data display (Moraga, 2019). 

# R shiny importance in the Cancer field: “DeepDR Model”

Determining novel therapeutic agents and creating medications require an understanding of the ability to predict correlations between cancer genomes and the reaction of cancer cells to anti-cancer therapies. Global consortia have utilized sequencing tools and drug-screening approaches to analyze the genetics of numerous pan-cancer cell lines and tumors (Wang et al., 2024). For example, consider the developed DeepDR. DeepDR is a simple implementation model mostly used to predict anti-cancer medication sensitivity. The model predicts a cancer sample's reaction to every drug in the GDSC library by integrating the gene mutation and expression patterns of the sample (Wang et al., 2024).  With the use of shinyDeepDR, users can input gene expression and/or mutation data from a cancer sample and accomplish two primary tasks, such as determining the drug and the sample (Wang et al., 2024). In conclusion, shinyDeepDR is a free-to-use web tool for in silico anti-cancer drug screening.

# Conclusion:

In conclusion, R Shiny is an effective tool for developing interactive web apps using the programming language R. Its configurable UI features, reactive programming methodology, and association with other R packages make it an excellent option for data scientists to produce visually stimulating and educational visualizations.



# References:
Miller, D. M., & Shalhout, S. Z. (2022). BodyMapR: An R package and Shiny application designed to generate anatomical visualizations of cancer lesions. JAMIA Open, 5(1), ooac013. https://doi.org/10.1093/jamiaopen/ooac013

Moraga, P. (2019). Introduction to shiny. Geospatial Health Data, 203–215. https://doi.org/10.1201/9780429341823-13

Wang, L.-J., Ning, M., Nayak, T., Kasper, M. J., Monga, S. P., Huang, Y., Chen, Y., & Chiu, Y.-C. (2024). shinyDeepDR: A user-friendly R Shiny app for predicting anti-cancer drug response using deep learning. Patterns, 5(2). https://doi.org/10.1016/j.patter.2023.100894

Wickham, H. (2021). Mastering shiny: Build interactive apps, reports, and dashboards powered by R (2nd ed.). O’Reilly Media, Inc. 






