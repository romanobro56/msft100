# msft100

Offline tracker for a 100-problem Microsoft SWE 1 / IC2 LeetCode path, plus a Refresh 50 track at the bottom: the 50 most important problems you've already solved, to re-solve from scratch. Open `microsoft-100.html` in Chrome from this folder.

## Syncing progress between devices

Progress lives in `progress.json`. The page writes to it directly once it's linked.

1. On each device, open the page and click **Link progress.json** once, then pick this repo's `progress.json`. If Chrome later shows **Reconnect progress.json**, click it to allow writing again.
2. When you finish a session: `git commit -am "progress" && git push`.
3. Before a session on another device: `git pull`, then reload the page (a tab left open from before the pull still runs the old page code). The newer of the browser's copy and `progress.json` wins.

Don't edit progress on two devices without pushing and pulling in between: the newer copy replaces the older one as a whole, it doesn't merge them.
