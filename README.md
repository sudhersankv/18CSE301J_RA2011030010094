# 18CSE301J_RA2011030010094
<a href="https://sudhersankv.github.io/18CSE301J_RA2011030010094/">18CSE301J_RA2011030010094</a>
<h1><strong>IV Project Sample Visualizations using Python, D3, Tableu, Giphy</strong></h1>
<p><em>Here I've visualized my chosen dataset using different tools and platforms and uploaded some samples below.</em></p>
<h2><small>Python</small></h2>
<h3>Code:</h3>
<pre><code>
import pandas as pd
import matplotlib.pyplot as plt
.
#Read the CSV file and store it in a DataFrame

df = pd.read_csv('indpowdata.csv')


#Group the data by primary fuel and sum the values in the 'Capacity MW' column for each primary fuel

grouped_data = df.groupby(['primary_fuel'])['capacity_mw'].sum()

#Plot the data

grouped_data.plot(kind='bar')

#Add x and y axis labels and a title

plt.xlabel('Primary Fuel')
plt.ylabel('Capacity (in MW)')
plt.title('Capacity by Primary Fuel in India')

#Show the plot

plt.show()
</code></pre>


<figure>
  <img src="IV/Python Viz 1.png" alt="Visualization 1 using Python (Cap in MW wrt Primary Fuel)">
  <figcaption>Visualization 1 using Python (Cap in MW wrt Primary Fuel)</figcaption>
</figure>
<h2><small>Python</small></h2>
<h3>Code:</h3>
<p>Visualization of Capacity WRT Location in India</p>
<pre><code>
import matplotlib.pyplot as plt

#Create the scatter plot
plt.scatter(df['longitude'], df['latitude'], s=df['capacity_mw']*0.1, alpha=0.5)

#Add axis labels and a title
plt.xlabel('Longitude')
plt.ylabel('Latitude')
plt.title('Capacity (in MW) by Location in India')

#Show the plot
plt.show()
</code></pre>
This adds a new heading for the second visualization and the code for creating a scatter plot of the capacity vs. location in India. The code block is again enclosed within pre and code tags to preserve the formatting and add syntax highlighting.
<figure>
  <img src="IV/scatterplot Python Viz 2.png" alt="Visualization 1 using Python (Cap in MW wrt Primary Fuel)">
  <figcaption>Visualization 2 using Python (Cap in MW wrt Location in India)</figcaption>
</figure>




