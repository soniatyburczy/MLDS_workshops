https://www.kaggle.com/datasets/kaggleprollc/phishing-url-websites-dataset-phiusiil

data prep (how this dataset became `phishing_urls.csv`)
* 237k rows -> 20k (random sampling, `random_state=64`)
* dropped all columns except URL and label
* reversed label column (in this dataset `1` indicates real url and `0` indicates phising url -> `0` for real url,
`1` for phishing url)