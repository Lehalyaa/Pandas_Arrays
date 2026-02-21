# Experiment 8 - Basic Tools of EDA Using Pandas Arrays

Pandas was originally built entirely on top of NumPy. While NumPy is incredibly fast for numerical data, it has two major "blind spots" that led to the creation of the Pandas Extension Array (EA).

### Aim:

To study about the basic tools used for EDA using Pandas arrays

### Tools used:

Google Colab or Jupyter Notebook

### Theory:

A Pandas Array (often accessed via pd.arrays.*) is a 1D container that implements the Extension Array interface. This interface allows Pandas to define new data types that behave like NumPy arrays but carry extra features.

**Key Characteristics**

* **Nullable Types:** Unlike NumPy, Pandas Arrays use a separate "mask" (a boolean array) to track where data is missing without changing the data type of the entire array.

* **Consistency:** They provide a unified way to handle specialized data types (categorical, sparse, string, and integer with nulls).

* **The .array Attribute:** You can extract these from a Series using series.array. This returns the underlying Pandas Array rather than a NumPy array (which you’d get via .values).

**Problems Faced by Using NumPy Arrays:**

* **Missing Data ($NaN$):** In NumPy, integer arrays cannot hold NaN values.

* **Non-Numeric Data:** Handling strings, categorical data, or time zones in NumPy often defaults to the object dtype, which is slow and memory-intensive.

**Architecture of Extended Arrays:**

The main advantage of Pandas is the ability to handle nullable integers. Pandas, which is also known as Integer Extension array, keeps the data as data only and doesn't use a bitmask to store it. Its theory basically relies on a backend/frontend split.

--> **Interface:** A set of requirements that a class must satisfy to get considered as a Pandas Array

--> **Storage:** The data is stored in such a way that it is optimized for that specific type.

--> **The ExtensionDType:** Pandas Array has a corresponding ExtensionDtype that tells Pandas how to register and display the data. This can also be known as the data type of the element stored.

**Basic Commands in Pandas:**

* **df.shape** --> Returns number of rows and columns

  

* **df.columns**  -->   Returns column names

  

* **df.index**  -->   Returns row labels

  

* **df.dtypes**  -->   Returns data types of columns

  

* **df.head()**  -->    Displays first 5 rows

  

* **df.tail()**    -->    Displays last 5 rows

**Advantages of Pandas:**

--> **Vectorization**

* The operations are done in C-level looping rather than Python-level looping.

--> **Memory efficiency:**

* Storing a string as a dedicated string array can increase memory efficiency.

--> **Type Safety**

**Applications:**

* **Algorithmic Trading & FinTech:**

--> Banks and hedge funds use Pandas to find tick data.

* **IoT & Industrial Sensor Monitoring:**

--> In IoT systems, sensors constantly stream temperature and live data.

* **Dynamic Business Dashboards:**

--> E-commerce sites use pandas as the backend engine for live dashboards.

* **Log analysis and cyber security:**

--> Security systems monitor server logs in real-time to spot hacking attempts.

**Conclusion:**

Thus, the basic commands in EDA are implemented using the commands in the Pandas Library, and the output is verified.
