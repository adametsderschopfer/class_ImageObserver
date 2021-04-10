# ImageObserver
 'ImageObserver' class for convenient loading and correct use of loaded images

```
// alternative for one => new ImageObserver('/link/to/img-2.png');
 const imgsWhichWeNeedUseAfterTheyLoading = new ImageObserver(['/link/to/img-1.png', '/link/to/img-2.png']);

 imgsWhichWeNeedUseAfterTheyLoading.wait() // Promise status panding
   .then(               // Promise status fulfilled
     (imgs) => {
       // imgs is array with html img with loaded img
       // use 'imgs' argument here which was be loaded
     },
     (err) => {
       if (err) {
         // err obj look like => {msg: "image loading is fall", invalidUri: "link/to/img"}
       }
     }
   )
   .catch(...)
   .finally(...)
```
