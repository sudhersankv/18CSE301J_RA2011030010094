
<!DOCTYPE html>
<html>
<title>18CSE301J-INFORMATION VISUALIZATION</title>

<head>
    <style>
h1 {
  text-align: center;
}
h2 {
  text-align: center;
}
</style>
</head>
<a href="https://sudhersankv.github.io/18CSE301J_RA2011030010094/">18CSE301J_RA2011030010094</a>
<h1><strong>IV Project Sample Visualizations using Python, D3, Tableu, Giphy</strong></h1>
<p><em>Here I've visualized my chosen dataset using different tools and platforms and uploaded some samples below.</em></p>
<body>
 
    <h2>Sudhersan K V  (RA2011030010094)</h2>
    <h2>TABLEAU PROJECT</h2>
  <div class='tableauPlaceholder' id='viz1678650929761' style='position: relative'><noscript><a href='#'><img alt='Comparing Capacity WRT Primary Fuel ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Bo&#47;Book1_16786509156870&#47;ComparingCapacityWRTPrimaryFuel&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Book1_16786509156870&#47;ComparingCapacityWRTPrimaryFuel' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Bo&#47;Book1_16786509156870&#47;ComparingCapacityWRTPrimaryFuel&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-GB' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1678650929761');                    var vizElement = divElement.getElementsByTagName('object')[0];                    vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>
    </div>
</body>
<h2>Python Project</h2>
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

</html>
