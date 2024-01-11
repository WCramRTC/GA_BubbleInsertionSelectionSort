# Guided Assignment: Understanding Bubble, Insertion, and Selection Sort Algorithms in C#

## Introduction
In this tutorial, we'll explore three fundamental sorting algorithms in computer science: Bubble Sort, Insertion Sort, and Selection Sort. These algorithms are essential for understanding basic sorting mechanisms and will lay the groundwork for more advanced sorting techniques. We'll implement each algorithm in C# and discuss their efficiency and use cases.

---

## Detailed Requirements

### Project Setup (10 Points)
- Create a new console application in your IDE (e.g., Visual Studio).
- Name the project `SortingAlgorithms_Tutorial`.
- Ensure the project has the necessary default files (`Program.cs`).

### Bubble Sort Implementation (20 Points)
- Implement the Bubble Sort algorithm in a method called `BubbleSort`.
- The method should take an array of integers as input and sort the array.
- Provide comments explaining the logic behind Bubble Sort.

### Insertion Sort Implementation (20 Points)
- Implement the Insertion Sort algorithm in a method called `InsertionSort`.
- This method should also sort an array of integers.
- Include comments to explain how Insertion Sort works.

### Selection Sort Implementation (20 Points)
- Create a method `SelectionSort` to implement the Selection Sort algorithm.
- The method should sort an integer array.
- Use comments to describe the Selection Sort process.

### Comparative Analysis (10 Points)
- In the `Main` method, create arrays to test each sorting algorithm.
- Explain, through comments, the differences in complexity and use cases of each algorithm.

### Efficiency Discussion (10 Points)
- Discuss the time complexity of each algorithm.
- Explain scenarios where one algorithm might be preferred over the others.

### Code Testing and Output Accuracy (5 Points)
- Test each sorting algorithm with the same input array.
- Ensure the output is correctly sorted for each algorithm.

### Submission (5 Points)
- Successfully upload the complete project to a repository (e.g., GitHub).
- Ensure the repository is public and contains all necessary files.

#### Total (100 Points)
- Follow the requirements closely to meet all the criteria outlined in the rubric.

---

### Starting Code
```csharp
using System;

class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Exploring Sorting Algorithms in C#");
        // Test arrays and method calls will go here
    }

    // Method definitions for BubbleSort, InsertionSort, and SelectionSort will go here
}
```

We'll focus on implementing each sorting method within this structure.

---

## Implementing Bubble Sort

**Bubble Sort** repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The process is repeated until the list is sorted.

- Implement the `BubbleSort` method in the `Program` class.

```csharp
public static void BubbleSort(int[] arr)
{
    for (int i = 0; i < arr.Length - 1; i++)
        for (int j = 0; j < arr.Length - i - 1; j++)
            if (arr[j] > arr[j + 1])
            {
                // Swap arr[j] and arr[j + 1]
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
}
```

**Test Bubble Sort**  
- Create an array in `Main` and call `BubbleSort` to sort it.
- Print the sorted array to the console.

---

## Implementing Insertion Sort

**Insertion Sort** builds the final sorted array one item at a time, with each new element being placed into its correct position.

- Add the `InsertionSort` method to your program.

```csharp
public static void InsertionSort(int[] arr)
{
    for (int i = 1; i < arr.Length; i++)
    {
        int key = arr[i];
        int j = i - 1;

        // Move elements of arr[0..i-1], that are greater than key, to one position ahead
        while (j >= 0 && arr[j] > key)
        {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}
```

**Test Insertion Sort**  
- Test this algorithm with the same array used for Bubble Sort.

---

## Implementing Selection Sort

**Selection Sort** divides the input list into two parts: a sorted sublist of items and a sublist of the remaining unsorted items. It repeatedly selects the smallest (or largest) element from the unsorted sublist, swapping it with the leftmost unsorted element.

- Implement the `SelectionSort` method.

```csharp
public static void SelectionSort(int[] arr)
{
    for (int i = 0; i < arr.Length - 1; i++)
    {
        int minIndex = i;
        for

 (int j = i + 1; j < arr.Length; j++)
            if (arr[j] < arr[minIndex])
                minIndex = j;

        // Swap the found minimum element with the first element
        int temp = arr[minIndex];
        arr[minIndex] = arr[i];
        arr[i] = temp;
    }
}
```

**Test Selection Sort**  
- Use the same array to test and validate this method.

---

## Comparative Analysis and Efficiency Discussion

- Analyze the efficiency of each algorithm in terms of time complexity.
- Discuss when one might be preferred over the others in practical scenarios.
- Ensure these discussions are included in the `Main` method as comments.

---

## Rubric

| Criteria | Description | Points |
|----------|-------------|--------|
| **Project Setup** | Proper creation and setup of the console application. | 10 |
| **Bubble Sort Implementation** | Correct implementation and explanation of the Bubble Sort algorithm. | 20 |
| **Insertion Sort Implementation** | Accurate implementation and description of Insertion Sort. | 20 |
| **Selection Sort Implementation** | Proper implementation and explanation of Selection Sort. | 20 |
| **Comparative Analysis** | Analysis of differences in complexity and use cases. | 10 |
| **Efficiency Discussion** | Discussion on the efficiency of each algorithm. | 10 |
| **Code Testing and Output Accuracy** | Successful testing and accurate sorting of arrays. | 5 |
| **Submission** | Successful upload to a public repository with all necessary files. | 5 |
| **Total** |  | 100 |

OpenAI. (2024). Understanding Bubble, Insertion, and Selection Sort Algorithms in C#. ChatGPT Tutorial.