# Experiment 8 - Basic Tools of EDA Using Pandas Arrays

Pandas was originally built entirely on top of NumPy. While NumPy is incredibly fast for numerical data, it has two major "blind spots" that led to the creation of the Pandas Extension Array (EA)

### Aim:

To study about the basic tools used for EDA using Pandas arrays

### Tools used:

Google Colab or Jupyter Notebook

### Theory:

A Pandas Array (often accessed via pd.arrays.*) is a 1D container that implements the Extension Array interface. This interface allows Pandas to define new data types that behave like NumPy arrays but carry extra features.

**Key Characteristics**

* **Nullable Types:** Unlike NumPy, Pandas Arrays use a separate "mask" (a boolean array) to track where data is missing without changing the data type of the entire array.

* **Consistency:** They provide a unified way to handle specialized data types (Categorical, Sparce, String, Integer with Nulls).

* **The .array Attribute:** You can extract these from a Series using series.array. This returns the underlying Pandas Array rather than a NumPy array (which you’d get via .values).

**Problems Faced by using Numpy arrays:**


















NumPy (Numerical Python) is the foundational library for scientific computing in Python. While Python lists are versatile, they aren't designed for heavy-duty mathematical processing. NumPy fills this gap by introducing the ndarray (n-dimensional array), a data structure designed for speed, memory efficiency, and mathematical elegance.

**Functions of Numpy Arrays:**

**(i)The concept of homogeneity:**

--> In Python, a list can contain elements of various data types inside it. It is because the list stores only the memory address of the data.

--> Numpy arrays can store elements of a particular data type only inside it.

--> This allows the system to know how many bits each and every element occupies so that the system can jump wherever and whenever needed.

--> It makes it fast and efficient instead of going all over again to search for an element.

**(ii) Contiguous Blocks of Data:**

--> Numpy arrays store data as contiguous blocks of memory, i.e., the data is stored next to each other in RAM.

--> Since the NumPy elements are adjacent, it makes it easier for the processor while fetching the data, i.e., the processor can predetermine the upcoming element and fetch them.

**(iii) The Metadata:**

--> The numpy elements have 2 types of data.

* Raw Data

* Metadata

--> The raw data simply means the memory buffer.

--> Whereas a meat data is how the raw data is interpreted.

It includes the dimension of an array, the data type of the elements present inside it, etc.

**(iv) Views vs. Copies:**

--> Since NumPy is designed for massive datasets, it avoids copying the data whenever possible.

--> When slicing or reshaping of an array takes place, NumPy usually creates a view.

--> This is just new metadata, which is shown to the user.

--> But if any changes are made in this view mode, the original array also changes.

**Basic Commands Used in NumPy:**

* np.array—Used to create a new array or convert a Python list to an array

  

* np.linspace—It is used as an alternative for step size in arrays.

  

* .ndim—Returns the number of axes the array has

  

* .shape—Returns a tuple representing the dimensions (rows, columns)

  

* np.sum - Gives the sum of all elements in the array

  

* np.mean—calculates the arithmetic mean of all elements

### Applications of Numpy Arrays:

* Digital Image Processing: For a computer an image is seen as a 3D NumPy array.

* Data Science and Tabular Analytics: Financial institutes run Monte Carlo simulations to predict stock market behavior.

* Machine Learning and AI: The systems used in this are built on tensors, which are nothing but N-dimensional arrays.

   

### Advantages:

* Speed: Loops are not used to perform any major functions; instead, vectorization is done.

* Memory Efficiency:

--> Every data has the same data type, so no type data needs to be stored.

--> Since it stores the data where the raw data is stored, no extra memory of address needs to be stored.

### Learning Outcomes:

* The NumPy array is the same as Python lists, but it can handle massive data very quickly and efficiently.

* It doesn't create a duplicate copy of the array every time some change is done; instead, a view is created where the array can be modified.

* Similar to lists, aggregate functions can be used in arrays also.

* The only difference between NumPy arrays and Python lists is the homogeneity of elements stored inside them.

* Predictability and Consistency: NumPy arrays are statically typed; they prevent a lot of common bugs found in data science.

### Conclusion:

Thus, basic commands in NumPy are executed in a basic array, and the output is verified.

