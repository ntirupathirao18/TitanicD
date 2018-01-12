import several libraries 
1. pandas
2. numpy 
3. PIL
4. os
5. matplotlib.pyplot
6. cv2
 
After importing, access the directory location of images and **dire** and extract all images into a list of **actualimages** 

Creating a **valid_images** list which consists different images format. Creating a loop of for each file in directory and checking if thee extension of thee file is present in the **valid_images** list by using the splitext function and checking whether the extension is in the **valid_images**.  Reading image using *cv2.imread* and converting into **img** to identifying of all rgb values of image by *cv2.cvtcolor* and the **img** will be a numpy array. *Resizing* the **img** used to mix up all numpy values of an image into single array list and *Reshaping* the **img** split up list array into 3 dimensional and append into **images** list.

Defining the function **find_histogram** with parameters  **K means cluster instantiation** , the fuction extract unique labels from the clusters and dividing into portions based on their existence of number of values these can be achieved by using *np.histogram* function and finding the number of portions the labels occupy and return the portions as **hist**.

Defining the function **plot_colors2** with parameters **hist** and **K means cluster centroids** . Create np array within **bar** three dimnesional of size 50*300, Iterating with all clusters labels, zipping parameters into **percent**, **color**, filling the values with the portions of bar with the color of cluster values and returning the **bar**.

Creating a machine learning model of k-means clustering, iterating the overall images **images** and fitting all images individually with 4 clusters at first. After fit of an image is done calling function of **find_ histogram** and **plot_colors2** to print the colors of most dominant of colors. The *silhouette_score* is used accracy how well values are well fitted and it gives the accracy, printing it.

To know if the colors are dominant please visit link [url](http://lokeshdhakar.com/projects/color-thief/), drop an image to see if the image color is dominant or not.

For finding the error rate, a single image with an increase of clusters is done and fitted in the model, this is considered to be error rate because if the larger clusters seperates the number of the colors in the image,so if any increase in accracy leads unindentifaction of colors, so the **accuracy** is calculated with number *silhouette_score*, and append into **accracy** with clusters value too **count_clusters**.     

Plotting the scatter plot with **accracy**  as *y- axis* and with **count_clusters** as *x-axis*.
