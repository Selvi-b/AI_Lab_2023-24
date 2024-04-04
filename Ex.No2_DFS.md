# Ex.No: 2  Implementation of Depth First Search
### DATE:19/03/2024                                                                            
### REGISTER NUMBER :212221060147 
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
```
def dfs(graph, start, visited=None):
    if visited is None:
        visited = set()
    visited.add(start)
    print(start, end=' ')

    for neighbor in graph[start]:
        if neighbor not in visited:
            dfs(graph, neighbor, visited)

# Example usage:
graph = {
    'A': ['B', 'C'],
    'B': ['D', 'E'],
    'C': ['F'],
    'D': [],
    'E': ['F'],
    'F': []
}

print("DFS traversal:")
dfs(graph, 'A')
```



### Output:

![WhatsApp Image 2024-04-04 at 20 33 16_82f64141](https://github.com/DrUmaRaniV/AI_Lab_2023-24/assets/166032806/294ec881-ad9a-4d76-a2fb-294aee1774de)



### Result:
Thus the depth first search order was found sucessfully.
