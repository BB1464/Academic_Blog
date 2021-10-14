---
date: "2021-01-01"
highlight: true
title: Visualization
type: book
weight: 30
---
Learn how to visualize data with ggplot2.

<!--more-->

{{< icon name="clock" pack="fas" >}} 1-2 hours per week, for 8 weeks

## Learn

{{< youtube hSPmj7mK6ng >}}

## Quiz

{{< spoiler text="When is a heatmap useful?" >}}
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
{{< /spoiler >}}

{{< spoiler text="Write ggplot2 code to render a bar chart" >}}
```{r}
data(mtcars)
library(ggplot2)
ggplot(mtcars,aes(mpg,hp))+geom_point()
```
{{< /spoiler >}}


<style type="text/css">

h1.title {
  font-size: 12px;
  color: Dark;
  text-align: centre;
}

<style>
body{
text-align: justify}
</style>

