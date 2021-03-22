# Predicting Optimal Bid Price Strategy for Advertising Data

## OBJECTIVE
A basic machine learning model that uses the associated criteo dataset and predicts the optimal bid price for the next period based on the included features.

## Source
https://ailab.criteo.com/criteo-attribution-modeling-bidding-dataset/

## Key figures
* 2,4Gb uncompressed
* 16.5M impressions
* 45K conversions
* 700 campaigns

## About the Dataset
* timestamp: timestamp of the impression (starting from 0 for the first impression)
* uid -  a unique user identifier campaign a unique identifier for the campaign
* conversion - 1 if there was a conversion in the 30 days after the impression (independently of whether this impression was last click or not)
* conversion_timestamp - the timestamp of the conversion or -1 if no conversion was observed
* conversion_id - a unique identifier for each conversion (so that timelines can be reconstructed if needed). -1 if there was no conversion
* attribution - 1 if the conversion was attributed to Criteo, 0 otherwise
* click - 1 if the impression was clicked, 0 otherwise
* click_pos - the position of the click before a conversion (0 for first-click)
* click_nb - number of clicks. More than 1 if there was several clicks before a conversion
* cost - the price paid by the company for this display
* cpo - the cost-per-order in case of attributed conversion 
* time_since_last_click - the time since the last click (in s) for the given impression
* cat[1-9] - contextual features associated to the display. Can be used to learn the click/conversion models.

## Summary of my analysis performed:
* Analysed 16000000+ rows of marketing data
* Pre-preprocessed rows and feature engineered columns
* Performed logistic regression to predict optimal bid price
