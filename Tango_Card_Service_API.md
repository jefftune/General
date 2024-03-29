<h1>Tango Card Service API</h1>
<h3>Incorporate the innovative Tango Card directly into your reward, loyalty, and engagement applications.</h3>
<h4>Update: Updated: 2013-June-15</h4>
===

Tango Card Service API is depracating in favor of the Tango Card Rewards-as-a-Service (RaaS™) API. More information about the RaaS&trade; API can be found at https://github.com/tangocarddev/RaaS/blob/master/README.md

Please contact sdk@tangocard.com for access to Sandbox and Production environment, as well as general help regarding the RaaS&trade; API.

<!--
# Table of Contents #
<ul>
    <li><a href="#introduction">Introduction</a>
        <ul>
            <li><a href="#tango_card_api">Tango Card Service API</a>
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
        </ul>
    </li>
    <li><a href="#puchasing_options">Understanding Gift Card Purchasing Options</a>
        <ul>
            <li><a href="#puchasing_options_distribution">Distribution of Gift Cards</a></li>
            <li><a href="#puchasing_options_skus">The Tango Card and other Retailer Brand Gift Cards</a></li>
            <li><a href="#puchasing_options_denominations">Gift Card Denominations</a></li>
            <li><a href="#puchasing_options_templates">The Tango Card and custom Company Email Templates</a></li>
        </ul>
    </li>
    <li><a href="#sdk_support">Tango Card SDKs and Service API Support</a>
        <ul>
            <li><a href="#sdk_support_resolve">Resolving Issues</a>
                <ul>
                    <li><a href="#sdk_support_resolve_fiddler_2">Fiddler 2</a></li>
                    <li><a href="#sdk_support_resolve_tc_diagnostic_tool">Tango Card Service API Diagnostic Tool</a></li>
                </ul>
            </li>
        </ul>
    </li>
    <li><a href="#tango_card_api_overview">Tango Card Service API Overview</a>
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
    <li><a href="#tango_card_api_methods">Tango Card Service API Methods</a>
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
    <li><a href="#license">License</a></li>
    <li><a href="#contact_us">Contact Us</a></li>
</ul>

<a name="introduction"></a>
# Introduction #

<a name="tango_card_api"></a>
## Tango Card Service API ##
The `Tango Card Service API` provides a flexible, secure, and straight forward solution for integrating into reward, loyalty, and engagement applications for purchasing the Tango Card from their funded Tango Card account on https://www.tangocard.com. 

<a name="tango_card_sdks"></a>
### Tango Card SDKs ###
For those developers who do not wish to develop directly with our Tango Card Service API, there are several `Tango Card SDKs` currently available that use the Tango Card Service API:
<ul>
    <li><a href="https://github.com/tangocarddev/TangoCard_DotNet_SDK" target="_blank">Tango Card C#/.Net 4.0 SDK</a></li>
    <li><a href="https://github.com/tangocarddev/TangoCard_PHP_SDK" target="_blank">Tango Card PHP SDK</a></li>
    <li><a href="https://github.com/tangocarddev/TangoCard_Java_SDK" target="_blank">Tango Card Java SDK</a></li>
    <li><a href="https://github.com/tangocarddev/TangoCard_Ruby_SDK" target="_blank">Tango Card Ruby SDK</a></li>
    <li><a href="https://github.com/tangocarddev/TangoCard_jQuery_Plugin" target="_blank">Tango Card jQuery Plugin</a></li>
</ul>

<a name="incorporate_tango_card"></a>
## Incorporate the Tango Card ##
The Tango Card Service API allows you to incorporate the innovative Tango Card directly into your reward, loyalty, and engagement applications.

Tango Card is the "exactly what you want" gift card and allows the recipient to use their value exactly how they want � they can select a premier gift card, they can divide their value among Brands, they can use some today and save the rest for another day. They can also donate to a non-profit organization. 

Tango Card value can be used via the web or from almost any mobile device. There are no fees or expiration dates of any kind. It's great for the recipient, and even better for you because it is an entire gift card program delivered in one card allowing you to focus on your core business.

Tango Card solutions are already used by Microsoft Bing, FedEx, Extole, Plink, beintoo, Lead Valu, Getty Images, and many others.

<a name="open_account"></a>
## Open Tango Card Account ##

In order to use the Tango Card Service API, it is required to open and fund a Tango Card account on https://www.tangocard.com

<a name="open_account_register"></a>
### Register ###

First, register to open a Tango Card account: <a href="https://www.tangocard.com/user/register" target="_blank">Register</a> 

The provided 'username (email address)' and 'password' will be the same as what will be used for authenticating usage of the Tango Card Service API's methods.

<a name="open_account_login"></a>
### Login ###

Second, to verify availability of your production account by using login: <a href="https://www.tangocard.com/user/login" target="_blank">Login</a>

<a name="open_account_add_funds"></a>
### Add Funds ###

Third, in order to purchase the Tango Card through the Tango Card Service API, there must be funds within your Tango Card account.

Fund your account here either by 'wire transfer', 'check', or 'credit card': <a href="https://www.tangocard.com/user/addfunds" target="_blank">Add Funds</a>

<a name="puchasing_options"></a>
# Understanding Gift Card Purchasing Options #

After opening and funding your Tango Card account, then you are ready to begin using the Tango Card Service API to access your account for getting available balance and for purchasing gift cards.

When you are ready to purchase a card, the Tango Card Service API has several options:

<dl>
    <dt>
    <a name="puchasing_options_distribution"></a>
    Distribution of Digital Gift Cards - parameter <code>tcSend</code> - boolean - <b>required</b></dt>
    <dd>
        Through the Tango Card Service API you can purchase Tango Card gift cards with your choice of delivery:
        <ul>
            <li><code>tcSend = true</code> - Have Tango Card service send gift cards directly to recipients via email which will include live gift card codes.</li>
            <li><code>tcSend = false</code> - You take the returned live gift card codes for you to customize and redistribute.</li>
        </ul>
    </dd>
    
    <dt>
    <a name="puchasing_options_skus"></a>
    The Tango Card and other Retailer Brand Gift Cards SKUs - parameter <code>cardSKU</code> - string - <b>required</b></dt>
    <dd>The API is optimized for ordering the Tango Card, which is SKU <code>"tango-card"</code>.

    <br>If you have questions about potentially incorporating other brands or digital goods in your program, then please do contact us at <a href="mailto:sdk@tangocard.com?Subject=Tango Card Service API Question">sdk@tangocard.com</a>. We will respond to inquiries within one business day.
    </dd>
    
    <dt>
    <a name="puchasing_options_denominations"></a>
    Gift Card Denominations - parameter <code>cardValue</code> - integer - <b>required</b></dt>
    <dd>Each gift card SKU has it own allowed set of denominations that can to assigned to parameter <code>cardValue</code>.
    <br/>For SKU <code>"tango-card"</code>, the available denomination in cents starting at <code>1 cents</code> ($0.01) to a maximum of user's available account balance (in cents).
    <br/>To find out about other available denominations for potentially incorporating other SKUs that can be assigned to parameter <code>cardValue</code>, then please do contact us at <a href="mailto:sdk@tangocard.com?Subject=Tango Card Service API Question">sdk@tangocard.com</a>. We will respond to inquiries within one business day.
    </dd>
    
    <dt>
    <a name="puchasing_options_templates"></a>
    The Tango Card and custom Company Email Templates - parameter <code>companyIdentifier</code> - string - <b>optional</b></dt>
    <dd>If you choose to have the Tango Card Service API send digital gift cards by setting <code>tcSend</code> to <code>true</code>, then by default the gift card information within a Tango Card email template.
    <br>If you prefer to have the Tango Card Service API send the gift card information with a custom email template (with your own branding), then please do contact us at <a href="mailto:sdk@tangocard.com?Subject=Tango Card Service API Question">sdk@tangocard.com</a>. We will respond to inquiries within one business day.
    </dd>
</dl>

<a name="sdk_support"></a>
# Tango Card SDKs and Service API Support #
If you have any questions with the Tango Card Service API, please contact us at <a href="mailto:sdk@tangocard.com?Subject=Tango Card Service API Question">sdk@tangocard.com</a>. We will respond to inquiries within one business day.

If you have any issues using this API, such as bugs or change requests, then please do <a href="https://github.com/tangocarddev/General/issues?state=open" target="_blank">Open Issue</a> in this repository.

<a name="sdk_support_resolve"></a>
## Resolving Issues ##

To expidite any issues you might be experiencing with our `Tango Card Service API` or our `Tango Card SDKs`, gather as much information by using the following two resolution approaches, and include the results when you contact us through <a href="mailto:sdk@tangocard.com?Subject=Tango Card Service API Question">sdk@tangocard.com</a>. We will respond to inquiries within one business day.

<a name="sdk_support_health_check"></a>
### Service Health Check ###

If you are having any issues with either INTEGRATION or PRODUCTION Tango Card Service API, check the endpoints' availability through a browser using the following health check URLs which should return a webpage with the text `"alive"`:

* INTEGRATION: [https://int.tangocard.com/Health/check](https://int.tangocard.com/Health/check)
* PRODUCTION: [https://api.tangocard.com/Health/check](https://api.tangocard.com/Health/check)

<a name="sdk_support_resolve_fiddler_2"></a>
### Fiddler 2 ###

The best way to resolve any issues that pertain to using our Tango Card SDKs or our Tango Card Service API is by using this freely available tool <a href="http://www.fiddler2.com/fiddler2/" target="_blank">`Fiddler 2 - Web Debugging Proxy`</a>, and providing us with the raw request and response bodies using its `Inspectors` tab feature.

Using `Fiddler 2` will provide us with the most complete detail and the fastest response from Tango Card by understanding if there is an issue on how a request was presented to our service, or if it is an issue with our service on how we replied to your request.

#### Fiddler 2 Example - Raw Request from Client - Get Available Balance ####

```Text
POST https://int.tangocard.com/Version2/GetAvailableBalance HTTP/1.1
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en-us
Content-Type: application/json; charset=UTF-8
Accept-Encoding: gzip, deflate
User-Agent: Mozilla/5.0 (compatible; MSIE 9.0; Windows NT 6.1; WOW64; Trident/5.0)
Host: int.tangocard.com
Content-Length: 69
Connection: Keep-Alive
Cache-Control: no-cache
 
{"username":"third_party_int@tangocard.com","password":"integrateme"}
```
 
#### Fiddler 2 Example - Raw Response from Service - Get Available Balance ####

```Text
HTTP/1.1 200 OK
Date: Wed, 26 Sep 2012 04:30:36 GMT
Server: Apache/2.2.22 (Ubuntu)
X-Powered-By: PHP/5.3.10-1ubuntu3.3
Access-Control-Allow-Origin: *
Content-Length: 68
Connection: close
Content-Type: application/json
 
{"responseType":"SUCCESS","response":{"availableBalance":873431432}}
```

<a name="sdk_support_resolve_tc_diagnostic_tool"></a>
### Tango Card Service API Diagnostic Tool ###

Within our <a href="https://github.com/tangocarddev/TangoCard_jQuery_Plugin" target="_blank"><code>Tango Card jQuery Plugin</code></a> examples, there is diagnostic tool which communicates with `Tango Card Service API` through <a href="http://api.jquery.com/jQuery.ajax/" target="_blank"><code>jQuery.ajax()</code></a> calls. It is useful for making raw calls to our service: <a href="https://github.com/tangocarddev/TangoCard_jQuery_Plugin#tango_card_service_api_diagnostic_tool" target="_blank">Tango Card Service API Diagnostic Tool</a>.

<a name="tango_card_api_overview"></a>
# Tango Card Service API Overview #

<a name="tango_card_api_requests"></a>
## Tango Card Service API Requests ##

With the Tango Card Service API, every request has a corresponding success-case response object. There are also several failure-case response objects which are shared between calls. The specifics of the request and response objects will be described in <a href="#tango_card_api_methods">Tango Card Service API Methods</a>.

<a name="http_post_request_body"></a>
### HTTP POST Request Body ###

All requests are via JSON-encoded objects as the payload of a HTTP POST call on a specified method. As an example, if the input listed below was "sku" then the POST body might look like:

```json
{"sku":"tango-card"}
```

Thereby, HTTP POST's `"Content-Type"` is expected to be <a href="http://tools.ietf.org/html/rfc4627" target="_blank">`application/json; charset=utf-8`</a>.

`Content-type: application/json; charset=utf-8` designates the content to be in JSON format, encoded in the UTF-8 character encoding. Designating the encoding is somewhat redundant for JSON, since the default encoding for JSON is UTF-8. So in this case the receiving server apparently is happy knowing that it's dealing with JSON and assumes that the encoding is UTF-8 by default, that's why it works with or without the header.

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
# Tango Card Service API Methods #

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
                    <dt><code>availableBalance</code></dt>
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
    <dt>companyIdentifier</dt>
    <dd>string (length 1 - 255, optional if tcSend=true) - Identifier of .</dd>
</dl>

#### Example `HTTP POST` Request ####

```http
POST https://int.tangocard.com/Version2/PurchaseCard HTTP/1.1
Content-Type: application/json
Host: int.tangocard.com
Content-Length: 201
Expect: 100-continue

{
  "username": "third_party_int@tangocard.com",
  "password": "integrateme",
  "cardSku": "tango-card",
  "cardValue": 500,
  "tcSend": true,
  "recipientName": "Jeff Tanner",
  "recipientEmail": "jeff@tangocard.com",
  "giftMessage": "Sorry for the trouble. Here is a Tango Card.",
  "giftFrom": "Jeff Tango Card Dev",
  "companyIdentifier": "Tango Card"
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
                    <dt><code>referenceOrderId</code></dt>
                    <dd>string - Confirmation number of purchase.</dd>
                    <dt><code>cardToken</code></dt>
                    <dd>string - Card reference to the aforementioned purchase..</dd>
                    <dt><code>cardNumber</code></dt>
                    <dd>string|null - If available, the card number provided to the recipient to be used at redemption of eGift Card upon the www.tangocard.com site.</dd>
                    <dt><code>cardPin</code></dt>
                    <dd>string|null - If available, the card pin provided to the recipient used to validate provided eGift Card number a redemption upon the www.tangocard.com site.</dd>
                    <dt><code>claimUrl</code></dt>
                    <dd>string|null - If available, the claim URL is an address to a web page on the World Wide Web. This URL can only be accessed through the email you received. It is a unique URL, meaning that it cannot be duplicated or altered.</dd>
                    <dt><code>challengeKey</code></dt>
                    <dd>string|null - If available, the challenge key provides access, which can be found next to the aforementioned claim URL. You will be prompted to input your Challenge Key when you try to open your eGift Card.</dd>
                    <dt><code>eventNumber</code></dt>
                    <dd>string|null - If available depending upon provided card SKU, then the event number is used when replacing lost card.</dd>
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
    "responseType": "SUCCESS",
    "response": {
        "referenceOrderId": "113-03237814-26",
        "cardToken": "51513caf481aa9.81359796",
        "cardNumber": "7001-3040-0191-1147-118",
        "cardPin": "536454",
        "claimUrl": null,
        "challengeKey": "7001304001911147118",
        "eventNumber": null
    }
}
```

<a name="failure_response_types" ></a>
# Failure Response Types #

Here are the following expected failure response types that can be returned from Tango Card Service API endpoint.

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

One (or more) of the supplied inputs didn�t meet the requirements. The request should be altered before resubmitting.

<dl>
    <dt>invalid<dt>
    <dd>JSON object - The object�s properties are the name of the invalid field, the value of the property is description of the associated problem.</dd>
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

{
    "responseType":"INV_CREDENTIAL",
    "response":
        {
            "message":"TCP:PNPA:3"
        }
}
```
    
<a name="failure_response_ins_inv" ></a>
### `INS_INV` ###

We don�t have enough available inventory to fulfill the request. The request should be altered before resubmitting.

<dl>
    <dt>sku<dt>
    <dd>string - The SKU that we couldn�t fulfill.</dd>
    <dt>value<dt>
    <dd>integer - The value that we couldn�t fulfill.</dd>
</dl>
    
<a name="failure_response_ins_funds" ></a>
### `INS_FUNDS` ###

The account associated with the authenticated user doesn�t have enough available balance to cover the cost of the purchase.

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

<a name="license"></a>
# License #

The Tango Card Service API is free to use, given some restrictions. Please see the <a href="href="https://github.com/tangocarddev/General/blob/master/LICENSE.md" target="_blank">LICENSE</a> file for details.

<a name="contact_us"></a>
# Contact Us #

If you have any questions about using this SDK, please do contact us at <a href="mailto:sdk@tangocard.com?Subject=Tango Card Service API Question">sdk@tangocard.com</a>. We will respond to inquiries within one business day.

To learn more about Tango Card integration solutions, call 1.877.55.TANGO (1.877.558.2646).
-->
