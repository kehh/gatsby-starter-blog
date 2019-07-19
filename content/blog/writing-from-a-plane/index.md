---
title: Writing a blog post via git on a plane
date: "2019-07-19"
---

I'm currently sitting on a plane writing this blog post. The static site generator that I'm using (Gatsby) 
allows me to edit the post and preview the page at the same time.

In order to start creating a page I just need to create a directory with the name matching the URL slug that I want to use
and then create an `index.md` file inside it with a little bit of metadata at the top of us such as:

```yml
---
title: Writing a blog post via git on a plane
date: "2019-07-19"
---
```

Next I kick of the development mode of the site using:
```bash
yarn develop
# or
gatsby develop
```

Next comes the bit that I've always struggled with - writing the actual content of the post! But hey here we go. Once I've written a 
bit and I want to see how it looks on the page I just have to save the file and the file watcher simply reloads the preview page
(by default at `http://localhost:8000`).

Once I'm happy with the content or am at a logical breakpoint it's simply a matter of committing the new file and pushing it to my dev branch:

```
git checkout dev
git pull origin dev
# Write some content
git add content/blog/writing-from-a-plane
git commit -m 'Basic article skeleton for wiring on a plane blog post'
git push origin dev
```
Wait a couple of minutes till I get an email from amplify stating that the content is now live on the [dev version of this site](https://dev.kehan.kim) .

Now it's simply a matter of rinse and repeat until I'm happy. Finally I push the content live on the non password protected version of the site:

```bash
git checkout master
git pull #origin master
git pull origin dev
git push #-u origin master
```

Finally wait for the email saying the new versino of the site is now successfully deployed.