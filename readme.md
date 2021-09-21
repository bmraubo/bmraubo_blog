I decided to use Hexo because it was based on Node.Js and focused on blogging which is the purpose of this. Initially, I used the JamStack button to circumvent the whole `hero init` process, but that left me in a pretty poor position where I had a template blog set up and linked to a GitHub repo, but had no idea how any of it worked. 

I deleted the repo and the site and started again using the helpful [Netlify step-by-step guide](#https://www.netlify.com/blog/2015/10/26/a-step-by-step-guide-hexo-on-netlify/). After some permissions errors that were resolved by getting a bit more familiar with nvm (on Linux I would have sudo’d my way around this, but this was not advised), I managed to get a boilerplate blog and repo set up manually.

I created a test post using `hexo new post` in Terminal, and pushed it to the repo. All working - the build process is automatic so I am taking some time reading through the deployment logs trying to understand what is going on behind the scenes.

Next step: mess around with themes - went from [Frame](#https://frame.zhangyongqi.com/) because of its simplicity. 