# Stripe Guide

## Configuration

### Account Settings

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

| Product Name | Amount | Currency | Interval | Interval Count | Usage Type | Tax Behavior |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Unlimited Plan** | 159,00 | eur | month | 1 | licensed | exclusive |
| **Unlimited Plan** | 1590,00 | eur | year | 1 | licensed | exclusive |
| **Higher 40 Plan** | 129,00 | eur | month | 1 | licensed | exclusive |
| **Higher 40 Plan** | 1290,00 | eur | year | 1 | licensed | exclusive |
| **Core 20 Plan** | 990,00 | eur | year | 1 | licensed | exclusive |
| **Core 20 Plan** | 99,00 | eur | month | 1 | licensed | exclusive |
| **AI Credits - 6250** | 25,00 | eur | | | | exclusive |
| **AI Credits - 11250** | 45,00 | eur | | | | exclusive |

#### **Coupons**
!!! info "Create coupon"
    **Name:** Introductory coupon
    **Type:** Percentage off
    **Percentage discount:** 30%
    **Duration:** 10 months
    **Redemption limits:** 01/04/2027
    **Codes:** INT2026

#### **Pricing tables**


#### **Tax**

!!! info "Business information"
    **Preset product category:** SaaS
    **Taxes on shipping:** Never
    **Include tax in prices:** No

!!! info "Integration"
    **Tax calculation:** Stripe Tax in use
    **Dashboard transactions:** Use automatic tax

### Product Settings

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


#### **Checkout, Payments metehods and currencies**

!!! info "Payments"
    **Checkout and Payment Links:** 
        **Address autocomplete:** with Google Maps
        **Pricing display:** Monthly terms
    **Payment methods:** Only Type Cards
    **Adaptive Pricing:** Enable Adaptive Pricing
    **Disputes:** Enable auto-submit

## Balances: Payouts 

## Refunds

## Disputes

## Exports



