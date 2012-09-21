<h1>Tango Card Service API</h1>
<h3>Incorporate the innovative Tango Card directly into your reward, loyalty, and engagement applications.</h3>
<h4>Update: 2012-09-20</h4>
===

# Table of Contents #
<ul>
    <li><a href="#introduction">Introduction</a>
        <ul>
            <li><a href="#tango_card_api">Tango Card API</a>
                <ul>
                    <li><a href="#tango_card_sdks">Tango Card SDKs</a></li>
                </ul>
            </li>
            <li><a href="#incorporate_tango_card">Incorporate the Tango Card</a></li>
            <li><a href="#open_account">Open Tango Card Account</a>
                <ul>
                    <li><a href="#open_account_register">Register</a></li>
                    <li><a href="#open_account_login">Login</a></li>
                    <li><a href="#open_account_add_funds">Add Funds</a></li>
                </ul>
            </li>
            <li><a href="#start_using">Start Using</a>
                <ul>
                    <li><a href="#start_using_purchase">Purchase and Distribution of Gift Cards</a></li>
                    <li><a href="#start_using_gift_cards">The Tango Card and other Retailer Brand Gift Cards</a></li>
                </ul>
            </li>
            <li><a href="#sdk_support">Tango Card API Support</a></li>
            <li><a href="#contact_us">Contact Us</a></li>
        </ul>
    </li>
    <li><a href="#tango_card_api_overview">Tango Card API Overview</a>
        <ul>
            <li><a href="#tango_card_service_requests">Tango Card Service Requests</a>
                <ul>
                    <li><a href="#http_post_request_body">HTTP POST Request Body</a></li>
                    <li><a href="#request_methods">Request Methods</a></li>
                    <li><a href="#response_body">Response Body</a></li>
                </ul>
            </li>
            <li><a href="#tango_card_service_api_endpoints">Tango Card Service API Endpoints</a></li>
            <li><a href="#tango_card_service_api_security">Tango Card Service API Security</a></li>
        </ul>
    </li>
    <li><a href="#tango_card_api_methods">Tango Card API Methods</a>
        <ul>
            <li><a href="#request_getavailablebalance">GetAvailableBalance</a>
                <ul>
                    <li><a href="#getavailablebalance_request_params">Request Parameters</a></li>
                    <li><a href="#getavailablebalance_response_types">Response Types</a></li>
                </ul>
            </li>
            <li><a href="#request_purchasecard">PurchaseCard</a>
                <ul>
                    <li><a href="#purchasecard_request_params">Request Parameters</a></li>
                    <li><a href="#purchasecard_response_types">Response Types</a></li>
                </ul>
            </li>
        </ul>
    </li>
    <li><a href="#failure_response_types">Failure Response Types</a>
        <ul>
            <li><a name="failure_response_sys_error" >SYS_ERROR</a></li>
            <li><a name="failure_response_inv_input" >INV_INPUT</a></li>
            <li><a name="failure_response_inv_credential" >INV_CREDENTIAL</a></li>
            <li><a name="failure_response_ins_inv" >INS_INV</a></li>
            <li><a name="failure_response_ins_funds" >INS_FUNDS</a></li>
        </ul>
    </li>
</ul>

<a name="introduction"></a>
# Introduction #

<a name="tango_card_api"></a>
## Tango Card Service API ##
Tango Card Service API is flexible, secure, and straightforward. It allows any server to purchase the Tango Card and is intended for users requiring high volume transactions and processes.

<a name="tango_card_sdks"></a>
### Tango Card SDKs ###
For those developers who do not wish to develop directly with our Tango Card API, there are several Tango Card SDKs currently available that use the Tango Card API:
<ul>
    <li><a href="https://github.com/tangocarddev/TangoCard_DotNet_SDK" target="_blank">Tango Card C#/.Net 4.0 SDK</a></li>
    <li><a href="https://github.com/tangocarddev/TangoCard_PHP_SDK" target="_blank">Tango Card PHP SDK</a></li>
    <li><a href="https://github.com/tangocarddev/TangoCard_Java_SDK" target="_blank">Tango Card Java SDK</a></li>
    <li><a href="https://github.com/tangocarddev/TangoCard_Ruby_SDK" target="_blank">Tango Card Ruby SDK</a></li>
</ul>

<a name="incorporate_tango_card"></a>
## Incorporate the Tango Card ##
The Tango Card Service API allows you to incorporate the innovative Tango Card directly into your reward, loyalty, and engagement applications.

Tango Card is the “exactly what you want” gift card and allows the recipient to use their value exactly how they want – they can select a premier gift card, they can divide their value among Brands, they can use some today and save the rest for another day. They can also donate to a non-profit organization. 

Tango Card value can be used via the web or from almost any mobile device. There are no fees or expiration dates of any kind. It’s great for the recipient, and even better for you because it is an entire gift card program delivered in one card allowing you to focus on your core business. 

Tango Card solutions are already used by Microsoft Bing, FedEx, Extole, Plink, beintoo, Lead Valu, Getty Images, and many others.

<a name="open_account"></a>
## Open Tango Card Account ##

In order to use the Tango Card API, it is required to open and fund a Tango Card account on https://www.tangocard.com

<a name="open_account_register"></a>
### Register ###

First, register to open a Tango Card account: <a href="https://www.tangocard.com/user/register" target="_blank">Register</a> 

The provided 'username (email address)' and 'password' will be the same as what will be used for authenticating usage of the Tango Card API's methods.

<a name="open_account_login"></a>
### Login ###

Second, to verify availability of your production account by using login: <a href="https://www.tangocard.com/user/login" target="_blank">Login</a>

<a name="open_account_add_funds"></a>
### Add Funds ###

Third, in order to purchase the Tango Card through the Tango Card API, there must be funds within your Tango Card account.

Fund your account here either by 'wire transfer', 'check', or 'credit card': <a href="https://www.tangocard.com/user/addfunds" target="_blank">Add Funds</a>

<a name="start_using"></a>
## Start Using ##

After opening and funding your Tango Card account, then you are ready to begin using the Tango Card API to access your account.

<a name="start_using_purchase"></a>
### Purchase and Distribution of Gift Cards ###
Through the Tango Card API you can purchase Tango Card gift cards with your choice of delivery:
<ul>
    <li>Have Tango Card service send gift cards directly to recipients via email which will include live gift card codes.</li>
    <li>You take the returned live gift card codes for you to customize and redistribute.</li>
</ul>

<a name="start_using_gift_cards"></a>
### The Tango Card and other Retailer Brand Gift Cards ###

The API is optimized for ordering the Tango Card, which has SKU of ```"tango-card"```.

If you have questions about potentially incorporating other brands or digital goods in your program please contact us at general@tangocard.com.

<a name="sdk_support"></a>
## Tango Card API Support ##
If you have any questions with the Tango Card API, please contact us at sdk@tangocard.com.

<a name="contact_us"></a>
## Contact Us ##
To learn more about Tango Card integration solutions, call 1.877.55.TANGO.

<a name="tango_card_api_overview"></a>
# Tango Card Service API Overview #

<a name="tango_card_api_requests"></a>
## Tango Card Service API Requests ##

With the Tango Card API, every request has a corresponding success-case response object. There are also several failure-case response objects which are shared between calls. The specifics of the request and response objects will be described in <a href="#tango_card_api_methods">Tango Card API Methods</a>.

<a name="http_post_request_body"></a>
### HTTP POST Request Body ###
All requests are via JSON-encoded objects as the payload of a HTTP POST call on a specified method. As an example, if the input listed below was "sku" then the POST body might look like:

```json
{"sku":"tango-card"}
```

Note, however that since this is an HTTP POST that this should be <a href="http://en.wikipedia.org/wiki/Percent-encoding">"percent-encoded"</a>, as normal, so the actual body might actually look more like:

```text
%7B%22sku%22%3A%22tango-card%22%7D
```

<a name="request_methods"></a>
### Request Methods ###

The available request methods through our API endpoints are:
<dl>
    <dt>GetAvailableBalance</dt>
    <dd>Request the available balance to the user whose authentication was supplied..</dd>
    <dt>PurchaseCard</dt>
    <dd>Purchase Tango Cards from account funded by user.</dd>
</dl>

<a name="response_body"></a>
### Response Body ###

All responses are a JSON-encoded object with the format of:

<dl>
    <dt>"responseType":</dt
    <dd>STRING</dd>
    <dt>"response":<dt>
    <dd>JSON OBJECT</dd>
</dl>
  
The value of "responseType" will influence the format of the object in response. For "responseType" of "SUCCESS", then the "response" will provide a JSON-encoded object with requested data. For other "responseType" cases are considered failure response and are detailed within section below <a href="#failure_response_types">Failure Response Types</a>.

<a name="tango_card_service_api_endpoints"></a>
## Tango Card Service API Endpoints ##

Available are two endpoints that provide the Tango Card Service API:
<dl>
    <dt><code>INTEGRATION</code></dt> 
    <dd>
        <ul>
            <li>Expected to be used for development and testing purposes.</li>
            <li><b>Important:</b> Purchases from this endpoint will: 
                <ul>
                    <li>Use funds from our test account.</li>
                    <li>Send real emails (with fake codes), so only use recipient email addresses you control for testing purposes.</li>
                </ul>
            </li>
            <li>Secure Endpoint URL: <code>https://int.tangocard.com/Version2</code></li>
            <li>Login to use our testing account through this endpoint is:
                <dl>
                    <dt>Username:</dt>
                    <dd>third_party_int@tangocard.com</dd>
                    <dt>Password:</dt>
                    <dd>integrateme</dd>
                </dl>
            </li>
        </ul>
    </dd>
    <dt><code>PRODUCTION</code></dt>
    <dd>
        <ul>
            <li>Performs actual card purchase requests.</li>
            <li><b>Important:</b> Purchases from this endpoint will: 
                <ul>
                    <li>Use funds from <b>your Tango Card account</b>!</li>
                    <li>Send real emails (with live codes), only use recipient email addresses you wish to deliver to.</li>
                </ul>
            </li>
            <li>Endpoint URL: <code>https://api.tangocard.com/Version2</code></li>
            <li>Login to use your production account through this endpoint is:
                <dl>
                    <dt>Username:</dt>
                    <dd>Your Tango Card account's username (email address)</dd>
                    <dt>Password:</dt>
                    <dd>Your Tango Card account's password</dd>
                </dl>
            </li>
        </ul>
    </dd>
</dl>

<a name="tango_card_service_api_security"></a>
## Tango Card Service API Security ##

Tango Card Service API Requests are performed using secure HTTP POST via <a href="http://en.wikipedia.org/wiki/Transport_Layer_Security" target="_blank">"TLS/SSL"</a>.

The use of SSL allows for securely transmitting data and prevents <a href="http://en.wikipedia.org/wiki/Man-in-the-middle_attack" target="_blank">man-in-the-middle attacks</a>.

The lack of sessions and the inability to communicate with the API over HTTP prevents <a href="http://en.wikipedia.org/wiki/Session_hijacking" target="_blank">session hijacking</a> and <a href="http://en.wikipedia.org/wiki/Cross-site_request_forgery" target="_blank">cross-site request forgery</a>.

<a name="tango_card_api_methods"></a>
# Tango Card API Methods #

<a name="request_getavailablebalance"></a> 
## GetAvailableBalance ##

<dl>
    <dt>Description</dt>
    <dd>Request the available balance to the user whose authentication was supplied.</dd>
</dl>

<a name="getavailablebalance_request_params"></a>
### Request Parameters ###
<dl>
    <dt>username</dt>
    <dd>https://www.tangocard.com user account's username</dd>
    <dt>password</dt>
    <dd>https://www.tangocard.com user account's password</dd>
</dl>

#### Example `HTTP POST` Request ####

```http
POST https://int.tangocard.com/Version2/GetAvailableBalance HTTP/1.1
Content-Type: application/json
Host: int.tangocard.com
Content-Length: 69
Expect: 100-continue
Connection: Keep-Alive

{
    "username":"third_party_int@tangocard.com",
    "password":"integrateme"
}
```

<a name="getavailablebalance_response_types"></a>
### Response Types ###

<dt>Success Response Type:</dt>
    <dd>
        <dl>
            <dt>SUCCESS</dt>
            <dd>JSON Object:
                <dl>
                    <dt>availableBalance</dt>
                    <dd>integer - The balance available to the user in cents (100 = $1.00).
                    </dd>
                </dl>
            </dd>
        </dl>
    </dd>
    <dt>Failure Response Types:</dt>
    <dd>See details for each within next section.
        <dl>
            <dt><a name="failure_response_inv_credential" ><code>INV_CREDENTIAL</code></a></dt>
            <dt><a name="failure_response_sys_error" ><code>SYS_ERROR</code></a></dt>
        </dl>
    </dd>
</dl>

#### Example `SUCCESS` Response Type ####

```http
HTTP/1.1 200 OK
Date: Fri, 21 Sep 2012 04:42:56 GMT
Server: Apache/2.2.22 (Ubuntu)
X-Powered-By: PHP/5.3.10-1ubuntu3.3
Access-Control-Allow-Origin: *
Content-Length: 68
Connection: close
Content-Type: application/json

{
    "responseType":"SUCCESS",
    "response":
        {
            "availableBalance":873486842
        }
}
```

<a name="request_purchasecard"></a>
## PurchaseCard ##

<dl>
    <dt>Description</dt>
    <dd>Purchase a single card to be delivered as described.</dd>
</dl>

<a name="purchasecard_request_params"></a>
### Request Parameters ###
<dl>
    <dt>username</dt>
    <dd>https://www.tangocard.com user account's username</dd>
    <dt>password</dt>
    <dd>https://www.tangocard.com user account's password</dd>
    <dt>cardSku</dt>
    <dd>string - The SKU of the card to purchase. The SKU for the Tango Card is "tango-card". For other SKUs, please refer to this section: <a href="#start_using_gift_cards">The Tango Card and other Retailer Brand Gift Cards</a></dd>
    <dt>cardValue</dt>
    <dd>integer - The value of the card to purchase in cents (100 = $1.00).</dd>
    <dt>tcSend</dt>
    <dd>boolean - Whether Tango Card will send the email to the user.</dd>
    <dt>recipientName</dt>
    <dd>string (length 1 - 255, required if tcSend=true) - The name of the person receiving the card.</dd>
    <dt>recipientEmail</dt>
    <dd>string (length 3 - 255, required if tcSend=true) - The email address of the person receiving the card.</dd>
    <dt>giftMessage</dt>
    <dd>string (length 1 - 255, required if tcSend=true) - A message from the sender of the card to the recipient. May be null, but must exist if tcSend = true.</dd>
    <dt>giftFrom</dt>
    <dd>string (length 1 - 255, required if tcSend=true) - The name of the person sending the card.</dd>
</dl>

#### Example `HTTP POST` Request ####

```http
POST https://int.tangocard.com/Version2/PurchaseCard HTTP/1.1
Content-Type: application/json
Host: int.tangocard.com
Content-Length: 201
Expect: 100-continue

{
    "cardSku":"tango-card",
    "cardValue":100,
    "tcSend":false,
    "recipientName":null,
    "recipientEmail":null,
    "giftMessage":null,
    "giftFrom":null,
    "username":"third_party_int@tangocard.com",
    "password":"integrateme"
}
```

<a name="purchasecard_response_types"></a>
### Response Types ###

<dl>
    <dt>Success Response Type:</dt>
    <dd>
        <dl>
            <dt>SUCCESS</dt>
            <dd>JSON Object:
                <dl>
                    <dt>referenceOrderId</dt>
                    <dd>string - A unique token that we can use to look up the order.</dd>
                    <dt>cardToken</dt>
                    <dd>string - A unique token that we can use to look up the card.</dd>
                    <dt>cardNumber</dt>
                    <dd>string - The card’s "number".</dd>
                    <dt>cardPin</dt>
                    <dd>string - The card’s "pin", may be null.</dd>
                </dl>
            </dd>
        </dl>
    </dd>
    <dt>Failure Response Types:</dt>
    <dd>See details for each within next section.
        <dl>
            <dt><a name="failure_response_inv_credential" ><code>INV_CREDENTIAL</code></a></dt>
            <dt><a name="failure_response_inv_input" ><code>INV_INPUT</code></a></dt>
            <dt><a name="failure_response_ins_inv" ><code>INS_INV</code></a></dt>
            <dt><a name="failure_response_ins_funds" ><code>INS_FUNDS</code></a></dt>
            <dt><a name="failure_response_sys_error" ><code>SYS_ERROR</code></a></dt>
        </dl>
    </dd>
</dl>


### Example `SUCCESS` Response Type ###

```http
HTTP/1.1 200 OK
Date: Fri, 21 Sep 2012 04:42:57 GMT
Server: Apache/2.2.22 (Ubuntu)
X-Powered-By: PHP/5.3.10-1ubuntu3.3
Access-Control-Allow-Origin: *
Content-Length: 172
Connection: close
Content-Type: application/json

{
    "responseType":"SUCCESS",
    "response":
        {
            "referenceOrderId":"112-09213864-21",
            "cardToken":"505bf051296370.96220841",
            "cardNumber":"7001-7040-0119-6557-815",
            "cardPin":"157228"
        }
}
```

<a name="failure_response_types" ></a>
# Failure Response Types #

Here are the following expected failure response types that can be returned from Tango Card API endpoint.

<a name="failure_response_sys_error" ></a>
### `SYS_ERROR` ###

An error happened on our end. The call may may be re-tried, however if the error persists please contact us.

<dl>
    <dt>errorCode<dt>
    <dd>string - An internal error code that we can use to track down where the error occurred.</dd>
</dl>

#### Example `SYS_ERROR` Response Type ####

```http
HTTP/1.1 200 OK
Date: Fri, 21 Sep 2012 05:34:08 GMT
Server: Apache/2.2.22 (Ubuntu)
X-Powered-By: PHP/5.3.10-1ubuntu3.3
Access-Control-Allow-Origin: *
Content-Length: 65
Connection: close
Content-Type: application/json

{
    "responseType":"SYS_ERROR",
    "response":
        {
            "errorCode":"TPC:PC:35"
        }
}
```
    
<a name="failure_response_inv_input" ></a>
### `INV_INPUT` ###

One (or more) of the supplied inputs didn’t meet the requirements. The request should be altered before resubmitting.

<dl>
    <dt>invalid<dt>
    <dd>JSON object - The object’s properties are the name of the invalid field, the value of the property is description of the associated problem.</dd>
</dl>

#### Example `INV_INPUT` Response Type ####

```http
HTTP/1.1 200 OK
Date: Fri, 21 Sep 2012 05:07:19 GMT
Server: Apache/2.2.22 (Ubuntu)
X-Powered-By: PHP/5.3.10-1ubuntu3.3
Access-Control-Allow-Origin: *
Content-Length: 98
Connection: close
Content-Type: application/json

{
    "responseType":"INV_INPUT",
    "response":
        {
            "invalid":
            {
                "cardSku":"SKU does not appear to be valid."
            }
        }
}
```
    
<a name="failure_response_inv_credential" ></a>
### `INV_CREDENTIAL` ###

The credential was either missing, or something was wrong with it. The request should be altered before resubmitting.

<dl>
    <dt>message<dt>
    <dd>string - A description of what appeared to be wrong with the supplied credential.</dd>
</dl>

#### Example `INV_CREDENTIAL` Response Type ####

<dl>
    <dt><code>TCP:PNPA:3</code></dt>
    <dd>Provided user credentials are not valid.</dd>
</dl>

```http
HTTP/1.1 200 OK
Date: Fri, 21 Sep 2012 05:07:17 GMT
Server: Apache/2.2.22 (Ubuntu)
X-Powered-By: PHP/5.3.10-1ubuntu3.3
Access-Control-Allow-Origin: *
Content-Length: 69
Connection: close
Content-Type: application/json

{   "responseType":"INV_CREDENTIAL",
    "response":
        {
            "message":"TCP:PNPA:3"
        }
}
```
    
<a name="failure_response_ins_inv" ></a>
### `INS_INV` ###

We don’t have enough available inventory to fulfill the request. The request should be altered before resubmitting.

<dl>
    <dt>sku<dt>
    <dd>string - The SKU that we couldn’t fulfill.</dd>
    <dt>value<dt>
    <dd>integer - The value that we couldn’t fulfill.</dd>
</dl>
    
<a name="failure_response_ins_funds" ></a>
### `INS_FUNDS` ###

The account associated with the authenticated user doesn’t have enough available balance to cover the cost of the purchase.

<dl>
    <dt>availableBalance<dt>
    <dd>integer - The balance currently available in cents (100 = $1.00).</dd>
    <dt>orderCost<dt>
    <dd>integer - The amount the order would cost to complete in cents (100 = $1.00).</dd>
</dl>

#### Example `INS_FUNDS` Response Type ####

```http
HTTP/1.1 200 OK
Date: Fri, 21 Sep 2012 05:07:18 GMT
Server: Apache/2.2.22 (Ubuntu)
X-Powered-By: PHP/5.3.10-1ubuntu3.3
Access-Control-Allow-Origin: *
Content-Length: 78
Connection: close
Content-Type: application/json

{
    "responseType":"INS_FUNDS",
    "response":
        {
            "availableBalance":0,
            "orderCost":100
        }
}
```

