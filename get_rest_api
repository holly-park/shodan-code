#파이썬 기본 인코딩은 아스키 코드이다. 스크립트 파일이 아스키 코드일거라고 가정해서 파싱하려는데 그렇지 않은 경우 SyntaxError(문법에러)가 발생할 수 있다
#그럴 때 아래와 같이 # -*- coding: utf-8 -*- 를 한다
# -*- coding: utf-8 -*-

import json
import shodan
from shodan.cli.helpers import get_api_key
api_use = shodan.Shodan(get_api_key())   #리눅스 쉘에서 shodan  init으로 해온 api값을 가져오면 문자열이 아니어서 에러가 날 수 있다

api_use = ''   #이렇게 다시 바꿈


import requests
query = 'cctv country:"KR"'  #검색할 쿼리
URL = "https://api.shodan.io/shodan/host/search?key={api_use}&query={query}".format(api_use=api_use, query=query)
print(URL)  #url 이 잘 나오나 프린트 꼭 해볼 것



r = requests.get(URL)
print(r.status_code)  #확인 코드도 꼭 프린트 해볼 것
content = json.loads(r.text)

print(type(content))
print(content.keys())
