# Improving categorization on Craigslist
  1. Introduction
  2. Objective
  3. Methodology
  4. Data Sources
  5. Data Dictionary
  6. Data Pre-processing
  7. Feature Engineering
  8. Model Development
  9. Result

# Introduction
  1. Craiglist is a classified advertisement site with sections for community, housing, jobs, sales, and services.
  2. Often there is misclassification of products across sections, especially in the Computers category.
  3. This can lead to a discourgaing user experience and engagement on the website.
  4. There lies an opporunity for enhancing customer satisfaction and business performance.
  5. Solving the issue by employing advanced modeling techniques to quickly identify and accurately recategorize misclassified products, improving browsing experience.

# Objective
 1. Even though Craiglist is one of the biggest adverstising website, there are potential problems faced by users. One such problem is to find appropriate product on the computer section. Certain product that should be under computer parts section are present     under the computer section.
 2. The motivation is to use the unstructured data and recategorize the product into pre-defined existing categories.

# Methodology
 1. Scrap the exisitng product on the website using BeautifulSoup and Selenium.
 2. Assign tag to each of the product as either a computer or not-a-computer.
 3. Cleaning and pre-processing of the data to make it usable for modelling.
 4. Modelling
 5. Analysis

# Data Sources
 1. The Data has been scraped from existing computer section on the Craiglist Website.
 2. This was done for 2 cities (San Francisco and Chicago).
 3. Dataset: 3 columns and 2143 rows.
