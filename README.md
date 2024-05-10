# Sensitivity-Analysis-Code


# Install and load the 'poLCA' package
install.packages("poLCA")
library(poLCA)

#Read the dataset
data <- read.csv("police_perception_cleaned.csv")

#Specify the formula for LCA

formula <- cbind(inter1, inter2, inter3,inter4,inter5, inter6, inter7, 
inter8, inter9, inter10, inter11, inter12) ~ 1

#Perform LCA
lca_model <- poLCA(formula, data= data, nclass =4) 
#We tried nclass= 
#2,3,4,5,6

#View the LCA results
summary(lca_model)
