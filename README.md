# graphite_heatmap
Using graphite and gnuplot to create a heatmap 

Graphite is very easy to use and can create all kind of graphic for you, but one thing missing is heatmap.
which make it hard for people who would like to track down individual items and get a whole picture all at the same time. 

For example: If I would like to track down temprature of 8 servers. I am using binary hplog from hp-health.rpm. I can use graphie to generate below temprature from these 8 servers. It will look like this.
![screen shot 2016-12-17 at 3 01 52 pm](https://cloud.githubusercontent.com/assets/5915590/21289724/e3da9202-c469-11e6-8440-424f3ed7422b.png)

Which is not too useful. 

Of course we can avarage them to one single line, but then it doesn't tell you which server might overheat because the HVAC can't cover that particular area.

![screen shot 2016-12-17 at 3 20 48 pm](https://cloud.githubusercontent.com/assets/5915590/21289834/7c264766-c46c-11e6-9b70-bdfe9748b2db.png)

However, we can use gunplot to greate a heatmap for us which will provide difference color to indicate tempature within a day.
You can modify my script blade1up_Ambient to suit your needs.

The end result come out like this.

![screen shot 2016-12-17 at 3 29 02 pm](https://cloud.githubusercontent.com/assets/5915590/21289869/a6372c7c-c46d-11e6-8da4-3adadfdf4150.png)

Now we can tell the wind is coming from right side of the cluster and we could adjust HVAC wind flow accordingly to provide cold air to my servers.

And now we apply this to my other clusters and use javascript to create a webpage which save all png for everyday and every month. You can find my script above in index.html.













