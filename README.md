# faster_RCNN_anchor_box
#### 示范faster-RCNN如何生成20000个anchor box及可视化最终的图像


每16像素为步长的扩展anchor box

600/16 * 1000/16 的anchor box中心点

<img src = "https://github.com/Stephenfang51/faster_RCNN_anchor_box/blob/master/2000%20anchor%20box%20center%20point.png?raw=true">

以3种长宽比(0.5, 1, 2)以及三种缩放系数(8, 16, 32)生成的9个基础anchor box
<img src = "https://github.com/Stephenfang51/faster_RCNN_anchor_box/blob/master/9%20anchor_base.png?raw=true">

将2394个中心点利用9个anchor box坐标进行延伸，形成如下遍布整副图像21546个anchor（2394x9)
<img src="https://github.com/Stephenfang51/faster_RCNN_anchor_box/blob/master/20000%20anchor%20boxes.png?raw=true">

#### 希望读过代码的朋友能更了解到anchor box在faster rcnn是如何生成的，我自己在阅读的时候，就一直对20000个生成很好奇如何实现的，自己实现一次也就通了
