# assignment8


library(tidyverse)

**Question 1.1**

mass = a \* length ^ b a \<- .73 b \<- 3.63

dinosaur_lengths \<- c(25.31, 16.7, 25.22, 24.08, 13.85, 24.57, 18.61,
17.79, 26.31, 15.02, 13.42, 16.4, 22.75, 23.68, 21.93, 17.33, 14.74,
21.52, 30.51, 10.98, 20.2, 16.1, 19.1, 13.65, 14.23, 26.76, 25.51,
26.03, 24.89, 18.49, 18.93, 25.46, 23.54, 11.81, 10.66, 30.36, 14.2,
21.34, 21.3, 23.46, 20.77, 17.27, 31, 17.66, 26.02, 16.02, 15.1, 26.05,
22.6, 23.22, 10.35, 21.14, 17.91, 15.35, 13.91, 26.17, 24.89, 16.86,
22.11, 27.07, 14.31, 12.02, 9.82, 19.85, 28.61, 22.57, 13.43, 10.41,
23.26, 22.65, 18.91, 26.58, 12.71, 9.34, 23.97, 22.89, 24.71, 10.73,
20.88, 18.67, 13.26, 16.38, 21.24, 13.39, 21.2, 21.36, 16.49, 26.13,
20.04, 18.9, 16.71, 24.74, 19.98, 18.05, 12.95, 22.64, 16.03, 11.21,
22.48, 20.48, 25.76, 12.01, 17.86, 17.12, 25.34, 22.18, 20.95, 21.17,
14.52, 20.82, 17.87, 27.45, 29.99, 31.3, 24.68, 22.55, 18.13, 18.97,
23.3, 18.66, 19.9, 25.52, 19.89, 24.7, 18.25, 24.53, 23.47, 16.26,
15.08, 19.67, 24.12, 26.03, 29.29, 16.65, 21.55, 22.44, 17.65, 24.67,
23.38, 18.18, 20.5, 25.62, 18.99, 13.3, 16.55, 29.76, 13.74, 25.04,
19.42, 26.29, 10.71, 22.19, 20.03, 23.14, 14.28, 18.93, 27.57, 16.3,
16.05, 23.26, 25.09, 16.97, 22.75, 16.62, 28.7, 20.82, 26.79, 20.75,
28.74, 19.59, 22.94, 24.51, 18.09, 16.91, 16.53, 20.89, 29.85, 12.89,
21.01, 19.41, 23.43, 21.13, 24.58, 23.22, 11.93, 22.36, 22.04, 27.25,
24.24, 11.39, 22.62, 24.38, 21.95, 17, 30.64, 29.53, 25.13, 20.21,
17.51, 26.25)

a_values \<- c(0.61, 0.74, 0.82, 0.78, 0.85, 0.72, 0.84, 0.65, 0.58,
0.82, 0.78, 0.8, 0.69, 0.65, 0.75, 0.72, 0.7, 0.7, 0.65, 0.77, 0.67,
0.86, 0.63, 0.6, 0.67, 0.57, 0.63, 0.72, 0.78, 0.91, 0.67, 0.81, 0.73,
0.8, 0.54, 0.77, 0.86, 0.81, 0.9, 0.68, 0.58, 0.8, 0.72, 0.67, 0.84,
0.63, 0.82, 0.61, 0.74, 0.83, 0.88, 0.66, 0.8, 0.72, 0.75, 0.58, 0.78,
0.76, 0.76, 0.77, 0.91, 0.57, 0.73, 0.87, 0.78, 0.72, 0.73, 0.89, 0.52,
0.87, 0.7, 0.67, 0.7, 0.81, 0.75, 0.7, 0.79, 0.83, 0.57, 0.88, 0.79,
0.77, 0.83, 0.69, 0.69, 0.91, 0.86, 0.66, 0.67, 0.88, 0.78, 0.82, 0.72,
0.86, 0.8, 0.69, 0.7, 0.68, 0.71, 0.83, 0.8, 0.64, 0.68, 0.51, 0.78,
0.8, 0.71, 0.73, 0.88, 0.83, 0.76, 0.95, 0.84, 0.75, 0.85, 0.79, 0.64,
0.94, 0.83, 0.64, 0.83, 0.8, 0.62, 0.79, 0.72, 0.8, 0.63, 0.79, 0.88,
0.64, 0.77, 0.85, 0.93, 0.85, 0.9, 0.83, 0.88, 0.95, 0.64, 0.78, 0.82,
0.77, 0.53, 0.96, 0.78, 0.66, 0.76, 0.69, 0.74, 0.64, 0.79, 1.05, 0.59,
0.82, 0.73, 0.64, 0.8, 0.86, 0.95, 0.95, 0.64, 0.87, 0.75, 0.59, 0.73,
0.7, 0.7, 0.8, 0.79, 0.75, 0.76, 0.64, 0.77, 0.64, 0.78, 0.75, 0.85,
0.75, 0.87, 0.72, 0.7, 0.62, 0.64, 0.79, 0.63, 0.71, 0.79, 0.66, 0.86,
0.93, 0.39, 0.62, 0.73, 0.7, 0.69, 0.7, 0.72, 0.81, 0.77, 0.57)

b_values \<- c(3.63, 3.57, 3.51, 3.5, 3.65, 3.64, 3.6, 3.59, 3.58, 3.61,
3.55, 3.61, 3.57, 3.61, 3.62, 3.62, 3.57, 3.6, 3.56, 3.59, 3.63, 3.61,
3.59, 3.66, 3.54, 3.59, 3.56, 3.65, 3.58, 3.6, 3.66, 3.58, 3.64, 3.62,
3.59, 3.65, 3.56, 3.64, 3.6, 3.52, 3.56, 3.63, 3.59, 3.63, 3.68, 3.65,
3.47, 3.49, 3.64, 3.65, 3.64, 3.6, 3.61, 3.66, 3.62, 3.6, 3.67, 3.62,
3.65, 3.57, 3.53, 3.55, 3.66, 3.51, 3.51, 3.64, 3.62, 3.65, 3.59, 3.68,
3.51, 3.63, 3.59, 3.56, 3.57, 3.66, 3.56, 3.63, 3.61, 3.62, 3.7, 3.63,
3.57, 3.58, 3.6, 3.57, 3.58, 3.58, 3.55, 3.49, 3.71, 3.56, 3.6, 3.59,
3.56, 3.65, 3.65, 3.65, 3.58, 3.57, 3.57, 3.57, 3.52, 3.53, 3.75, 3.68,
3.56, 3.71, 3.57, 3.58, 3.58, 3.57, 3.64, 3.56, 3.63, 3.53, 3.6, 3.7,
3.64, 3.62, 3.59, 3.59, 3.57, 3.58, 3.56, 3.61, 3.6, 3.59, 3.63, 3.63,
3.61, 3.62, 3.59, 3.49, 3.53, 3.58, 3.66, 3.59, 3.69, 3.65, 3.59, 3.67,
3.59, 3.64, 3.61, 3.53, 3.54, 3.49, 3.68, 3.63, 3.64, 3.62, 3.7, 3.69,
3.59, 3.58, 3.61, 3.56, 3.72, 3.58, 3.64, 3.57, 3.72, 3.6, 3.49, 3.63,
3.55, 3.58, 3.62, 3.63, 3.65, 3.57, 3.7, 3.59, 3.64, 3.59, 3.69, 3.5,
3.6, 3.61, 3.56, 3.64, 3.58, 3.62, 3.63, 3.56, 3.66, 3.63, 3.49, 3.54,
3.73, 3.61, 3.47, 3.53, 3.68, 3.63, 3.63, 3.59, 3.52, 3.62)

**1.1**

``` r
.73 * 16 ^ 3.63
```

**1.2**

using vectorization

``` r
massv <- a_values * dinosaur_lengths ^ b_values

massv
```

using a for loop

``` r
massf <- NULL

for (i in 1:length(a_values)) {
massf <- c(massf, a_values[i] * dinosaur_lengths[i] ^ b_values[i])

}

massf
```

**1.3**

using vectorization

``` r
system.time(massv <- a_values * dinosaur_lengths ^ b_values)

massv
```

user system elapsed 0 0 0

using a for loop

``` r
massf <- NULL

system.time(for (i in 1:length(a_values)) {
massf <- c(massf, a_values[i] * dinosaur_lengths[i] ^ b_values[i])

})
```

user system elapsed 0.00 0.00 0.02

**Exercise 2**

**2.1**

What parts of your code are consistent across every line/code chunk?
-for each line of code, the defining text bouy\_ stays the same, most of
the github data link (except for the year) stays the same, and the na =
argument remains the same.

What parts are different? - for each line of code, the year in the
bouy\_ name and the year in the github link changes.

**2.2**

``` r
  start <- 1987
end <- 1992
for (i in start:end){
  path <- str_c('https://raw.githubusercontent.com/nt246/NTRES-6100-data-science/master/datasets/buoydata/44013_', i, '.csv')
  print(path)
}
```

**2.3**

``` r
start <- 1987
end <- 1992
df_combined <- NULL
for (i in start:end){
  path <- str_c("https://raw.githubusercontent.com/nt246/NTRES-6100-data-science/master/datasets/buoydata/44013_", i, ".csv")
  df <- read_csv(path)
  df_combined <- bind_rows(df_combined, df)
}

dim(df_combined)
```

**2.4**

``` r
start <- 1987
end <- 1992
df_summary_combined <- NULL
for (i in start:end){
  path <- str_c("https://raw.githubusercontent.com/nt246/NTRES-6100-data-science/master/datasets/buoydata/44013_", i, ".csv")
  df <- read_csv(path) %>%
    select(YY, MM, WVHT, WTMP) %>%
    rename(Year = YY, Month = MM, Wave_Height = WVHT, Water_Temperature = WTMP) %>%
    group_by(Year, Month) %>%
    summarize(Avg_Wave_Height = mean(Wave_Height, na.rm = TRUE),
              Avg_Water_Temperature = mean(Water_Temperature, na.rm = TRUE))
  
  df_summary_combined <- bind_rows(df_summary_combined, df)
}
```

data plot

``` r
ggplot(df_summary_combined, aes(x = as.Date(paste(Year, Month, "15", sep = "-")), 
   y = Avg_Wave_Height)) +
  geom_line(color = "blue") +
  labs(title = "Monthly Averaged Wave Heights (1987-1992)",
       x = "Date",
       y = "Average Wave Height (m)") +
  theme_minimal()
  
ggplot(df_summary_combined, aes(x = as.Date(paste(Year, Month, "15", sep = "-")), 
   y = Avg_Water_Temperature)) +
  geom_line(color = "blue") +
  labs(title = "Monthly Averaged Wave Heights (1987-1992)",
       x = "Date",
       y = "Average Water temperature (m)") +
  theme_minimal()
```

![](problem_sets/Assignment%208/a1e0f841-13e1-4223-9a9f-4d05f25bb0bb.png)

![](problem_sets/Assignment%208/e9f2326a-4034-4098-8562-a899994584bb.png)

Note: I didn’t make these blue, copilot did, lol

Note 2: I have tried debugging the outliers. I have manually re imported
the data, and it seems that the outliers are being caused by genuine
outliers… When I imported the buoy_1989 data with the argument na =
c(“0”, “0”, “0”, “0”) the outliers didnt go away, so im making the
assumption they are genuine data points, or at least that I don’t know
why they exist. but I did manually look, so i don’t think its a
hallucination?
