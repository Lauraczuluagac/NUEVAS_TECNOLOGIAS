<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 

...
import pandas as pd
import streamlit as st
import matplotlib.pyplot as plt

data = pd.read_csv('ventas_vehiculos .csv')

st.header("Tabla antes de la limpieza de datos")
data
#datos vacios
data = data.dropna()

#datos atipicos
plt.hist(data["Kilometraje"])
st.pyplot()

plt.boxplot(data["Kilometraje"])
st.pyplot()

data.plot.scatter(x="Estado", y="Kilometraje")
st.pyplot()

data = data[~((data["Kilometraje"] > 5.000) & (data["Estado"] == "Usado"))]
data = data[data["Año"]>2010]



#formato de datos
#st.write(data.dtypes)
data["Fecha"] = pd.to_datetime(data["Fecha"])
#st.write(data.dtypes)

st.header("Tabla con limpieza de datos")
data

...

https://sesion9-ag6zpyhxgicwvhdxbwxyrr.streamlit.app/

<!-- Su documentación aquí -->






