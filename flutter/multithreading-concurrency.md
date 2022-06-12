# When, why, and how to multithread in Flutter?

## Sometimes, a piece of code can block the UI from updating.

## Async vs Sync (Keeping the event loop running)

- All dart code runs in an `isolate`.
- Each isolate has its `private memory` an a single thread running an `event loop`.
- As new events happen, they are added to an event queue.
- For smoother rendering, Flutter sends `repaint` (UI update) event `request` to the `event queue`, 60 times a second.
- It is necessary for those `repaint requests` to be processed on time for smoother experience.
- `compute()` function can be used to offload the heavy processes. If there is any short-lived function which is computationally expensive, that function can be passed into `compute()` function for asynchronous processing.

## For those workloads or functions which are long lived.
- A separate worker isolate should be created.