# Stripe Guide

## Configuration

### Settings/Account Settings

#### **Business**

!!! info "Account details"
    **Account name:** Gradewing
    **Business address:** Travesia De Somosierra, 9 2ºB 28760 Tres Cantos
    **Time zone:** UTC 

!!! info "Business details"
    **Website - URL:** www.gradewing.com
    **Public details:** 
        **Legal business name:** Pablo Peñas Lopez
        **Business name:** Gradewing
        **Statement descriptor:** GRADEWING.COM
        **Shortened descriptor:** GRADEWING
        **Customer support phone number:** +34 639 73 23 07
        **Customer support address:** Travesía De Somosierra, 9 2ºB
        **Customer support email:** hello@gradewing.com
        **Customer support URL:** https://gradewing.com
        **Business website:** www.gradewing.com
        **Privacy policy URL:** https://www.gradewing.com/legal/
        **Terms of service URL:** https://www.gradewing.com/legal/
    **Management and ownership:** Pablo Peñas Lopez - pablopen01@gmail.com - 10/04/1990 - Travesía De Somosierra, 9 2ºB - 53746221M

!!! warning "Por precaución eliminamos los acentos, por ejemplo de Lopez, y la dirección postal siempre la ponemos exactamente igual. Se mantiene la "ñ" de Peñas."

!!! info "Bank account and currencies"
    **Settlement currencies and bank accounts:** EUR - Santander ...9068
    **Payout schedule:** Manual payouts
    **Payout speed:** Standard payout speed

!!! info "Tax details"
    **Type of business:** Empresario individual (Autonomo)
    **The name you provide must exactly match the name associated with your tax ID:** PABLO PEÑAS LOPEZ
    **Tax identification number:** 53746221M
    **VAT number (NIF):** ES53746221M

!!! info "Branding"
    **Icon:** gradewing_icon.png
    **Logo:** gradewing_logo.png
    **Brand colour:** #ddf3f3
    **Accent colour:** #2ea1a3
    **Add your domain:** checkout.stripe.com, buy.stripe.com, billing.stripe.com will be used

!!! info "Customer emails"
    **Default language:** English
    **Payments:** Successful payments, Refunds
    **Domain:** stripe.com

### Products: Tax

!!! info "Add Registration"
    **Choose a location:** Spain
    **How do you want to register?:** I've already registered
    **Select the type of registration that's applicable to you:** Domestic
    **Do you want to collect VAT on the cross-border sales of goods shipped from outside the EU to Spain?:** No
    **Have your sales of goods or digital services to individuals in other EU countries been less than €10,000 in the current or previous calendar year?:** Yes
    **Schedule tax collection:** 5/10/2026
    **Confirm your tax rates in Spain:** SaaS

### Product catalogue

#### **All products**

| Product Name | Amount | Currency | Interval | Interval Count | Tax Behavior |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Unlimited Plan** | 159,00 | eur | month | 1 | exclusive |
| **Unlimited Plan** | 1590,00 | eur | year | 1 | exclusive |
| **Higher 40 Plan** | 129,00 | eur | month | 1 | exclusive |
| **Higher 40 Plan** | 1290,00 | eur | year | 1 | exclusive |
| **Core 20 Plan** | 990,00 | eur | year | 1 | exclusive |
| **Core 20 Plan** | 99,00 | eur | month | 1 | exclusive |
| **AI Credits - 6250** | 25,00 | eur | | | exclusive |
| **AI Credits - 11250** | 45,00 | eur | | | exclusive |

#### **Coupons**
!!! info "Create coupon"
    **Name:** Introductory coupon
    **Type:** Percentage off
    **Percentage discount:** 30%
    **Duration:** 10 months
    **Redemption limits:** 01/04/2027
    **Codes:** INT2026

#### **Pricing tables**

!!! info "Products"
    | Product Name | Amount | Currency | Interval |
    | :--- | :--- | :--- | :--- |
    | **Unlimited Plan** | 159,00 | eur | month |
    | **Unlimited Plan** | 1590,00 | eur | year |
    | **Higher 40 Plan** | 129,00 | eur | month |
    | **Higher 40 Plan** | 1290,00 | eur | year |
    | **Core 20 Plan** | 990,00 | eur | year |
    | **Core 20 Plan** | 99,00 | eur | month |

!!! info "Display settings"
    **Default view:** Yearly
    **Language:** English
    **Background colour:** #ffffff
    **Button colour:** #2fa29a
    **Font:** Nunito
    **Button shape:** Rounded

!!! info "Payment settings"
    Collect tax automatically
    Allow promotion codes
    Allow business customer to provide tax IDs
    Collect billing addresses
    Collect phone numbers
    Don't show confirmation page
    Redirect customers to your website: (https://gradewing.com/app/products/billing/payment-success?session_id={CHECKOUT_SESSION_ID})

!!! info "Set up customer portal"
    **Customer portal:** Allow customer to change products

### Settings/Product Settings

#### **Billing**

!!! info "Subscriptions and emails"
    **Email notifications and customer management:** 
        **Customer emails:** Send emails about upcoming renewals - Send emails about expiring cards - Send emails when card payments fail
        **Payment method updates:** Use your own custom link: https://www.gradewing.com
    **Prevent failed payments:** Upcoming renewal events: 3 days
    **Manage failed payments for subscriptions:** 
        **Card payments:** Retry 5 days after the previous attempt and Retry 5 days after the previous attempt
        **Subscription status:** leave the subscription overdue
        **Invoice status:** leave the invoice overdue
    **Manage disputed payments:** leave the subscription overdue
    **Default billing mode:** Flexible

!!! info "Invoices"
    **General:**
        **Invoice numbering:** Sequentially across your accout
            **Invoice prefix:** INVyyyy
            **Next live invoice sequence:** 1
        **Invoice PDFs:** Include pdf links on invoice emails and payment page
        **Manual tax amount rounding:** At invoice level
        **Default item prices:** Include inclusive tax
        **Default payment terms:** Save customer payment information & Ask customers before saving their payment information
        **Default payment methods:** Default
        **Adaptive Pricing:** International customers will have the option to pay one-time invoices in their local currency on your payment page.
        **Reminders and retries:**
            **Retries for failed card payments:** Retry 5 days after the previous attempt and Retry 5 days after the previous attempt
        **Invoice finalisation grace period:** Default - 1 hour
        **Invoice tax information:**
            **Tax ID:** 
                **ES NIF:** 53746221M
                **ES VAT:** ES53746221M 
    **Templates:** Gradewing_Inv

!!! info "Customer portal"
    **Portal configuration:** Default
    **Invoices:** Invoices history
    **Customer information:** Name, Email address, Billing address, Phone number, Tax ID
    **Payment methods:** Default - Credit and debit cards
    **Cancel subscription:** At the end of the billing period - Collect a cancelation reason
    **Subscriptions:** Customers can switch plans
    **When customers change plans or quantities:** Prorate charges and credits - Invoice proration immediately at time of the update
    **Downgrades:** Update immediately - Update immediately

#### **Tax**

!!! info "Business information"
    **Preset product category:** SaaS
    **Taxes on shipping:** Never
    **Include tax in prices:** No

!!! info "Integration"
    **Tax calculation:** Stripe Tax in use
    **Dashboard transactions:** Use automatic tax

#### **Payments**

!!! info "Checkout, Payments methods and currencies"
    **Checkout and Payment Links:** 
        **Address autocomplete:** with Google Maps
        **Pricing display:** Monthly terms
    **Payment methods:** Only Type Cards
    **Adaptive Pricing:** Enable Adaptive Pricing
    **Disputes:** Enable auto-submit

## Ongoing Management

### Balances

!!! info "Pay out:"
    **Amount to pay out**

!!! info "Manage payouts"
    **Manage bank account**

### Refunds - Credit notes

!!! info "Invoices: select an invoice"
    **Credit notes:** + Credit note

!!! info "Issue a Credit note"
    **Reason:** Duplicate charge, Order change, Other 
    **Credit Amoun:** Amount to refund
    **How to credit:** Refund to Credit(Debit Card)
    **Issue a credit note**

!!! info "Send receipt to the customer"
    **Customers:** Select the customer
    **Payments:** Select the payment refunded - ... Send receipt

### Disputes

!!! info "Transactions/Payments/Disputed"
    **Actions:** Submit evidence to counter dispute

### Libro de Facturas: Invoices and Credit notes

### VIES: VAT Information Exchange System

!!! info "Tax transactions"
    **Products/Tax/Overview:** Tax collected on paid invoices
    **Explore:** Choose period, usually from 01/mm/yyyy to 31/mm/yyyy (month)
    **Summary:** Spain Location
    **Tax collected on paid invoices in Spain:** "Copy" all the rows, then "Paste" them on corresponding excel workbook.

| Location | Tax collected | Currency | Description | Date |
| :--- | :--- | :---: | :--- | :--- |
| Spain | **€27.09** | EUR | `tax_1TSLOsRV6uy3eJFZJDhZnvoX` | 1 May 2026, 18:03 |
| Spain | **-€6.30** | EUR | `tax_1TSLSQRV6uy3eJFZjrIH2KJg` | 1 May 2026, 18:07 |
| Spain | **€20.79** | EUR | `tax_1TShFGRV6uy3eJFZxgPBnyhG` | 2 May 2026, 17:23 |
| Spain | **€20.79** | EUR | `tax_1TShbqRV6uy3eJFZT5n7gUvX` | 2 May 2026, 17:46 |
| Spain | **€27.09** | EUR | `tax_1TShhoRV6uy3eJFZM7zPAc3L` | 2 May 2026, 17:53 |
| Spain | **€20.79** | EUR | `tax_1TSiPkRV6uy3eJFZWb0aRxeP` | 2 May 2026, 18:38 |
| Spain | **-€5.73** | EUR | `tax_1TSivPRV6uy3eJFZD0GGgRMe` | 2 May 2026, 19:10 |
| Spain | **-€6.93** | EUR | `tax_1TSkkFRV6uy3eJFZd2w9K2IE` | 2 May 2026, 21:06 |
| Spain | **-€4.34** | EUR | `tax_1TSxLCRV6uy3eJFZucuE1wMy` | 3 May 2026, 10:33 |

!!! warning "Si no hay **Credit Notes**, podria utilizarse directamente el **Export** que aparece en Tax collected on paid invoices in Spain."

### Comisiones Stripe (Gastos deducibles)



