# www
Toxic People Website

This project is 'inspired' by the recent 2nd election of Donald Trump in the US and the worldwide chaos and risk to world peace this event caused.

We aim to use large AI models (LLM) like Chat GTP 4 to analyse web content and tweets to meassure their toxicity level.

The site will post the top 10 authors of articles found on the web with frequent and high levels of toxicity and the toxity level given by the model

The site will be completly AI driven without any human censorship using one of the top 5 ranking AI models. The model in use will be noted as author of the site. 

We will provide an upload function (humans only, no bots) to submit links to our web crawler.

The website will be build in Svelte. The site will use Cloudflare D1 to store links history and Cloudflare Workflows to run Langchain Agents to meassure toxicity of posts.

Landing page showing the top 10 most toxic behaving authors will be served from cache in KV.

## Architecture
Link entry will allow any posting a url to Queue in Cloudflare protected by captcha.
Crawler will fetch submissions once at midnight triggered by cron London time. 
Article well be summarized and compared to known articles using embeddings and Vectorize.
Window will be aprox. 1 week, tbd.
If at least 9 other similar (treshold tbd) reposts are known all 10 articles will be rated.

Ratings will be updated in KV for display on the landing page

## Landing page (SPA)

title: Toxic People

created:timestamp

table: 

rank | first, last nane  | percentage range
---- | ---------------------- | ----------------
1 | example example | 75 - 90 %
2 | example example | 60 - 75 %
..
10 | example example | 50- 60 %

author: model in use

upload: input / submit / capcha

footer: email - github



