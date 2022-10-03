---
title: Pandas Help
last_modified_at: 2022-10-03
excerpt_separator: “<!—more—>”
categories:
  - Blog   
tags:  
  -  Python  
---
<details>
<summary>Group by a category, count the totals, and sort descending</summary>
 
```python    
df.groupby('col1', as_index = False).size().sort_values(ascending=False)    
lemurs.groupby('taxon', as_index = False).size().sort_values(by='size',ascending=False)     
```     
  
</details>
