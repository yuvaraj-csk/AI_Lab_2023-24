# Ex.No: 2  Implementation of Depth First Search
### DATE: 17/02/2024                                                                         
### REGISTER NUMBER : 212221040187
### AIM: 
To write a python program to implement Depth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function dfs and take the set “visited” is empty 
4. Search start with initial node. Check the node is not visited then print the node.
5. For each neighbor node, recursively invoke the dfs search.
6. Call the dfs function by passing arguments visited, graph and starting node.
7. Stop the program.
### Program:
~~~
graph = {
    '1': ['2', '3'],
    '2': ['4', '5'],
    '3': ['6', '7'],
    '4': [],
    '5': [],
    '6': [],
    '7': [],
}
visited = set()
def dfs(node, graph):
    if node not in visited:
        print(node)
        visited.add(node)

        if graph[node]:
            for neighbor in graph[node]:
                dfs(neighbor, graph)

dfs('1', graph)
~~~

### Output:

![image](https://github.com/yuvaraj-csk/AI_Lab_2023-24/assets/134052574/62d30525-97ff-40ad-983e-594e8b2181a2)


### Result:
Thus the depth first search order was found sucessfully.
