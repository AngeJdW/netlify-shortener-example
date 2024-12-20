# Purpose of this repository
The purpose of this repository is to store the code required to run the URL Shortener application. 

# About this application
This application has two fundamental fucntions. 
 - A _redirects file which is used to redirect shortened strings to a url. 
 - Github code so that this redirects file can be edited and changed, pushing to Netlify with simple github commands. 

# Further information about this application
This application uses the _redirects file within netlify to creeate a URL Shortener. 
Each line in th _redirects file has a "/<shortname> <URL>"
When using Github, updating this document will update the _redirects file which is used for** ajdw-short-url.netlify.app/<shortname> 

For exmaple, uploading the _redirects file with **
/cnet www.cnet.com
Means that if you type into the URL space on a browsser ajdw-short-url.netlify.app/cnet,  www.cnet.com will be returned. **

Further to this very basic page, you can update this _redirects file easier with npm commands. 
netlify-shortner under MIT license enables you to do the following: **

npm run shorten # **simply formats your _redirects file**
npm run shorten https://yahoo.com # **generates a short code and adds it for you**
npm run shorten https://github.com gh # **adds gh as a short URL for you**

The netlify-shortener does a few things:
generates a short code if one is not provided
validates your URL is a real URL
adds the URL to the top of _redirects
runs a git commit and push (this will trigger netlify to deploy your new redirect)
Copies the short URL to your clipboard
Netlify's deploys are normally fast enough that the new URL should be deployed by the time you've shared it to someone.**
