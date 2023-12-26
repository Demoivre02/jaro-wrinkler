# Jaro-Winkler String Similarity and Distance

The Jaro-Winkler algorithm is a method for comparing strings and measuring the similarity or distance between them. It is commonly used in various applications, such as record linkage and spell checking. The algorithm takes two strings as input and produces a similarity score between 0 and 1, where 1 indicates identical strings and 0 indicates no similarity.

## Usage

The JaroWinkler class in this code provides both similarity and distance measures. It is implemented as a Python class that inherits from the `NormalizedStringSimilarity` and `NormalizedStringDistance` classes.

### Initialization

```python
from JaroWinkler import JaroWinkler

# Create an instance of JaroWinkler with an optional threshold (default is 0.7)
jaro_winkler = JaroWinkler(threshold=0.8)
```

### Similarity Calculation

```python
# Calculate similarity between two strings
similarity_score = jaro_winkler.similarity("string1", "string2")
print(f"Similarity Score: {similarity_score}")
```

### Distance Calculation

```python
# Calculate distance between two strings
distance_score = jaro_winkler.distance("string1", "string2")
print(f"Distance Score: {distance_score}")
```

### Threshold Retrieval

```python
# Retrieve the threshold used in the Jaro-Winkler calculation
threshold_value = jaro_winkler.get_threshold()
print(f"Jaro-Winkler Threshold: {threshold_value}")
```

## Internal Method

The `matches` method is an internal method used in the Jaro-Winkler calculation. It returns a list containing information about matches, transpositions, prefix, and length.

## Example

```python
# Example usage of Jaro-Winkler
jaro_winkler_instance = JaroWinkler()

# Calculate similarity
similarity_result = jaro_winkler_instance.similarity("apple", "aple")
print(f"Similarity: {similarity_result}")

# Calculate distance
distance_result = jaro_winkler_instance.distance("apple", "aple")
print(f"Distance: {distance_result}")
```

## Note

Ensure that you have the required dependencies installed to use this code. Additionally, you can adjust the threshold and other parameters according to your specific use case.
