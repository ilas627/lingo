[Qwen_javascript_20261104_42pv1kj1m.js](https://github.com/user-attachments/files/34368259/Qwen_javascript_20261104_42pv1kj1m.js)
const CACHE_NAME = 'lingoschool-v2';
self.addEventListener('install', event => { self.skipWaiting(); });
self.addEventListener('fetch', event => {
  event.respondWith(
    caches.match(event.request).then(response => response || fetch(event.request))
  );
});
