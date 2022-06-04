Flutter apps are very performant if some of the performance optimisations are kept in mind while developing the apps. No doubt, apps can become laggy and janky.

**1: Use smaller image files:**
No doubt, images are essential for any mobile application. And this is the area where performance gets the hit by a good margin, if not managed correctly. I started my journey as an Android Developer and I soon experienced lot of lag and poor performance in my apps. Later, I found that I was using the images which were of several MBs each. The resolution of image assets was much higher than required.
This took lot of time for device to load the assets and draw pixels, increasing CPU & GPU’s work. Sometimes, images even failed to load, making app completely unresponsive.
Here are some tips to follow to avoid performance issues related to image assets.
Try reducing size of you images from tinypng.
Lower the resolution of image here. Make sure the resolution is not more than any higher end device’s resolution.

**2: Avoid Unnecessary Animations:**
Animation is a foe of performance, using animations may cause your device resources to constantly work (since the animation values are generated again & again). CPU constantly needs to generate values & GPU has to redraw widgets.

**3: Remove Redundant Widgets:**
Personally, I used lot of redundant widgets like useless containers & other widgets which did not contribute to overall UI feel of the app. Gradually, I realised that this was becoming my habit. Although this can be subjective. Make sure to use only those widgets which are necessary.

**4: Proper State Management:**
A proper state management solution can make your app very efficient & avoid computational overhead. A typical Flutter app may contain hundreds of widgets. Updating these widgets & redrawing them again & again may cause your device to work more. The proper state management allows only necessary widgets to update their state or redraw. Let’s assume that you are using Provider as your state management tool for the app, Provider will only notify its listeners i.e consumer widgets. Only widgets listening to that Change Notifier Provider will update.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/4465dbpfwodw839nwa9x.png)

**5: Use Dart Dev Tools (Flutter Dev Tools):**
Dart Dev Tools is a combination of some useful profiling tools which can help to determine which widget or functionality is taking much processing power and cause lag or jank. Dev Tools illustrate a clear picture of things happening at main & UI thread.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6amt62j3cipedxg740tk.png)

**6: Use Const Widgets Wherever Possible:**
It is good practice to use the keyword const for constants that we can initialise at compile time. Let's also not forget to use const as much as possible for our widgets, this allows us to catch and reuse widgets to avoid unnecessary rebuilds that are caused by their ancestors.

**7: Avoid Functional Components:**
Flutter is all about widgets, creating a custom widget can be done in two popular ways. Either create a function returning respective widget (functional approach) or create a whole new widget. It is highly recommended to create either Stateless or Stateful widget rather than creating a function.

I hope this article will help to make performant Flutter apps.