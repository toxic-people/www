# www
Toxic People Website

This project is 'inspired' by the recent 2nd election of Donald Trump in the US.

We aim to use AI models like Chat GTP to analyse web content and tweets to meassure their toxicity level.

The site will post the top 10 authors of articles found on the web with frequent and high levels of toxicity.

The site will be completly AI driven without any humen censorship using one of the top 5 ranking AI models.

We will provide an upload function to submit links to our web crawler.

The website will be build in Svelte. The site will use Cloudflare D1 to store links history and Cloudflare Workflows to run Langchain Agents to meassure toxicity of posts.

Result showing the 10 most toxic behaving authors will be served from cache in KV.
