# Cassini App 
This app was built by following along on the itunesU class Stanford cs193p lecture 9. This is a simple split view app that fetches for images over the network off of the main thread.  Then displays that image into to the detail view.   

![LandScape Screenshot](https://github.com/ajrosario08/Cassini/blob/master/landscape.png)
![Portrait Screenshot](https://github.com/ajrosario08/Cassini/blob/master/portrait.png)

## Topics covered 

### Lecture 9 
- Scrollview 
  - Can be embed in itself
  - Set .contentSize
  - .addSubviews
  - Set scrollView.delegate
  - Zooming 
  - set .minimumZoomScale
  - set .maximumZoomScale
  - viewForZoomInScrollView()
- Closures 
  - Warning if a closure capture a pointer to something that has a pointer back to it, it creates a loop a memory cycle
  - Fix the problem by including [unowned self] in the closure  so the closure will not be keep self  in memory
-Multithreading
  - Is about queues 
  - Main Queue - very important queue - UI activity must happen on the main queue 
  - Dispatch_async(queue) - use this function to execute code on another queue 
  - Common way to implement multithreading is to execute code off of the main queue and then return to the main queue 
  - Dispatch_after() is used to do something in the future 
-Other Queues
  - QOS_CLASS_USER_INTERACTIVE 
  - QOS_CLASS_USER_INITIATED 
  - QOS_CLASS_UTILITY 
  - QOS_CLASS_BACKGROUND
