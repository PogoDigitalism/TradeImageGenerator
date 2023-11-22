# Allows for Pillow image generation in an asynchronous environment without blocking the event loop. ⭐


## how to do it:
(check for async_example.py for a pseudo code showcase of how it works)

- Instance a ThreadPoolExecutor()
- Create an AsyncIO task (If you dont want your async function to (asynchronously) yield until the image has been generated)
- Get the current event loop
- await loop.run_in_executor and pass your threadpoolexecutor, (synchronous) image generator function and image configs here
