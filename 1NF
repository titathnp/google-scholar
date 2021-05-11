import pandas as pd 
import time
start_time_allprocess = time.time()
paper=pd.read_csv('paper.csv')
p_paper = pd.DataFrame(columns=['title','authors','publication_date','description','cite_by'])
rows = 0
for index, row in paper.iterrows():
    for token in str(row['authors']).split(','):
        p_paper.loc[rows]=[row['title'],token,row['publication_date'],row['description'],row['cite_by']]
        rows +=1
p_paper.to_csv('1NF_paper.csv')
print("--- %s seconds ---" % (time.time() - start_time_allprocess))
