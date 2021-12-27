# smrtthings-braviaTV

Curl Command to test:

    curl -i -H "X-Auth-PSK: Sonypsk" -d '{"method": "getSystemInformation","id": 1,"params": [],"version": "1.0"}' http://10.10.200.32/sony/system


References:
    
    https://gist.github.com/kalleth/e10e8f3b8b7cb1bac21463b0073a65fb
    https://pro-bravia.sony.net/develop/integrate/rest-api/spec/getting-started/


Instead of using display_control.html, you can easily send the REST API command by the following JavaScript sample using Google Chrome Developer Tools - Console.

    var xhr = new XMLHttpRequest();
    xhr.open('POST', 'http://192.168.0.1/sony/avContent');
    xhr.setRequestHeader('X-Auth-PSK', '1234');
    xhr.send(JSON.stringify(
    {method: "setPlayContent",
      version: "1.0",
      id: 1,
      params: [{uri: "extInput:hdmi?port=2"}]}
    ));

