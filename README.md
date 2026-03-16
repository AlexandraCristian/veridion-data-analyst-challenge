# veridion-data-analyst-challenge
To pick the best matches, I considered columns region -> street number as the base information we have for the companies in the list, and began to filter the candidates according to the best matches between company details and candidate details.
To filter i used excel formulas:
- to check if name of the candidate matches with name of the company
- to check if country of candidate matches with country of the company
- to check the matches between address informations (region -> street number)
- if multiple candidates had the same number of matches mentioned above, i did a further check on which candidate has the most information present in the fields ibc_insurance_codes -> tiktok_url

The candidates that had less matches were removed by searching for the input_row_key without comments.
The companies considered with no match were the ones with candidades that had just a company name match and not even a country match. I separated the matches i did find with a company match grade (high -> low). For the companies considered with no match i left the first canditate on the list in the file.

Notes: Some of the companies were missing address information which made it harder to pick a match. Additional information should be added to the company information to make a more accurate match search like a tax identification number, an oficial telephone number, email.

Regarding curating the data atributes, to make the data cleaner, the following should be taken in account:
- standardization: keeping the same format in names, numbers, telephones etc
- removing diacritics
- removing duplicate data/columns (i see there are too many columns related to the industry type)
- to check with the company what fields they require for their database
