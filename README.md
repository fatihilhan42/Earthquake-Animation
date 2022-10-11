# Earthquake-Animation
An earthquake (also known as a quake , tremor or temblor ) is the shaking of the surface of the Earth, resulting from the sudden release of energy in the Earth 's lithosphere that creates seismic waves . (Wiki) Animation with Plotly

## Dataset import
```Python
data = pd.read_csv("../input/database.csv")
data = data.drop([3378,7512,20650])
data["year"]= [int(each.split("/")[2]) for each in data.iloc[:,0]]
```

![image](https://user-images.githubusercontent.com/63750425/195078199-af4efac0-1262-426c-8e24-15f0524fc18b.png)

```Python
data.Type.unique()
```

```Python
dataset = data.loc[:,["Date","Latitude","Longitude","Type","Depth","Magnitude","year"]]
dataset.head()
```

![image](https://user-images.githubusercontent.com/63750425/195078332-8320c172-d60f-4298-9088-c2cec424936d.png)

## Output Image

![image](https://user-images.githubusercontent.com/63750425/195078434-cbfb0fca-eef7-4ae2-8900-bf35dd341130.png)


