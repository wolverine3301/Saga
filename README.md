<img src="https://github.com/wolverine3301/Saga/blob/master/logo.png" width="516" height="138">

### What is it?
Saga is a data manipulation tool aimed to be similar to pandas in python in usability.
You can use it to load plain text data file formats, such as **.csv** and **.tsv** into a table like structure that can be easily manipulated.
It can handle various data types such as string, integer and doubles, as well as missing values. Also attempts to automatically determine types on loading

## Main Objects
* **Particle** - the building block of Saga. A particle encapsulates a value, such as string or a number and attempts to resolve to the correct type such as a Double Particle or a String Particle. There is also Object Particle for custom objects, and NANParticle for missing values. Particles inside a **Row** will have links to their original neighbors so sorting a **Column** it will not lose track of the original row.
* **Column** - a Vartical ArrayList of any type of **Particle**. The column has many attributes such as name and type. The Column type attribute is to represnt the type of data whithin the column such as Number/ String/ Object ect. , this is automatically determined at loading but is possible to be wrong but will not throw an error. Columns other attributes are mostly basic statistics of the data stored within it. 
* **Row** - a hosizontal ArrayList of particles.
* **DataFrame** - the entire table of data that is composed of **Column Objects** , as well as additional info such as number of columns/rows, totals
