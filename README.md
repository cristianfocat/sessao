import requests
session=requests.session()
#print(session.cookies.get_dict())
#print('-'*50)
response=session.get("http://google.com")
print(session.cookies.get_dict())
print('-'*50)
result=[{'name':c.name, 'value':c.value, 'domain':c.path} for c in session.cookies]
print(result)
