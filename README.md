# VoiceRecognition

#GET THE SENCE OF THE SENDING MESSAGE
curl \
   -H 'Authorization: Bearer O2UYDHYINQY6LL3RWLGKQAAISU3SVR3I' \
   'https://api.wit.ai/message?v=20161212&q=Bonjour%20Fortunat'
   
Response:
{
  "msg_id" : "bc8f9919-45f2-427e-8996-8693f6442b6e",
  "_text" : "Bonjour Fortunat",
  "entities" : {
    "contact" : [ {
      "confidence" : 0.9798607592679585,
      "type" : "value",
      "value" : "Fortunat",
      "suggested" : true
    } ],
    "intent" : [ {
      "confidence" : 0.9933277077988402,
      "value" : "salutation"
    } ]
  }
}

#GET THE RESPONSE OF THE BOT
curl -XGET "https://api.wit.ai/message?v=2016056&q=Quel%20temps%20fait-t-il%20aujourd'hui%20à%20Paris?"\
-H 'Authorization: Bearer O2UYDHYINQY6LL3RWLGKQAAISU3SVR3I'

Response:
{
  "msg_id" : "3c69ab37-ba31-4c4a-8f35-005b356c4778",
  "_text" : "Quel temps fait-t-il aujourd'hui ￃﾠ Paris?",
  "entities" : {
    "date" : [ {
      "confidence" : 0.9287822791473954,
      "type" : "value",
      "value" : "aujourd'hui "
    } ],
    "location" : [ {
      "confidence" : 0.9740309001423672,
      "type" : "value",
      "value" : "Paris",
      "suggested" : true
    } ],
    "intent" : [ {
      "confidence" : 0.9931502275885096,
      "value" : "meteo"
    } ]
  }

#GET ALL THE ENTITIES OF THE APP
curl -XGET 'https://api.wit.ai/entities?v=20160526' \
-H 'Authorization: Bearer O2UYDHYINQY6LL3RWLGKQAAISU3SVR3I'

Response:
[ "wit$number", "wit$location", "wit$quantity", "wit$email", "wit$agenda_entry", "wit$duration", "wit$local_search_query", "wit$on_off", "wit$datetime", "wit$contact", "wit$message_body", "wit$reminder", "wit$distance", "wit$wdatetime", "wit$wikipedia_search_query", "wit$amount_of_money", "wit$ordinal", "wit$message_subject", "wit$wolfram_search_query", "wit$url", "wit$math_expression", "wit$phone_number", "wit$temperature", "wit$search_query", "wit$phrase_to_translate", "wit$age_of_person", "intent", "date" ]
