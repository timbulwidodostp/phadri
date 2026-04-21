# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Hadri panel stationarity test Use phadri (punitroots) With (In) R Software
install.packages("remotes")
remotes::install_github("rforge/punitroots/pkg")
library("punitroots")
# Estimation Hadri panel stationarity test Use phadri (punitroots) With (In) R Software
phadri = read.csv("https://raw.githubusercontent.com/timbulwidodostp/phadri/main/phadri/phadri.csv",sep = ";")
phadri_data = cbind(phadri$CAN, phadri$FRA, phadri$GBR, phadri$GER, phadri$ITA, phadri$JPN)
phadri <- phadri(phadri_data, exo = "intercept", bw = 2, adjust = FALSE)
phadri_1 <- phadri(phadri_data, exo = "trend", bw = 2, adjust = FALSE)
phadri_2 <- phadri(phadri_data, exo = "intercept", bw = 2, adjust = TRUE)
phadri_3 <- phadri(phadri_data, exo = "trend", bw = 2, adjust = TRUE)
phadri
phadri_1
phadri_2
phadri_3
# Hadri panel stationarity test Use phadri (punitroots) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished