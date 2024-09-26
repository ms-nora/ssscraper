#Profile Scraper -- ssscraper
 
This project is a Python-based web scraper designed by **ms-nora** to extract profile information from websites. 
 
It uses the `requests` library to fetch web pages, `BeautifulSoup` for parsing HTML, and `csv` for exporting data into a CSV file. 

The script filters profile-related links, scrapes the profiles, and organizes them based on the length of their profile information. 

#Features 
  - Scrapes profile links: Identifies and extracts URLs related to profiles or user information. 
  - Gathers profile data: Extracts key details such as profile name and profile information length from each page.
  - Categorizes profiles: Sorts and labels profiles based on the length of their information.
  - CSV Export: Saves all the scraped data into a CSV file with categories ('Best' and 'Not So Good').


#Requirements.

- Python 3.x 
- Requests library 
- BeautifulSoup4 library 
You can install the required packages with the following command: ```bash pip install requests beautifulsoup4 ```

#How to Use 

1. Clone this repository: ```bash git clone https://github.com/ms-nora/ssscraper.git cd ssscraper ```
2. Prepare a file named `liste_links.txt` containing the base URLs to scrape, with one URL per line.
3. Update the `proxies` variable in the `main()` function if you require proxy settings. 
4. Run the script: ```bash python scraper.py ``` 
5. The output will be saved in `CSV_Profile_links.csv`. 

#Script Overview 

  #Functions 
    - `load_urls(filename)`:  Loads URLs from a text file.
    - `is_profile_url(url)`:  Checks if a URL is related to a profile or user. 
    - `scrape_profile(url)`: Scrapes the profile name and profile information length from the URL.
    - `extract_profiles_from_site(base_url)`: Extracts and processes profile links from a website. 
    - `process_sites_and_save_to_csv(site_urls, csv_filename, proxies)`: Scrapes multiple websites and exports the 
    results to a CSV file. 
    
# Example If the input URL is a website containing profiles, the script will output a CSV like:

| Profile URL | Profile Name | Info Length | Category | |---------------------------|---------------|-------------|--------------| 
| http://example.com/profile | John Doe | 200 | Best | 
| http://example.com/user | Jane Smith | 120 | Not So Good | 


#License 
This project is open-source and available under the [MIT License](LICENSE). 
Authored by **ms-nora**.
