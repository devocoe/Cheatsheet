
#### Installation

```python
pip install beautifulsoup4
```

#### Import

```python
from bs4 import BeautifulSoup
```

#### Create soup

```python
soup = BeautifulSoup(html_content,"html.parser")
```

#### pretify the document 

```python
soup.prettify()
```

#### find first matching tag or element

```python
soup.find(a)
```

#### find all the matching tags or elements

```python
soup.find_all(a)
```

### get innertext of tag

```python
tag = soup.find(a)
tag.getText()
```

#### get attributes of tag

```python
tag = soup.find(a)
tag.get("href")
```

#### get innertext of tag

```python
tag = soup.find(a)
tag.getText()
```

#### match by more than one parameter

```python
tag = soup.find(name="p",id="single")
tags = soup.find_all(name="h3",class_="title")
```


#### select one tag by css selector

```python
tag = soup.select_one(".container p")
```

#### select all matching tag by css selector

```python
tags = soup.select(".container p")
```