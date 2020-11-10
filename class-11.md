# Reading Notes
### class 11


## Images

- You can control the size of an image using height and width.

- To make images responsive to all sizes of viewports use percents% or VW or VH in your height or width.

- You can just use sizes for the height or witdh , like small, medium or large.

- Align images to either the left or right using floats

- Align images to the center by using the property text-align witht the value of center on the parent element.

- The background image allows you to place an image behind the content inside the element. ``` background-image: url('images/pattern.gif'); ```

- Backgrond images can be put on repeat across the background of an element.

- You can create roll over efects by moving the position of the background image.

- to reduce the amount of images a  browser has to load, you can create image sprites.



## Practical Information

- SEO stands for search engine optimization. It is the practice of deploying a content strategy with the goals of getting a webpage to the top of google search results.

- On page SEO techniques are methods you can use on your web pages to improve their rating in search engines. This would be keyword filling, making sure that every image has alt tags, and being strategic with your H1 tag.

- Off page SEO techniques are having relevant links or getting a lot of link backs. Site speed and organized to be opimized for googles web crawlers.

- Finding key words to add to your site is easy. There are keyword google chrome plug in that tell you what keywords someone else is using. Go to youtube and search something related to your website. Click on the top 5 and see what keywords they are using. This can give you a good idea, write down the ones you see repeating. Then take those keywords over to google trends and study to find the words on the most upwards trajectory. Ride the wave. 

- Figure out who your user is. Use google analytics to get a sense of your current visitors. Look for age, genders, and other intrest. The most time the site is up the better of an idea you will get of your users.

- FTP programs allow you to transfer files from your local computer to your web server.

## Audio and Video

- The ``` <video> <audio> ``` elements allow us to embed video and audio into web pages. 

```<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
</video>```


```<div class="player">
  <video controls>
    <source src="video/sintel-short.mp4" type="video/mp4">
    <source src="video/sintel-short.webm" type="video/webm">
    <!-- fallback content here -->
  </video>
  <div class="controls">
    <button class="play" data-icon="P" aria-label="play pause toggle"></button>
    <button class="stop" data-icon="S" aria-label="stop"></button>
    <div class="timer">
      <div></div>
      <span aria-label="timer">00:00</span>
    </div>
    <button class="rwd" data-icon="B" aria-label="rewind"></button>
    <button class="fwd" data-icon="F" aria-label="fast forward"></button>
  </div>
</div>
```

CSS styling
```
.controls {
  visibility: hidden;
  opacity: 0.5;
  width: 400px;
  border-radius: 10px;
  position: absolute;
  bottom: 20px;
  left: 50%;
  margin-left: -200px;
  background-color: black;
  box-shadow: 3px 3px 5px black;
  transition: 1s all;
  display: flex;
}

.player:hover .controls, player:focus .controls {
  opacity: 1;
}

```




