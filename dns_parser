from bs4 import BeautifulSoup
from lxml import html
import requests

url = 'https://www.dns-shop.ru/'
page = requests.get(url)
print(page)
print(page.text)
soup = BeautifulSoup(page.text, 'html.parser')
#print()

for a in soup.find_all('a', href=True):
    print ("Found the URL:", a['href'])


from urllib.request import urlopen, Request
headers = {'User-Agent': 'Mozilla/5.0 (Windows NT 6.1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/41.0.2228.0 Safari/537.3'}
reg_url = 'https://www.dns-shop.ru/catalog/17a8a69116404e77/myshi/'
req = Request(url=reg_url, headers=headers)
html = urlopen(req).read()
#print(html)
soup = BeautifulSoup(html, 'html.parser')
#print(soup.prettify())
images = soup.findAll('img')
for image in images:

    print (image['img'])
