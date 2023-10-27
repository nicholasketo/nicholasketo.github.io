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

```javascript
%pip install scipy

%pip install tensorflow[and-cuda]
%pip install --upgrade tensorflow-hub


%pip install colorama


%pip install sbrscrape
```

```javascript
import os
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '2'

! python3 main.py -xgb -odds=fanduel

```

```javascript

!pip install openai

```

```javascript

## Add GPT Explanation


# Import the OpenAI library
import openai

# Set the API key
openai.api_key = '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'

# Define the text to summarize
text = "------------------fanduel odds data------------------Detroit Pistons (144) @ Charlotte Hornets (-172) Denver Nuggets (-205) @ Memphis Grizzlies (172) New York Knicks (100) @ Atlanta Hawks (-118) Miami Heat (300) @ Boston Celtics (-375) Oklahoma City Thunder (122) @ Cleveland Cavaliers (-144) Toronto Raptors (116) @ Chicago Bulls (-136) Houston Rockets (116) @ San Antonio Spurs (-136) Brooklyn Nets (188) @ Dallas Mavericks (-225) LA Clippers (-186) @ Utah Jazz (156) Orlando Magic (-144) @ Portland Trail Blazers (122) Golden State Warriors (114) @ Sacramento Kings  (-134)---------------XGBoost Model Predictions---------------Charlotte Hornets (59.4%) vs Detroit Pistons: OVER 227 (53.2%) Memphis Grizzlies (64.0%) vs Denver Nuggets: UNDER 222 (63.2%) Atlanta Hawks vs New York Knicks (51.6%): UNDER 229.5 (54.8%) Boston Celtics (62.2%) vs Miami Heat: UNDER 217 (65.5%) Cleveland Cavaliers (69.8%) vs Oklahoma City Thunder: UNDER 226.5 (53.8%) Chicago Bulls (62.1%) vs Toronto Raptors: OVER 216.5 (67.9%) San Antonio Spurs vs Houston Rockets (50.7%): OVER 226 (72.2%) Dallas Mavericks (50.7%) vs Brooklyn Nets: OVER 231.5 (59.0%) Utah Jazz vs LA Clippers (57.9%): UNDER 229 (51.0%) Portland Trail Blazers vs Orlando Magic (50.7%): UNDER 223.5 (60.8%) Sacramento Kings (63.8%) vs Golden State Warriors: OVER 238.5 (67.4%)--------------------Expected Value---------------------Charlotte Hornets EV: -6.09 Detroit Pistons EV: -0.9 Memphis Grizzlies EV: 74.21 Denver Nuggets EV: -46.51 Atlanta Hawks EV: -10.62 New York Knicks EV: 3.24 Boston Celtics EV: -21.24 Miami Heat EV: 51.28 Cleveland Cavaliers EV: 18.24 Oklahoma City Thunder EV: -32.91 Chicago Bulls EV: 7.76 Toronto Raptors EV: -18.14 San Antonio Spurs EV: -14.42 Houston Rockets EV: 9.47 Dallas Mavericks EV: -26.7 Brooklyn Nets EV: 41.85 Utah Jazz EV: 7.8 LA Clippers EV: -10.98 Portland Trail Blazers EV: 9.43 Orlando Magic EV: -14.08 Sacramento Kings EV: 11.35 Golden State Warriors EV: -22.45"

# Use the OpenAI API to summarize the text
response = openai.Completion.create(
    engine="text-davinci-002",
    prompt=(f"summarize this text: {text}"),
    max_tokens=100
)

# Print the summary
print(response["choices"][0]["text"])

```

