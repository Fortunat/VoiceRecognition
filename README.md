# VoiceRecognition

#GET THE SENCE OF THE SENDING MESSAGE
curl \
   -H 'Authorization: Bearer O2UYDHYINQY6LL3RWLGKQAAISU3SVR3I' \
   'https://api.wit.ai/message?v=20161212&q=Bonjour%20Fortunat'

#GET THE RESPONSE OF THE BOT
curl -XGET "https://api.wit.ai/message?v=2016056&q=Quel%20temps%20fait-t-il%20aujourd'hui%20à%20Paris?"\
-H 'Authorization: Bearer O2UYDHYINQY6LL3RWLGKQAAISU3SVR3I'
