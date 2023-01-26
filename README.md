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

## **Note**

You need to replace the path of the parquet file with the actual path of the file on your machine.

## **The reasoning behind it**

The task at hand is to extract valid addresses from a list of company websites. The addresses must be in the format of country, region, city, postcode, road, and road numbers.

The first step in solving this problem is to understand the structure of the data. In this case, we are given a list of company websites in a snappy parquet file format. The websites are stored in a column called 'domain'. We will read the file using the pyarrow.parquet package and convert it to a pandas dataframe. Then we will extract the list of websites from the 'domain' column.

Once we have the list of websites, we need to iterate through each website and make a request using the requests library. We will parse the HTML of the website using BeautifulSoup. We will then search for all the span, p, and a elements on the page.

The next step is to search for the postcode. We will use the re library to search for the postcode in the text of each element. We will use regular expression to search for postcode.

If a postcode is found, we will extract all the text inside the element using the stripped_strings attribute. This attribute returns a generator of all the substrings with surrounding whitespaces stripped.

We will then print the element text.

It is worth noting that this code is a rough example and may not work for all websites, as different websites may have different HTML structures and use different conventions for indicating address information.

The task at hand is to extract valid addresses from a list of company websites. The addresses must be in the format of country, region, city, postcode, road, and road numbers.

The first step in solving this problem is to understand the structure of the data. In this case, we are given a list of company websites in a snappy parquet file format. The websites are stored in a column called 'domain'. We will read the file using the pyarrow.parquet package and convert it to a pandas dataframe. Then we will extract the list of websites from the 'domain' column.

Once we have the list of websites, we need to iterate through each website and make a request using the requests library. We will parse the HTML of the website using BeautifulSoup. We will then search for all the span, p, and a elements on the page.

The next step is to search for the postcode. We will use the re library to search for the postcode in the text of each element. We will use regular expression to search for postcode.

If a postcode is found, we will extract all the text inside the element using the stripped_strings attribute. This attribute returns a generator of all the substrings with surrounding whitespaces stripped.

We will then print the element text.

It is worth noting that this code is a rough example and may not work for all websites, as different websites may have different HTML structures and use different conventions for indicating address information.
