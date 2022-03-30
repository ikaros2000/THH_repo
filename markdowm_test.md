
##school of Computer Science and Technology, Jilin University
##This is a simple practice to get started with markdown

##1. Title

##h2

####h4

##2. Code block

```pycon
#python code example
def getContent(url, name):
    headers = {"User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:77.0) Gecko/20100101 Firefox/77.0"}
    response = requests.get(url=url, headers=headers)
    response.encoding = 'utf-8'
    time.sleep(1)
    code = response.text
    tree = etree.HTML(code)
    chap = tree.xpath('//div[@class="bookname"]/h1/text()')[0]
    content = tree.xpath('//div[@id="content"]/text()')
    with open('Novels/' + name + '.txt', 'a+', encoding='utf-8') as file:
        print("start crawling:" + chap)
        file.write(chap + '\n\n')
        for i in content:
            text = str(i)
            text = text.replace('\xa0','')
            text = text.strip()
            file.write(text)
        file.write("\n\n")
        file.close()
```

```shell
//shell script example
//Start command of spring project under linux
java -jar blog start
```

##3. Font

###**bolded text**

###~~strikethrough text~~

###*italicized text*

##4. Quote

> primary quote
>> secondary quote
>>> tertiary quote

##5. Dividing line

---

***

##6. Image insertion

![image 1](logo.png)

![image 2](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fnimg.ws.126.net%2F%3Furl%3Dhttp%253A%252F%252Fdingyue.ws.126.net%252F2021%252F0911%252Fd6c3858fj00qz8re6003vc000b4007rg.jpg%26thumbnail%3D650x2147483647%26quality%3D80%26type%3Djpg&refer=http%3A%2F%2Fnimg.ws.126.net&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651225144&t=99b3f0696e72145e66752aff693754cc)

##7. Link

####Hyperlink

[my github](https://github.com/ikaros2000/THH_repo)

[baidu](https://www.baidu.com/)

####Interpage links

[readme.md](readme.md)

##8. list

####a bulleted list

- line 1
- line 2
- line 3

####a numbered list
1. line 1
2. line 2
3. line 3

##9.table

|  subject   | grade  |
| :-----:| :----: | 
| Maths  | 100 |
| English  | 90 |



