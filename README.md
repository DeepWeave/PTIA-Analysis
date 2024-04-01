# PTIA-Analysis
Project to assess the impact of the Pretrial Integrity Act on Buncombe County Jail Stays

THis is the contents of .Rprofile

require(magrittr)
require(plyr)
require(dplyr)
require(reshape2)
require(scales)
require(ggplot2)
require(ggbreak)
require(GGally)
require(stringr)
require(readr)
require(digest)
require(Hmisc)
require(kableExtra)
require(openssl)
require(rmarkdown)
require(lubridate)
require(naniar)
require(qwraps2)
require(fitdistrplus)
require(cowplot)
require(zip)
require(santoku)
# RANSEED used in script 1_create_basic.Rmd:
RANSEED <- <enter your random seed value here as an integer>
RDataPath <- "R_Data/"
# this is the location of the csv files provided by E. Jackson and derived from the daily logs:
csvPath <- "../../BuncombeData/"
# date of jail file extraction:
FILE_DATE <- "2024-03-16"
PTIA_DATE <- "2023-10-01"
# date of the data to be compared with the PTIA data; it will have to change depending on FILE_DATE:
COMPARE_TO_DATE_START <- "2022-10-01"
COMPARE_TO_DATE_STOP <- "2023-03-15"
MAX_LEVELS <- list(1:14, 1:4, 5:14, 1:6)
GROUPS <- list("All", "Misdemeanor", "Felony", "1 to 6")
BUNCHES_DAYS <- list("Mon/Tue","Tue/Wed","Wed/Thu","Thu/Fri","Fri/Sat","Sat/Sun","Sun/Mon")
GROUP_TXT <- c("Week or less", "8 to 30 days", "31 to 90 days", "Over 90 days", "Ambig.")
OFFENSES <- c("violent", "drugs", "dwi", "theft")
CLASSES <- c("U", "M", "F", "L", "H")
