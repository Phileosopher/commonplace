
## 00 TT Torrent - How To Proxy 'Any' Website Using Cloudflare Workers

  1. _Sign_ up on <https://www.cloudflare.com/> if not already.
  2. _Click_ on workers tab.
  3. _Choose_ a subdomain where you would like to see your workers.
such as [zyx.subdomain.workers.dev](http://zyx.subdomain.workers.dev)
here zyx will be replaced by your future worker names.
the subdomain will stay same
  4. _After_ selecting subdomain click on create a service/worker.
  5. _Name_ your new worker anything you want.
  6. _Click_ create.
  7. _Click_ quick edit.
  8. _Click_ next.
  9. _Delete_ existing code.
  10. _Paste_ the following code there.

   async function handleRequest(request) {
  const url = new URL(request.url)
  if (url.hostname in ORIGINS) {
const target = ORIGINS[url.hostname]
url.hostname = target
return fetch(url.toString(), request)
  }
  return fetch(request)
}
addEventListener('fetch', event => {
  event.respondWith(handleRequest(event.request))
})
const ORIGINS = {
  '1337x.subdomain.workers.dev': '1337x.to'
}

> Replace 1337x with whatever you named your new worker.
>
> Replace [1337x.to](http://1337x.to) with the website you want to be proxied.
>
> Don't enter <https://1337x.to/>
>
> Only [1337x.to](http://1337x.to)
>
>
>

   BOOM you can access your proxied website at [1337x.subdomain.workers.dev](http://1337x.subdomain.workers.dev)

Enjoy and cheers!

Not all websites can be proxied. Either because the websites don't want to be proxied or because can't be proxied through cloudflare workers or because cloudflare itself doesn't support them.

Leaving some sample workers. Feel free to use them.

<https://1337x.unban.workers.dev>

<https://scrolller.unban.workers.dev>
