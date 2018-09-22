The simplest way to make your images appear "retina" (and optimize them for retina displays) is to define their width and height values as only half of what the original file is.

Here is an example of an image that is only using half of the original height and width:
```
<style>
  img { height: 250px; width: 250px; }
</style>
<img src="coolPic500x500" alt="A most excellent picture">
```

## responsive images
 use:
```
img {
  max-width: 100%;
  display: block;
  height: auto;
}
```