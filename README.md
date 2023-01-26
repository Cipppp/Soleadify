# **Address Extraction**

The purpose of this code is to extract all the valid addresses from a list of company websites. The addresses will be extracted in the following format: country, region, city, postcode, road, and road numbers.

## **Requirements**

-   pyarrow
-   pandas
-   requests
-   BeautifulSoup4
-   re

## **Usage**

1. First, we need to read the snappy parquet file, for that we use pyarrow.parquet package.

2. We convert the parquet file to a pandas dataframe and extract the list of websites from the 'domain' column.

3. Then we iterate through each website and make a request using the requests library.

4. We parse the HTML using BeautifulSoup.

5. We search for all the span, p, and a elements on the page and use re to search for the postcode.

6. If postcode is found, we extract all the text inside the element using stripped_strings attribute and print it.

It's worth noting that this code is a rough example and may not work for all websites, as different websites may have different HTML structures and use different conventions for indicating address information. Also, the regular expressions used here are not complete and may not match all possible addresses. It will require a lot of testing and fine-tuning to extract the correct information and format it correctly.

## **Errors**

If any error occurs, it will print the error message.

# **Note**

You need to replace the path of the parquet file with the actual path of the file on your machine.
