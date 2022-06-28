# Cimet - Developer Assignment

Your task is to build a React.JS application.

Build a product listing page with one of the following options:
- render products in a table view
- render products in a card view

Product data displayed should be using the REST API provided below.

Reference desing:
Table view
![image](https://user-images.githubusercontent.com/19356394/173732953-4dcc11a6-a823-4cc0-9fff-429d5f5af3b3.png)
 
## Notes
 
Feel free to use any boilerplate or libraries to help you achieve a result.
We are expecting:
- Good codebase structure
- ES6
- Showcase your skills ![image](https://img.shields.io/static/v1?label=&message=wow&color=green)
 
## Deliverable

``` diff 
- Please don't push branches.
- Please don't make copies of this repository.
- Please don't share details with others.
```

Make a Fork and Submit a pull request against this repository. 
 
We will pull your code and execute the following commands:
 
js
```
yarn install
yarn start
```
 
or
 
```
npm install
npm start
```
 
These commands should bring your app up in development mode. We expect the terminal to display a URL where we can visit in browser.
 
## REST API
 
Please add http header Api-key with 4NKQ3-815C2-8T5Q2-16318-55301 when making any requests.
1. You need to generate a token using the token API. (it will last for 3hrs) 
```
endpoint : https://devcore02.cimet.io/v1/generate-token
Api-key : 4NKQ3-815C2-8T5Q2-16318-55301
Method: Post
```

2. Once you have the token, you can access our products.
 ```
endpoint: https://devcore02.cimet.io/v1/plan-list
Api-key : 4NKQ3-815C2-8T5Q2-16318-55301
Auth-token : {{token generated in previous step}}
Method: Post
Request Body: {"session_id":"eyJpdiI6IkVNUkZ1N0hlSHhHSnJ3Vjl4aUlxc0E9PSIsInZhbHVlIjoieFlxa1wvVDYxQWl5U2pxMDFcL0R6ZVVvdEN6Mkk0R29TRDN3ZnN0U3VGcER0cEFMa2NVb0xNcDJudjlRTHRUbGJkIiwibWFjIjoiMTE0MmU0MGE5YmJhMzY4Nzc4MDExNmZkNTI1MjZhMGE3OTQyMDZmOTc1MTVmZDM1Mzc3ZmJmNjhmMzllOGYxYSJ9"}
 ```
    

Data structure sample:
```
{
   "status": 1,
   "message": "Plan(s) found successfully.",
   "data": {
       "electricity": [
           {
               "id": 117,
               "provider_id": 5,
               "plan_name": "Total Plan Home - NSW",
               "energy_type": "electricity",
               "contract_length": "No Contract",
               "features": "<p></p>",
               "benefit_term": "12 month",
               "credit_card_service_fee": "<p></p>",
               "counter_fee": "<p>Nil</p>",
               "paper_bill_fee": "<p>Nil</p>",
               "cooling_off_period": "<p>10 business days</p>",
               "other_fee_section": "<p></p>",
               "plan_bonus": "",
               "plan_bonus_desc": "No Bonus",
               "billing_options": "Quarterly",
               "payment_options": "Direct debit, BPAY, cash, cheque, EFTPOS, MasterCard®, Visa and American Express® credit cards and debit cards.",
               "plan_desc": "",
               "plan_features": "<p>.</p>",
               "why_us": "",
               "is_bundle_dual_plan": "no",
               "bundle_code": "",
               "show_solar_plan": 0,
               "days": 365,
               "provider_image": "https://devcore02.cimet.io/uploads/providers_logo/5_EnergyAustralia.png",
               "provider_name": "EnergyAustralia",
               "applied_pay_day_discount_usage": "yes",
               "expected_annual_adjustments": 0,
               "daily_usage_limit": 10.684931506849,
               "pay_day_discount_usage": "10",
               "gurrented_discount_usage": "",
               "exit_fee_option": "no",
               "exit_fee": "No",
               "provider": {
                   "id": 5,
                   "eic": "",
                   "logo": "https://devcore02.cimet.io/uploads/providers_logo/5_EnergyAustralia.png",
                   "name": "EnergyAustralia",
                   "phone": "133466",
                   "status": 1,
                   "why_us": "",
                   "telecom_allow": "yes",
                   "send_plan_allow": "yes",
                   "demand_usage_check": "1"
               },
               "terms_condition": "<p>.</p>",
               "solar_rates": [
                   {
                       "id": 10,
                       "plan_id": 117,
                       "solar_price": 12.5,
                       "status": "1",
                       "type": 1,
				…
                   }
                   ...
               ],
               "solar_rate_normal": 12.5,
               "solar_rate_premium": 0,
               "plan_tags": [],
               "rates": [
                   {
                       "control_load_1_daily_supply_charges": 0,
                       "control_load_2_daily_supply_charges": 0,
                       "control_load_one_charges": 0,
                       "control_load_two_charges": 0,
                       "daily_supply_charges": 12.5,
                       "direct_debit_discount_desc": "",
                       "direct_debit_discount_supply": "",
                       "direct_debit_discount_usage": "",
                       "distributor_id": 4,
                       "distributor_name": "Ausgrid",
                       "effective_from": "2021-01-11",
                       "exit_fee": "No",
                       "exit_fee_option": "no",
                       "gst_rate": "0",
                       "id": 10589,
                       "master_content_status": "0",
                       "meter_type": "",
                       "off_peak_charges": 0,
                       "pay_day_discount_supply": "",
                       "pay_day_discount_supply_desc": "",
                       "pay_day_discount_usage": "10",
                       "pay_day_discount_usage_desc": "Pay Day Discount on Usage Description",
                       "plan_id": 117,
                       "provider_id": 5,
                       "rate_type": "Normal",
                       "remaining_offpeak_charges": 0,
                       "remaining_peak_usage_charges": 0,
                       "status": 1,
                       "tariff_type_title": "Single Rate Demand",
                       "timeofuse_charges": 0,
                       "type": "peak_only",
                       "demand_usage_check": "1",
                       "plan_rate_limit": [
                           {
                               "id": 33356,
                               "is_deleted": "0",
                               "limit_charges": 22.5,
                               "limit_daily": 10.68,
                               "limit_desc": "Peak usage charges exl. GST. ",
                               "limit_level": "1",
                               "limit_type": "peak",
                               "limit_yearly": 0,
                               "plan_rate_id": 10589
                           }
                       ],
                       ...
                   },
                   ...
               ],
               "dual_only": "0",
               "is_highlighted": "yes",
               "is_one_in_state": "no",
               },
               "dmo_percentage": {
                   "Ausgrid": "12 less than"
               },
               "plan_name_below_data": "the Reference price"
               ...
           }
           ...
       ]
   }
}
```
