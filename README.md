# Bahrain Tech Resource

List of online services that can be used by developers in Bahrain.
## Content

### Payment

#### Gateway
- [Benefit](https://www.benefit.bh/Services/paymentgateway/): The Payment Gateway (PG) enables merchants, corporate and Government entities to process online transactions via the use of **debit (ATM) card payments**.
- [CreditMax](https://www.credimax.com.bh/en/e_payment_gateway): Offer **credit card payments**.
- Paypal: Developer tools and resources to integrate PayPal Commerce Platform.
    - [Documentation](https://developer.paypal.com/home/)
    - [Fee](https://www.paypal.com/us/webapps/mpp/merchant-fees#paypal-payouts)
    - **Note: Not all debet cards in Bahrain work with Paypal**

#### Payment tools 
- [BenefitJS](https://github.com/yazinsai/benefit-js-1): a simple, open-source library that allows you to accept BENEFIT payments through a modern, reliable interface that is optimized around the User Experience.
- [Tap](https://www.tap.company/)
- [Sadad Bahrain](https://sadadbahrain.com)
- [Gaatee](http://gaatee.com/): 
    
### Shipping
#### International 
- [Aramex](https://www.aramex.com/bh/en/solutions-services/developers-solutions-center/apis)
- [DHL](https://www.dhl.com/bh-en/home/all-products-and-solutions/technology-platform-integration/request-api-access.html)
- [FedEx](https://www.fedex.com/en-us/developer.html)
- [TNT](https://express.tnt.com/expresswebservices-website/app/landing.html)

### Data
#### Weather 
- [OpenWeather](https://openweathermap.org/api)

#### Geographic
- [Bahrain map ](http://www.ma-investment.gov.bh/website/discover_bah/)
- [Ministry of Education Open Data](https://www.moe.gov.bh/opendata.aspx?lan=en), note: the location point for some of the data is incorrect.
- [Air Quality ](https://aqicn.org/api/): non commercial use

#### Other
- [Bahrain (COVID-19) statistics](https://github.com/plusmnt/bh-cv-api): a json interface for the [summary of cases table](https://www.moh.gov.bh/COVID19) in Bahrain Ministry of Health website.

### Rules and regulations
- [Decrees related to the Information & eGovernment Authority](http://www.iga.gov.bh/en/category/decrees)
- [Telecommunications Regulatory Authority](https://www.tra.org.bh/en/category/regulations)

## Known issues
### NTP Protocal (STC network)
For some reason [NTP protocol](https://tools.ietf.org/html/rfc958) blocked by STC network, if you are trying to get the time from the internet you can use [HTTP Time protocol](http://www.vervest.org/htp/) instead.      

To test if your ISP block NTP you can install [Python NTP library](https://pypi.org/project/ntplib/) and run the example. If you get `NTPException: No response received from europe.pool.ntp.org.` exception, your ISP is blocking  NTP connection.

---

### STC timeout redirect error.
If you try to connect to offline server or unregistered domain you will get a [302 http](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/302) code and get redirected to https://stcerror.stc.com.bh/.     
The solution to this problem is to change your DNS to someone else other than STC DNS, if your service check if the domain is working, you might need to check if you get redirected to `stcerror.stc.com.bh` and consider that as timeout error.
