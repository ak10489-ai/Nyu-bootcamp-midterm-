# Nyu-bootcamp-midterm-
midterm project for data bootcamp 


For my midterm project, I decided to open an Aritzia store in Paris. To do that, I compared it to two French brands: Sézane and Maje. These brands are quite popular and have a similar price point. Maje represents the premium line at Aritzia, while Sézane is closer to the regular line. I focused on three main categories: dresses, coats, and tops.

At first, I wanted to do web scraping, but each website had anti-scraping protection, which made it impossible to extract data directly. So instead, I used SerpAPI, which is a Google Search API that allows structured access to Google search results using Python (SerpApi, 2025). The downside is that I don’t have access to all the data that’s available on the brand websites. For example, when I wanted to find the total number of products for each category, I could only retrieve what was indexed on Google meaning I only got data for what appears on each results page.

Because of that barrier, I created separate code for each brand and category, since using Google Search instead of direct web scraping caused differences in how much data I could get, especially because I used French searches for Sézane and Maje and U.S. searches for Aritzia.

Once I extracted the data, I created two data frames: one for the French brands, since their data was in euros and French, and one for Aritzia, which was in English and U.S. dollars. I separated them because converting the currencies in Python caused complications with data formatting.

After that, I calculated the average price per category for each dataset and visualized it using a bar plot with the Python libraries matplotlib and pandas. Since Aritzia will likely pay exportation fees when selling in France, I assumed 1 USD = 1 EUR for this analysis to simplify comparisons. I compared it to other Us Brands in Europe such as On running which has the same prices in Dollars and Euro

Inventory and Category Comparison
For inventory, I used the same SerpAPI approach to count how many product listings appeared per category. While this doesn’t represent the exact number of items sold, it works as a good proxy for brand visibility online. I plotted the data using matplotlib.pyplot to show how many dresses, coats, and tops each brand had available (SerpApi, 2025).

The bar plot helped show how Aritzia’s online offering compares to the French brands. Even though I didn’t have direct access to each brand’s inventory, this method still gave a good visual comparison of the range of available products.

Popularity and Age Demographics
To analyze brand popularity, I used PyTrends, which is an unofficial Python interface for the Google Trends API (Python Software Foundation, 2025). This allowed me to track how often each brand was searched on Google over the past year. I focused on searches in France for Sézane and Maje, and the United States for Aritzia.

Next, I wanted to see if age affects popularity. For example, on social media platforms like TikTok and Instagram, Aritzia is very popular with younger audiences, mostly Gen Z. Since Google Trends doesn’t provide age data, I simulated brand popularity by age using approximate values based on social media partnerships and influencer demographics. This simulation was created in Python and integrated into the same dataset, showing that Aritzia appeals strongly to the 18–35 age range, while Maje and Sézane have broader appeal among 25–45-year-olds.

Price–Popularity Correlation
To check if price impacts popularity, I calculated the correlation coefficient between product prices and popularity for each dataset using Python’s pandas.corr() function.

For Aritzia, the correlation was r = 0.98, showing a very strong positive relationship that means that higher-priced items tend to be more popular. This reflects how the U.S. market associates higher price with quality and exclusivity.

For Maje and Sézane, the correlation was r = 0.46, showing a moderate positive correlation, which means that in France, higher prices slightly increase popularity but aren’t the main factor. This supports the idea that French consumers value quality and craftsmanship more than price alone (Python Software Foundation, 2025). This findings are the first I did not know that google trends cannot be run multiple times which is why there is the error message but it works now the results are r=1 and r=0.36 which is not that different. 

Location Analysis
For location selection, I looked at three major Paris areas that fit Aritzia’s image and customer base: Champs-Élysées, Le Marais, and Opéra (near Galeries Lafayette). I used the Google Maps Places API to search for Sézane and Maje store locations within a 1 km radius of each area’s coordinates (Google LLC, 2025).

The API provided structured data on nearby stores, which I stored in a pandas dataframe and then visualized with Folium, a Python library that integrates with Leaflet.js to create interactive maps (Folium, 2025). I generated a heat map to visualize store density in each district. The results showed that Champs-Élysées had fewer competitors compared to Le Marais and Opéra, making it a strong candidate for Aritzia’s first Paris flagship.

Findings and Recommendations
From my data, I observed that there is an opening for Aritzia in Paris. The biggest competitor would be Sézane, more than Maje.


Aritzia should not increase its prices too much, I think they should stay close to the U.S. price range or only slightly higher, but not as high as Maje’s. In terms of products, coats would be a smart focus since competitors have fewer options in that category.

Aritzia should target younger consumers (18–35) who are already familiar with the brand through social media. It’s also important to remember that the French market values quality over price, and price doesn’t directly impact popularity as much as it does in the U.S.

Finally, I recommend that Aritzia open its first store on the Champs-Élysées, since it’s a central and iconic area with less competition, high visibility, and great potential to attract both locals and tourists.

References (APA 7th Edition)
Folium. (2025). Folium: Python data, Leaflet.js, and interactive maps [Computer software]. Retrieved from https://python-visualization.github.io/folium/

Google LLC. (2025). Google Maps Platform: Places API. Retrieved from https://developers.google.com/maps/documentation/places

Google LLC. (2025). Google Trends. Retrieved from https://trends.google.com/trends/

Python Software Foundation. (2025). PyTrends: Google Trends API for Python [Computer software]. Retrieved from https://github.com/GeneralMills/pytrends

SerpApi. (2025). Google Search API documentation. Retrieved from https://serpapi.com
