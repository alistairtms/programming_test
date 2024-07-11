# Question 3

Write a function that flattens all the items in an array. For example, the array [1, [2, 3], [[4], [5]]] becomes [1, 2, 3, 4, 5].

Assume that the array contains only numbers and other arrays, which in turn only contain numbers and other arrays.

def flatten(nested_list):
    flat_list = []
    for item in nested_list:
        if isinstance(item, list):
            flat_list.extend(flatten(item))
        else:
            flat_list.append(item)
    return flat_list




