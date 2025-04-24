# Load libraries
library(dplyr)
library(ggplot2)

# Read the CSV file
covid_df <- read.csv("data/03-09-2023.csv")

# Check structure (optional)
str(covid_df)

# Plot Top 10 States by Confirmed Cases
top_confirmed <- covid_df %>%
  arrange(desc(Confirmed)) %>%
  slice(1:10)

ggplot(top_confirmed, aes(x = reorder(Province_State, Confirmed), y = Confirmed)) +
  geom_bar(stat = "identity", fill = "steelblue") +
  coord_flip() +
  labs(
    title = "Top 10 U.S. States by COVID-19 Confirmed Cases",
    x = "State",
    y = "Total Confirmed Cases"
  ) +
  theme_minimal()

ggsave("plots/top_10_confirmed.png", width = 8, height = 6)

# Plot Top 10 States by Deaths
top_deaths <- covid_df %>%
  arrange(desc(Deaths)) %>%
  slice(1:10)

ggplot(top_deaths, aes(x = reorder(Province_State, Deaths), y = Deaths)) +
  geom_bar(stat = "identity", fill = "firebrick") +
  coord_flip() +
  labs(
    title = "Top 10 U.S. States by COVID-19 Deaths",
    x = "State",
    y = "Total Deaths"
  ) +
  theme_minimal()

ggsave("plots/top_10_deaths.png", width = 8, height = 6)

# Optional: Plot Recovered if available
if ("Recovered" %in% colnames(covid_df)) {
  top_recovered <- covid_df %>%
    arrange(desc(Recovered)) %>%
    slice(1:10)
  
  ggplot(top_recovered, aes(x = reorder(Province_State, Recovered), y = Recovered)) +
    geom_bar(stat = "identity", fill = "forestgreen") +
    coord_flip() +
    labs(
      title = "Top 10 U.S. States by COVID-19 Recoveries",
      x = "State",
      y = "Total Recovered"
    ) +
    theme_minimal()
  
  ggsave("plots/top_10_recovered.png", width = 8, height = 6)
}

# Print full data summary
cat("COVID-19 State Summary:\n")
print(covid_df)
