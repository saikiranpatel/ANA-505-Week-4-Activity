# ANA-505-Week-4-Activity
ANA 505 Week 4 Activity Assignment

#Week 4: dplyr package



df_haireyecolor <- data.frame(HairEyeColor)



head(df_haireyecolor,10)



install.packages("dplyr")
library(dplyr)



select(df_haireyecolor, Hair, Sex)



df_hairandsex <- select(df_haireyecolor, Hair = Hair, Sex = Sex)



df_hairandsex <- select(df_hairandsex, -Sex)



rename(df_haireyecolor, Gender = Sex)



df_haireyecolor[,"Gender"] <- NA
df_haireyecolor



df_male <- filter(df_haireyecolor, Sex == "Male")
df_male <- select(df_male, Sex)
df_male



group_by(df_haireyecolor, Sex)

#After you run it, write the total here:592

total=mutate(df_haireyecolor, total=cumsum(Freq))
total



df_female <- filter(df_haireyecolor, Sex == "Female")
df_female <- select(df_female, Sex)
df_female



bind_rows(df_male,df_female)


#Here we are using 'arrange' function to arrange a dataframe with 'Hair' Column

arrange_df_haireyecolor_by_Hair<- arrange(df_haireyecolor, desc(Hair))
arrange_df_haireyecolor_by_Hair

