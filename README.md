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
	return re.search('\d+$', requests.get('https://api.github.com/
