Для создания base auth:  
```sudo apt-get install apache2-utils```  
```echo $(htpasswd -nbB <USER> "<PASS>") | sed -e s/\\$/\\$\\$/g```
