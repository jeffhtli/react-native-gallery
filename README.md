## fork of [react-native-gallery](https://github.com/Exilz/react-native-gallery)

## Documentaion

Quite easy to use:

```
import Gallery from 'react-native-gallery';
...

  render() {
    return (
      <Gallery
        style={{flex: 1, backgroundColor: 'black'}}
        images={[
          'http://p10.qhimg.com/t019e9cf51692f735be.jpg',
          'http://ww2.sinaimg.cn/mw690/714a59a7tw1dxqkkg0cwlj.jpg',
          'http://www.bz55.com/uploads/allimg/150122/139-150122145421.jpg'
        ]}
      />
    );
  }
```

This component utilizes **[@ldn0x7dc/react-native-view-pager](https://github.com/ldn0x7dc/react-native-view-pager)** as the scrollable container and **[react-native-transformable-image](https://github.com/ldn0x7dc/react-native-transformable-image)** as the wrapped image. 

#### Props

* **images**: array, contains image urls
* **initialPage**, **pageMargin**, **onPageSelected**, **onPageScrollStateChanged**, **onPageScroll**: inherited from **[@ldn0x7dc/react-native-view-pager](https://github.com/ldn0x7dc/react-native-view-pager)**. Check the link for more details.
* **onSingleTapConfirmed**: Called after user single taped( not a double tap)
* **onGalleryStateChanged**: function. (idle) => {}.
* **loader**: React component that will be displayed before each image has been loaded. For instance, you could use `ActivityIndicator`.




### Add your custom views above image

It's a common practice to float a comment box or like button above the image. This component provides a convenient interface to implement this feature:

- onSingleTapConfirmed(): a good time for you to display the responding floating view. 
- onGalleryStateChanged(idle): If *idle* is false, it's a good time for your to hide any floating views.

Check the Demo project for a simple demonstration.
