## Github link : 
https://github.com/sssh311318/ESL_midterm_project

## Algorithm : Cocktail Sort
這個排序法跟bubble sort很類似，他是以雙向的方式在序列中排序。
## Optimization
### BASIC 
---
area = 5352.6

latency = 810

runtime = 4250 

---
### Flatten
---
area = 29200.4

latency = 301

runtime = 1605

---
## Analyzation
---
從以上數據可以看出flatten之後，雖然latency和runtime下降了3倍左右，但是area也是增加了5倍多，我有試過UNROLL和PIPELINE，但是他合成的回報顯示說沒有地方可以UNROLL，PIPELINE的話她則回報說無法PIPELINE，我想應該是因為data dependence的原因，所以她無法pipeline，至於unroll的部分它可以合成，但是latency和BASIC一樣，AREA有多一點點，我看其他做SORTING的同學也是有相同的情況。

---
## Analyzation of unrolling and pipelining
---
### Unroll

![unrolling](https://github.com/sssh311318/ESL_midterm_project/blob/main/midterm_project/%E6%93%B7%E5%8F%96.JPG?raw=true)

如上圖所示，在合成report裡面有顯示出warming但是沒有跳error，我看合出來的area有比basic大一點點但是latency沒有改善。

### Pipeling

![pipeling](https://github.com/sssh311318/ESL_midterm_project/blob/main/midterm_project/pipeline_error.JPG?raw=true)

![nested_loop](https://github.com/sssh311318/ESL_midterm_project/blob/main/midterm_project/nested-loop.JPG?raw=true)

如上圖所示，因為我的演算法是while 裡面包著for-loop，所以沒有辦法合成。


## Result
---
BASIC_AREA

![BASIC_AREA](https://github.com/sssh311318/ESL_midterm_project/blob/main/midterm_project/basic_area.JPG?raw=true)

BASIC_LATENCY AND RUNTIME

![BASIC_LATENCY](https://github.com/sssh311318/ESL_midterm_project/blob/main/midterm_project/BASIC_LATENCY.JPG?raw=true)

FLATTEN_AREA 

![FLATTEN_AREA](https://github.com/sssh311318/ESL_midterm_project/blob/main/midterm_project/flatten_area.JPG?raw=true)

FLATTEN_LATENCY AND RUNTIME

![FLATTEN_LATENCY](https://github.com/sssh311318/ESL_midterm_project/blob/main/midterm_project/FLATTEN_LATENCY.JPG?raw=true)

---





