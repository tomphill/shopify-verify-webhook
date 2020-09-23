# shopify-verify-webhook
```
const verifyWebhookIntegrity = require('shopify-verify-webhook');

function someHttpRequest(req){
  const isValid = verifyWebhookIntegrity(
    process.env.SHOPIFY_WEBHOOK_SIGNATURE, 
    req.body, req.headers['x-shopify-hmac-sha256']);
  
  if(isValid){
    // happy days
  }else {
    // this request did not originate from shopify
  }
}
```
