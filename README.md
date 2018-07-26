# Logging best practice in Ruby
It's opionated stuff but it was from my practice.

1. Write logs in json format it will help you to easy transform it and process in ElasticSearch or in something similar
2. Add time key into json logs it also can help you to process logs in Kibana and app event can be differ from time when log was save espessially when you use centralized storage for logs
3. Seaparate logs by type it's not about sevrerity but about physical storage like _bussines events_, _logs for yourself_, _tech logs(standard rails log, gem logs)_ 
4. Add _Trace Id_ (SecureRandom.hash or something else) to log entity it helps you to use tools like [Zipkin](https://github.com/openzipkin/zipkin) to trace issues from distributed system if you have microservices
5. Write logs through you custom singleton class it give you more fine control instead of using standard Rails logger

its opionated you might not agree with that but if so let me know. Its fine to disagree with someone.

Usefull links:

[https://github.com/rocketjob/semantic_logger](https://github.com/rocketjob/semantic_logger) - logger

[https://github.com/vsevolod/xyeger](https://github.com/vsevolod/xyeger) - logger

[https://github.com/roidrage/lograge](https://github.com/roidrage/lograge) - logger
