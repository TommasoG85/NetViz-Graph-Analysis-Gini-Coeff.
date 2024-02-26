# NetViz: Network Analysis and Visualization Toolkit

NetViz is a powerful toolkit designed for network analysis and visualization tasks in Python. Leveraging the capabilities of NetworkX and Matplotlib libraries, NetViz provides a comprehensive set of tools to explore, analyze, and visualize various types of graph structures.

## Features

- **Graph Generation**: Easily generate different types of graphs including complete graphs, Barabási-Albert graphs, and scale-free graphs.
  
- **Degree Distribution Analysis**: Calculate and visualize the degree distributions of nodes within generated graphs, providing insights into the connectivity patterns.
  
- **Gini Coefficient Calculation**: Measure the inequality in the distribution of connections using Gini coefficients, aiding in understanding the network's structure.
  
- **Customizable Visualization**: Customize the visual representation of graphs and degree distributions to suit specific analysis needs.

## Usage

1. **Installation**: Install the required dependencies using `pip install -r requirements.txt`.
  
2. **Generating Graphs**: Use NetViz to create different types of graphs using provided functions.
  
3. **Analyzing Degree Distributions**: Calculate and visualize degree distributions for generated graphs to gain insights into network connectivity.
  
4. **Computing Gini Coefficients**: Utilize NetViz to compute Gini coefficients for degree distributions, enabling the quantification of connectivity inequality.
  
5. **Customization**: Customize visualizations by adjusting parameters such as node color, size, and edge color.

## Examples

```python
import networkx as nx
import matplotlib.pyplot as plt
import numpy as np
from netviz import gini_coefficient, plot_degree_distribution

# Create a Barabási-Albert graph
ba_graph = nx.barabasi_albert_graph(100, 2)

# Calculate degree distribution and Gini coefficient
degrees = list(dict(ba_graph.degree()).values())
gini_coef = gini_coefficient(degrees)

# Plot degree distribution
plot_degree_distribution(degrees, gini_coef)
plt.show()
```

## Contributing

Contributions are welcome! Feel free to open issues for feature requests, bug fixes, or general improvements. Pull requests are also appreciated.

## License

This project is licensed under the CREATIVE COMMONS - see the [LICENSE](LICENSE) file for details.
