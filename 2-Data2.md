## 1.3 网页数据抓取
### Web scraping tools
### Craw individual pages
### Extract data
### Cost
### Crawl images
### Legal Consideration
### Summary
1. Web scraping is a powerful way to collect data at scale when the website doesn’t offer a data API
2. Low cost if using public clouds
3. Use browser’s inspection tool to locate the information in HTML
4. Be cautious to use it properly

## 1.4 数据标注 Data Labeling
### Flow Chart for Data Labelling
### Semi-Supervised Learning (SSL)
### Self-training
### Label through Crowdsourcing
Challenges：
1. Simplify user interaction
2. Cost：reduce #tasks X #time per task sent to labelers
3. Quality control
### Active Learning + Self-training
### Weak Supervision
### Summary
1. Ways to get labels：
Self-training:iteratively train models to label unlabeled data   
Crowdsourcing:leverage global labelers to manually label data   Dataprogramming:heuristic programs to assign noisy labels   
2. Alternatively, You could also consider unsupervised/self-supervised learnings