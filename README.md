# SES6003-Programming-for-Sports-Perfromance
Victoria University SES6003

This is for Assessment 3 






colnames(Data_Clean) <- gsub("\\."," ", colnames(Data_Clean))

dataHM <- Data_Clean %>%
  filter(Team %in% c("Melbourne Vixens", "Queensland Firebirds", "Collingwood Magpies", "West Coast Fever", "GIANTS Netball", "Adelaide Thunderbirds", "NSW Swifts", "Sunshine Coast Lightning")) %>%
  arrange(Team)

heatmaply(Data_Clean,
          ncol (8), nrow(9),
               dendrogram = "none",
               xlab = "",
               ylab = "",
               main = "",
               scale = "collumn",
               margins = c(60,100,40,20),
               grid_color = "grey",
               grid_width = 0.00001,
               titleX = FALSE, 
                scale_fill_viridis(),
               hide_colorbar = TRUE,
               branches_lwd = 0.1,
               label_names = c("Athlete", "Team", "Output"),
               fontsize_row = 5, fontsize_col = 5,
               labCol = colnames(Data_Clean),
               labRow = rownames(Data_Clean),
               heatmap_layers = theme(axis.line = element_blank()))