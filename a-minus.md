---
layout: default
title: A-Minus markup reference
---

Fontus uses **a-minus** markup to describe scenes. Scenes must
be **valid xml**, but we recommend serving them using the `.html` 
extension. View the <a href="/scenes/homeroom.html">homeroom</a>
to see an example scene.

<div class='docs' markdown="1">

# Supported entities:

## a-entity

An empty node that allows you to nest transforms and group objects.


```
<a-entity position='5 0 0' rotation='0 90 0'>
  <a-box color='#ff00aa' position='-2 0 0' />
  <a-box color='#00aaff' position='2 0 0' />
</a-entity>
```

## a-hypercard

Renders basic html (very basic renderer, no javascript, no videos, no flash)
onto a transparent plane.

```
<a-hypercard>
  <div>
    <h1>Hello world!</h1>
  </div>
</a-hypercard>
```

## a-box

Renders a cube.

```
<a-box color='#ff00aa' position='1 2 3' />
```

## a-sphere

Renders a sphere.

```
<a-sphere color='#00aaff' position='1 2 3' scale='4 4 4' />
```

## a-plane

Renders a plane on the X-Y axis.

```
<a-plane color='#00aaff' position='1 2 3' scale='4 4 4' rotation='-90 0 0' />
```

## a-obj-model

Renders an obj model from a http url.

```
<a-obj-model src='suzanne.obj' color='#00ffaa' scale='4 4 4' />
```

# Supported attributes:

## position="1 2 3"

Position expressed in meters in x, y z.

## rotation="0 45 0"

Rotation expressed in degrees as a XYZ euler angle three.js style.

## scale="2 2 2"

Scale expressed in dimensionless units in x, y, z. `1 1 1` is the
default scale.

## color='#ff00aa'

Color, supports only 6 letter hex colors.

## material='color: red; flat-shading: true'

Takes a css semicolon-seperated style list of properties.

### material='color: red'

Color property, supports only 6 letter hex colors.

### material='flat-shading: (true|false)'

Whether to use flat-shading, or the default phong shader.

### material='src: image.png'

An image to use as the texture.

### material='repeat: 10 10'

Number of times to repeat the texture on x and y

</div>