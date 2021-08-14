---
layout: post
title: "Sharing interactive dashboards across teams with ipywidgets and reviewNB"
author: "Archana Kumari"
tags: internal-tools success
excerpt_separator: <!--more-->
---

If you have tried to create interactions in your Jupyter Notebook turns out you might have heard about Ipython widgets. In this blog, let's explore ipywidgets, how you can create interactive dashboards with them and lastly how easily you can collaborate on your notebooks with your peers and leaders. <!--more-->

## What are ipywidgets?

In short, ipywidgets are Interactive HTML widgets for Jupyter notebooks.

These tools allow us to create interaction in our notebooks often with just a few lines of code. These widgets are particularly very handy in data exploration and analysis. Widgets will help you convert your  Jupyter Notebooks into an interactive dashboard instead of plain static documents. 

Widgets can make your notebooks look more lively and fun. To put is simply, widgets are elements like buttons, drop-down lists, sliders, etc. With widgets, you can manipulate the output according to the selection of parameters in the widget.

## Installing ipywidgets

You can easily install the latest version of ipywidgets with pip or conda.

For pip -

```jsx
pip install ipywidgets
```

For Conda -

```jsx
conda install -c conda-forge ipywidgets
```

If you have the latest version of Jupyter Notebook, installing `ipywidgets` will also automatically configure your Jupyter to use widgets. This happens with the help of the `widgetsnbextension` package. This package configures the Notebook to display and use widgets.

If you have an older version of Jupyter Notebook , then you might have to manually enable the ipywidgets notebook extension. Run the following command in your notebook cell -

```jsx
jupyter nbextension enable --py widgetsnbextension
```

Here is the expected output once you run the commands in your notebook -

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/download.png)

You can find more details on installation [here](https://ipywidgets.readthedocs.io/en/stable/index.html) 

## Your first Widget

Here is a very simple example of a widget. 

You can create a slider interaction with just these two lines of code.

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/simple.gif)

## Interacting with Widgets

The widget.IntSlider() function only displays the slider. Let's see how we can interact with it. The interact function present in the ipywidgets package easily helps us interact with our widgets. This function creates a user interface. With this we can explore and interact with our data. 

ipywidgets.interact() automatically generates UI controls for function arguments. It calls the function with the arguments whenever we want to manipulate the controls interactively. First step is to define a function in order to use interact. Here is a very simple way to interact with slider -

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/interact.png)

## Widgets Events

When you will try to manipulate a widget, a message is returned from the interaction. The message from the window system is called a widget event. Usually, when this message is received by the widget program, an action is performed. Examples of actions could be opening a file, creating a graph, etc.

Here is an example of the button widget. The button can be used to take care of the clicks. When the button is clicked, the on_click method is used to register the function.

Note that the button clicks are stateless. The message is sent from the front end to the back end once the button is pressed. You can use the output widget to print the message. Here is how you can show the message once you click on the button -

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/event.png)

## Creating complex interactive dashboards for Analysis

Let's go through an example of how you can create a complex interactive dashboard with widgets.  Create a dataframe with your choice of data. Here I have taken an example of importing data with medium article statistics. With just a slider and drop-down widget, you can easily play around with your dataframe. With the help of the interact function, you can easily manipulate data without writing additional code. 

Check out the demo [here](https://mybinder.org/v2/gh/Dhankie/notebooks.git/HEAD)

Here is a sample -

![Example](https://github.com/Archana-blog/product/blob/d3264017492acbdc076305f0d8f3a83d1db8e8c3/assets/slider.gif)

Pretty impressive, right? Now let's have look at more examples of widgets to analyze and explore data. This widget can help you find correlations between columns. The corr function computes the pairwise correlation of columns, excluding the NA/null values. Note that correlation of a variable with itself is 1.

Check out the demo [here](https://hub.gke2.mybinder.org/user/dhankie-notebooks-uto9gqfg/notebooks/ipywidgets_demo.ipynb)

Here is a sample -

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/correlation.gif)

Now let's see how you can create interactive plots using widgets. With widgets you can extend the power of plotly library. Plotly's python API can be used to plot inside your Jupyter Notebook. Here I have called the plot with iplot function which automatically generates an interactive version of the plot inside the Notebook. Here I have used selection widget. A list can be passed as values to the selection widget. You can specify the enum of the selectable options by passing a list. The options can be either (label, value) pairs, or simply values for which the labels are derived by calling str).

Check out the demo [here](https://mybinder.org/v2/gh/Dhankie/notebooks.git/HEAD)

Here is a sample -

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/maps.gif)

Here is another powerful example to create heatmap and explore your data. A heatmap is slightly more interesting way to represent data.  Data values are represented as colors in heatmap. Heatmap uses color in order to represent a value. This is a great tool to assist when you have a large volume of data.

Check out the demo [here](https://mybinder.org/v2/gh/Dhankie/notebooks.git/HEAD)

Here is a sample -

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/heatmap.gif)

## Sharing interactive dashboards with your team using ReviewNB

ReviewNB is a remarkable tool to help you share your interactive dashboards with your peers and leaders. Here are few ways to explore and reap the benefits of ReviewNB .

Notebooks are flexible and effective with data analysis. With the power of widgets, you can easily share your work with your team. Traditionally, notebooks were not that good when it comes to version control as well as collaboration. But with ReviewNB you can make your notebooks overcome these shortcomings.

Here is how ReviewNB can help you and your team to manage your work effectively -

1. **Rich Diff** -You can review and verify diffs side by side easily. GitHub diffs are not very visually appealing but with ReviewNB you can check out diffs in a more human-readable format.

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/rich_diff.png)

2. **Cell comments -** You can initiate discussions on any notebook cell within ReviewNB. This helps avoid any confusion while discussing with your teammates. You don't have to keep track of which comment corresponds to which cell. ReviewNB allows you to do that with this sleek feature.

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/cell_comment.png)

3. **Resolving open threads and conversations** - Once you have reviewed the changes, you can resolve and close the open discussions and share your insights with your team.

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/resolve_conflict.png)

Check this [here](https://app.reviewnb.com/Dhankie/notebooks/pull/1/discussion/) 

## Additional benefits of ReviewNB

With ReviewNB there are several other advantages. Here are a few more -

1. **Easy integration with GitHub -** You don't have to do any complex configuration to use ReviewNb with your notebooks. Just select a repo once you successfully log in to ReviewNB. Once your github is integrated with ReviewNB, you can see a "ReviewNB" button that can take you ReviewNB UI. 

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/easy_integration.png)

Check this [here](https://github.com/Dhankie/notebooks/pull/1)

2. **Easy history logs** - You can see who has committed when and how often. You can also see pull requests history. 

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/list.png)

Check this out [here](https://app.reviewnb.com/Dhankie/notebooks/commits/)

3. **Easily finish and discard reviews** - You have the option of discarding and finishing your comments and reviews.

![](https://github.com/Archana-blog/product/blob/9590396cc9af0e30ad12a384f684fc4f2e53609b/assets/rich_diff2.png)

## Final Thoughts

I hope this article is helpful to you all. How easily you can use your Jupyter Notebooks to create interactive dashboards using simple yet powerful widgets. Once you have your dashboards, you can leverage ReviewNB to share your dashboards with your peers and leaders. Would you like to try [ReviewNB](https://www.reviewnb.com/?utm_source=reviewnb_blog)? It is [completely free](https://github.com/marketplace/review-notebook-app/plan/MDIyOk1hcmtldHBsYWNlTGlzdGluZ1BsYW4yMDIz#pricing-and-setup) for open source and academic users. Alos, If you want to track notebooks in private repositories, [check out our options](https://www.reviewnb.com/?utm_source=reviewnb_blog#pricing)!
