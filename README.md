graph = {
    'a': ['b', 'c'],
    'b': ['e', 'f'],
    'c': ['d', 'e'],
    'd': ['e'],
    'e': ['z'],
    'f': ['z'],
    'z': []
}

def dfs(graph, node, visited=None):
    if visited is None:
        visited = set()
    visited.add(node)
    print(node, end=' ')  
    
    for neighbor in graph[node]:
        if neighbor not in visited:
            dfs(graph, neighbor, visited)


print("DFS traversal order:")
dfs(graph, 'a')
