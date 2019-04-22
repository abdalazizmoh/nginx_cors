# nginx_cors
#To build the image for testing
docker build . -t nginx_cors
# To run images just build it
docker run -d --name test -p 80:80 nginx_cors
#for test the cors
curl -H "Origin: https://demo.com" -H "Access-Control-Request-Method: GET" -X OPTIONS --verbose "http://localhost/ico-whitelabels-de.woff?v=1.4&h=4a7010798c0bb9d1"
