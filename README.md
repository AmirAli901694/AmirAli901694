Import requests
from bs4 import BeautifulSoup

url = "https://www.digikala.com/product/dkp-123456"  https://www.digikala.com/product/dkp-13917628
response = requests.get(url)
soup = BeautifulSoup(response.content, 'html.parser')

title = soup.find('h1', {'class': 'c-product__title'}).text
print(title)
