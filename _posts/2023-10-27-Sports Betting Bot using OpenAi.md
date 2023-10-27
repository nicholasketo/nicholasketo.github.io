---
title: "Sports Betting NBA Analytics"
layout: post
---

## Predicting the outcome of NBA games using Machine Learning
Using OpenAi, NBA games were modelled. 

```javascript
#Remove Preexisting Files
! rm -rf NBA-Machine-Learning-Sports-Betting
! rm -rf *

#Bootstrap Files
! git clone https://github.com/kyleskom/NBA-Machine-Learning-Sports-Betting.git
! mv -v ./NBA-Machine-Learning-Sports-Betting/* .
! pip3 install -r requirements.txt

#Clear Bootstrap Logs
from IPython.display import clear_output
clear_output()

print("Successful Bootstrap!!!")
```

