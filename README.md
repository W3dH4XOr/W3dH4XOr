- 👋 Hi, I’m @W3dH4XOr
- 👀 I’m interested in Programming....
- 🌱 I’m currently learning Web-KiT...
- 💞️ I’m looking to collaborate on Something ...
- 📫 How to reach me .......

<!---
W3dH4XOr/W3dH4XOr is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

import requests
import re

def commitCount(u, r):
	return re.search('\d+$', requests.get('https://api.github.com/repos/{}/{}/commits?per_page=1'.format(u, r)).links['last']['url']).group()

def latestCommitInfo(u, r):
	""" Get info about the latest commit of a GitHub repo """
	response = requests.get('https://api.github.com/repos/{}/{}/commits?per_page=1'.format(u, r))
	commit = response.json()[0]; commit['number'] = re.search('\d+$', response.links['last']['url']).group()
	return commit
