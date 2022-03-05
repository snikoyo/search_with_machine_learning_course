# Answers for Week 3

## Link to your Gitpod/Github repo 

https://github.com/snikoyo/search_with_machine_learning_course

Branch: my-week-3

## 1. For classifying product names to categories:

### a. What precision (P@1) were you able to achieve?

P@1     0.656
R@1     0.656

### b. What fastText parameters did you use?

` -lr 1.0  -epoch 25 -wordNgrams 2 -maxn 0 -minn 0`

### c. How did you transform the product names?

First, I removed the duplicate product names (there were over 20000 of them) using `sort | uniq | shuf > output.fasttext`.
Then I tokenized and stemmed them (the stemmer also lowercased), using NLTK and the Porter Stemmer:

```    words = word_tokenize(product_name)
       words = [ps.stem(w) for w in words]
    
       product_name_transformed = ' '.join(words) ```

Also, I used 20000 product names instead of 10000 in the training set. 


### d. How did you prune infrequent category labels, and how did that affect your precision?

## 2. For deriving synonyms from content:

### a. What 20 tokens did you use for evaluation?

#### brands

Windows
Pioneer
Nintendo
KitchenAid
Toshiba


### b. What fastText parameters did you use?

### c. How did you transform the product names?

### d. What threshold score did you use?

### e. What synonyms did you obtain for those tokens?
