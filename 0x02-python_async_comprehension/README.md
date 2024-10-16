# Async Comprehension in Python

## Author
**Harrison Eze**  
GitHub: [harystyleseze](https://github.com/harystyleseze)  
Email: [harystyleseze@gmail.com](harystyleseze@gmail.com)

## Repository
This repository contains solutions to the ALX Backend Python project, focusing on asynchronous programming and comprehensions in Python.

- **GitHub Repository**: [alx-backend-python](https://github.com/harystyleseze/alx-backend-python)
- **Directory**: `0x02-python_async_comprehension`

## Project Overview
Asynchronous programming is a powerful tool in Python that allows for concurrent execution of tasks, enhancing performance and responsiveness. This project demonstrates how to use asynchronous features in Python, particularly:
- **Asynchronous Generators**: Yielding values from a generator asynchronously.
- **Async Comprehensions**: Collecting results from asynchronous iterables in a concise manner.
- **Runtime Measurement**: Evaluating the execution time of asynchronous operations to understand their performance characteristics.

### Goals
The primary goals of this project include:
- Understanding how to create and use asynchronous generators.
- Utilizing async comprehensions for collecting results from async generators.
- Measuring the execution time of concurrent tasks to gauge efficiency.
  
## Files Included
### 1. `0-async_generator.py`
- **Description**: Defines a coroutine named `async_generator` that asynchronously yields 10 random numbers between 0 and 10, with a 1-second delay between each yield.
- **Key Concepts**: Async Generators, `async def`, `await`, `random` module.

### 2. `1-async_comprehension.py`
- **Description**: Implements a coroutine called `async_comprehension` that collects 10 random numbers from `async_generator` using async comprehensions.
- **Key Concepts**: Async Comprehensions, List Comprehensions, Asynchronous Iteration.

### 3. `2-measure_runtime.py`
- **Description**: Defines a coroutine `measure_runtime` that executes `async_comprehension` four times in parallel using `asyncio.gather` and measures the total runtime.
- **Key Concepts**: Parallel Execution, Runtime Measurement, `asyncio.gather`.

### 4. `0-main.py`
- **Description**: A main script to test the `async_generator` coroutine by printing the list of random numbers generated.
  
### 5. `1-main.py`
- **Description**: A main script to test the `async_comprehension` coroutine and display the collected random numbers.
  
### 6. `2-main.py`
- **Description**: A main script that tests the `measure_runtime` coroutine, printing the total time taken for the four async calls.

## Usage Instructions
To run the scripts, ensure you have Python 3.7 or higher installed on your system. Follow the steps below:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/harystyleseze/alx-backend-python.git
   cd alx-backend-python/0x02-python_async_comprehension
   ```

2. **Run the Main Scripts**:
   Each main script can be executed independently to test the respective coroutine:
   ```bash
   # Test async_generator
   ./0-main.py
   
   # Test async_comprehension
   ./1-main.py
   
   # Test measure_runtime
   ./2-main.py
   ```

3. **Expected Output**:
   - `0-main.py`: A list of 10 random floating-point numbers.
   - `1-main.py`: A list of 10 random numbers collected using async comprehension.
   - `2-main.py`: The total runtime of executing async_comprehension four times, which should be roughly 10 seconds.

## Performance Explanation
The total runtime for executing the `async_comprehension` coroutine four times in parallel is expected to be approximately 10 seconds. This is due to the following reasons:
- Each execution of `async_comprehension` internally calls `async_generator`, which has a 1-second wait for each of the 10 numbers, resulting in a total wait time of about 10 seconds.
- Because the calls are made concurrently (in parallel), the overall execution time does not accumulate linearly but instead reflects the time of the longest running task.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgments
This project is part of the ALX Backend Python curriculum, aimed at deepening understanding of asynchronous programming concepts in Python. Special thanks to the ALX team for their guidance and support throughout this learning process.

## Contributions
Feel free to open issues or pull requests if you would like to contribute to this project. Your feedback and improvements are welcome!
```
