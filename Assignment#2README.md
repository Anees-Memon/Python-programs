! pip install pandas

import pandas as pd

data= pd.read_csv("Pokemon.csv")
data.head()

data.head(n=10)

hp_mean = data["HP"].mean()
def set_hp(val):
    if val < hp_mean:
        return "HP Low"
    else:
        return "HP High"
    

data["HP_High_Low"]= data["HP"].apply(set_hp)
data

speed_mean = data["Speed"].mean()
def set_speed(val):
    if val < speed_mean:
        return "HP Low"
    else:
        return "HP High"
    

data["Speed_High_Low"]= data["Speed"].apply(set_speed)
data



