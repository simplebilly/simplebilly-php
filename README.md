# SimpleBilly PHP SDK

[![Release](https://img.shields.io/github/v/release/simplebilly/simplebilly-php?label=release&logo=github)](https://github.com/simplebilly/simplebilly-php/releases)
[![CI](https://github.com/simplebilly/simplebilly-php/actions/workflows/release.yml/badge.svg)](https://github.com/simplebilly/simplebilly-php/actions/workflows/release.yml)
[![CodeQL](https://github.com/simplebilly/simplebilly-php/actions/workflows/codeql.yml/badge.svg)](https://github.com/simplebilly/simplebilly-php/actions/workflows/codeql.yml)
[![Scorecard](https://github.com/simplebilly/simplebilly-php/actions/workflows/scorecard.yml/badge.svg)](https://github.com/simplebilly/simplebilly-php/actions/workflows/scorecard.yml)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/simplebilly/simplebilly-php/badge)](https://scorecard.dev/viewer/?uri=github.com/simplebilly/simplebilly-php)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Docs](https://img.shields.io/badge/docs-simplebilly.com-blue)](https://simplebilly.com/api/docs)
# OpenAPIClient-php

Simplebilly API - Bookkeeping, CRM, ERP. Multi-tenant API: a tenant is isolated and routed by subdomain (or a configured custom domain) under the base domain.

## Rate limiting
All endpoints are rate-limited per client IP: **100 requests per minute** on API routes and **5 requests per minute** on authentication routes. Exceeding a limit returns `429 Too Many Requests`; the window resets after 60 seconds.

For more information, please visit [https://simplebilly.com/en/legal/imprint](https://simplebilly.com/en/legal/imprint).

## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AbsenceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$absence_create = new \OpenAPI\Client\Model\AbsenceCreate(); // \OpenAPI\Client\Model\AbsenceCreate

try {
    $result = $apiInstance->createAbsence($absence_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AbsenceApi->createAbsence: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://demo.simplebilly.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AbsenceApi* | [**createAbsence**](docs/Api/AbsenceApi.md#createabsence) | **POST** /api/v1/absences | 
*AbsenceApi* | [**deleteAbsence**](docs/Api/AbsenceApi.md#deleteabsence) | **DELETE** /api/v1/absences/{id} | 
*AbsenceApi* | [**getAbsence**](docs/Api/AbsenceApi.md#getabsence) | **GET** /api/v1/absences/{id} | 
*AbsenceApi* | [**getAbsences**](docs/Api/AbsenceApi.md#getabsences) | **GET** /api/v1/absences/ | 
*AbsenceApi* | [**updateAbsence**](docs/Api/AbsenceApi.md#updateabsence) | **PUT** /api/v1/absences/{id} | 
*ActivityApi* | [**createActivity**](docs/Api/ActivityApi.md#createactivity) | **POST** /api/v1/activities | 
*ActivityApi* | [**deleteActivity**](docs/Api/ActivityApi.md#deleteactivity) | **DELETE** /api/v1/activities/{activity_id} | 
*ActivityApi* | [**getActivity**](docs/Api/ActivityApi.md#getactivity) | **GET** /api/v1/activities/{activity_id} | 
*ActivityApi* | [**listActivities**](docs/Api/ActivityApi.md#listactivities) | **GET** /api/v1/activities/ | 
*ActivityApi* | [**updateActivity**](docs/Api/ActivityApi.md#updateactivity) | **PUT** /api/v1/activities/{activity_id} | 
*ActivityApi* | [**updateActivityStatus**](docs/Api/ActivityApi.md#updateactivitystatus) | **PUT** /api/v1/activities/{activity_id}/status | 
*AdminApi* | [**triggerMirror**](docs/Api/AdminApi.md#triggermirror) | **POST** /api/v1/admin/storage/mirror | 
*AiApi* | [**aiSuggestApi**](docs/Api/AiApi.md#aisuggestapi) | **POST** /api/v1/support/ai/suggest | 
*AiApi* | [**createWorkerApi**](docs/Api/AiApi.md#createworkerapi) | **POST** /api/v1/support/ai/workers | 
*AiApi* | [**listWorkersApi**](docs/Api/AiApi.md#listworkersapi) | **GET** /api/v1/support/ai/workers | 
*AiApi* | [**runWorkerApi**](docs/Api/AiApi.md#runworkerapi) | **POST** /api/v1/support/ai/workers/{worker_id}/run | 
*AnlageEksApi* | [**eksApi**](docs/Api/AnlageEksApi.md#eksapi) | **GET** /api/v1/bookkeeping/eks | 
*AnlageGApi* | [**anlageGApi**](docs/Api/AnlageGApi.md#anlagegapi) | **GET** /api/v1/bookkeeping/anlage-g | 
*AnlageSApi* | [**anlageSApi**](docs/Api/AnlageSApi.md#anlagesapi) | **GET** /api/v1/bookkeeping/anlage-s | 
*AttachmentApi* | [**attachmentRestore**](docs/Api/AttachmentApi.md#attachmentrestore) | **POST** /api/v1/attachments/{id}/restore | 
*AttachmentApi* | [**createAttachment**](docs/Api/AttachmentApi.md#createattachment) | **POST** /api/v1/attachments | 
*AttachmentApi* | [**deleteAttachment**](docs/Api/AttachmentApi.md#deleteattachment) | **DELETE** /api/v1/attachments/{id} | 
*AttachmentApi* | [**getAttachment**](docs/Api/AttachmentApi.md#getattachment) | **GET** /api/v1/attachments/{id} | 
*AttachmentApi* | [**listAttachments**](docs/Api/AttachmentApi.md#listattachments) | **GET** /api/v1/attachments/ | 
*AttachmentApi* | [**saveAttachmentOcrText**](docs/Api/AttachmentApi.md#saveattachmentocrtext) | **PUT** /api/v1/attachments/{attachment_id}/ocr-text | Persist client-side OCR output for an attachment.
*AttachmentVersionApi* | [**createAttachmentVersion**](docs/Api/AttachmentVersionApi.md#createattachmentversion) | **POST** /api/v1/attachments/{attachment_id}/versions | 
*AttachmentVersionApi* | [**listAttachmentVersions**](docs/Api/AttachmentVersionApi.md#listattachmentversions) | **GET** /api/v1/attachments/{attachment_id}/versions | 
*AttachmentVersionApi* | [**restoreAttachmentVersion**](docs/Api/AttachmentVersionApi.md#restoreattachmentversion) | **POST** /api/v1/attachments/{attachment_id}/versions/{version_id}/restore | 
*AuthApi* | [**acceptInvite**](docs/Api/AuthApi.md#acceptinvite) | **POST** /auth/accept-invite | Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.
*AuthApi* | [**forgotPassword**](docs/Api/AuthApi.md#forgotpassword) | **POST** /auth/forgot-password | Send a password reset email to the user
*AuthApi* | [**login**](docs/Api/AuthApi.md#login) | **POST** /auth/login | Authenticate a user with email + password (optional TOTP)
*AuthApi* | [**logout**](docs/Api/AuthApi.md#logout) | **POST** /auth/logout | Log out the current user (kills the assay session)
*AuthApi* | [**magicLinkLogin**](docs/Api/AuthApi.md#magiclinklogin) | **POST** /auth/magic-link | Request a magic link login (sends an email with a one-time link)
*AuthApi* | [**magicLinkVerify**](docs/Api/AuthApi.md#magiclinkverify) | **POST** /auth/magic-link/verify | Verify a magic link token and log the user in
*AuthApi* | [**register**](docs/Api/AuthApi.md#register) | **POST** /auth/register | Register a new user account
*AuthApi* | [**resetPassword**](docs/Api/AuthApi.md#resetpassword) | **POST** /auth/reset-password | Reset the user&#39;s password using a reset token
*AuthApi* | [**totpEnable**](docs/Api/AuthApi.md#totpenable) | **POST** /auth/totp/enable | Enable TOTP two-factor authentication by verifying a code
*AuthApi* | [**totpSetup**](docs/Api/AuthApi.md#totpsetup) | **GET** /auth/totp/setup | Set up TOTP two-factor authentication (generates secret + backup codes)
*AuthApi* | [**verifyEmail**](docs/Api/AuthApi.md#verifyemail) | **POST** /auth/verify-email | Verify a user&#39;s email address using a verification token
*AutomationsApi* | [**listAutomations**](docs/Api/AutomationsApi.md#listautomations) | **GET** /api/v1/automations | 
*AutomationsApi* | [**triggerAutomation**](docs/Api/AutomationsApi.md#triggerautomation) | **POST** /api/v1/automations/{key}/trigger | 
*AutomationsApi* | [**updateAutomation**](docs/Api/AutomationsApi.md#updateautomation) | **PUT** /api/v1/automations/{key} | 
*BankingApi* | [**bankLookupApi**](docs/Api/BankingApi.md#banklookupapi) | **GET** /api/v1/bookkeeping/banking/lookup | 
*BankingApi* | [**bankTransactionsApi**](docs/Api/BankingApi.md#banktransactionsapi) | **GET** /api/v1/bookkeeping/banking/transactions | 
*BankingApi* | [**hebesatzLookupApi**](docs/Api/BankingApi.md#hebesatzlookupapi) | **GET** /api/v1/bookkeeping/hebesatz | 
*BillingApi* | [**getPlans**](docs/Api/BillingApi.md#getplans) | **GET** /api/v1/plans | All canonical plans (free/starter/business/enterprise) — the single source of truth lives in &#x60;crate::saasy::plans&#x60;, matching marketing.
*BillingApi* | [**getQuotaApi**](docs/Api/BillingApi.md#getquotaapi) | **GET** /api/v1/quota | Effective limits + current usage for the calling tenant.
*BillingApi* | [**getSubscriptionApi**](docs/Api/BillingApi.md#getsubscriptionapi) | **GET** /api/v1/subscription | 
*BillingApi* | [**getUsageApi**](docs/Api/BillingApi.md#getusageapi) | **GET** /api/v1/usage | 
*BillingApi* | [**paddleSubscriptionWebhook**](docs/Api/BillingApi.md#paddlesubscriptionwebhook) | **POST** /api/webhooks/paddle/subscription | Paddle Billing subscription webhook. Verifies the &#x60;Paddle-Signature&#x60; header (HMAC-SHA256 over &#x60;\&quot;{ts}:{raw_body}\&quot;&#x60; with the webhook secret), then updates &#x60;billing_info&#x60; and &#x60;tenants.plan&#x60; for the tenant identified by the subscription &#x60;custom_data&#x60; (JSON &#x60;{\&quot;tenant_id\&quot;: \&quot;...\&quot;}&#x60; or a bare tenant UUID).
*BillingApi* | [**putQuotaApi**](docs/Api/BillingApi.md#putquotaapi) | **PUT** /api/v1/quota | Write the per-tenant quota override (&#x60;admin:settings&#x60;). An empty object clears the override.
*BomApi* | [**createBom**](docs/Api/BomApi.md#createbom) | **POST** /api/v1/boms | 
*BomApi* | [**deleteBom**](docs/Api/BomApi.md#deletebom) | **DELETE** /api/v1/boms/{bom_id} | 
*BomApi* | [**getBom**](docs/Api/BomApi.md#getbom) | **GET** /api/v1/boms/{bom_id} | 
*BomApi* | [**listBoms**](docs/Api/BomApi.md#listboms) | **GET** /api/v1/boms/ | 
*BomApi* | [**updateBom**](docs/Api/BomApi.md#updatebom) | **PUT** /api/v1/boms/{bom_id} | 
*BookkeepingApi* | [**allocatePaymentApi**](docs/Api/BookkeepingApi.md#allocatepaymentapi) | **POST** /api/v1/payments/allocate | Allocate a payment to an invoice
*BookkeepingApi* | [**bwaReportApi**](docs/Api/BookkeepingApi.md#bwareportapi) | **GET** /api/v1/bookkeeping/bwa | Get BWA (Betriebswirtschaftliche Auswertung) report
*BookkeepingApi* | [**elsterStatusApi**](docs/Api/BookkeepingApi.md#elsterstatusapi) | **GET** /api/v1/bookkeeping/elster/status | 
*BookkeepingApi* | [**elsterValidateApi**](docs/Api/BookkeepingApi.md#elstervalidateapi) | **POST** /api/v1/bookkeeping/ustva/elster-validate | 
*BookkeepingApi* | [**elsterXmlApi**](docs/Api/BookkeepingApi.md#elsterxmlapi) | **GET** /api/v1/bookkeeping/ustva/elster-xml | 
*BookkeepingApi* | [**getCashflow**](docs/Api/BookkeepingApi.md#getcashflow) | **GET** /api/v1/bookkeeping/cashflow | GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.
*BookkeepingApi* | [**getLiquidity**](docs/Api/BookkeepingApi.md#getliquidity) | **GET** /api/v1/bookkeeping/liquidity | GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.
*BookkeepingApi* | [**getOpenInvoicesApi**](docs/Api/BookkeepingApi.md#getopeninvoicesapi) | **GET** /api/v1/payments/open-invoices/{customer_id} | Get open invoices for a customer
*BookkeepingApi* | [**getVerfahrensdokumentation**](docs/Api/BookkeepingApi.md#getverfahrensdokumentation) | **GET** /api/v1/bookkeeping/verfahrensdokumentation | GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.
*BookkeepingApi* | [**runDunningApi**](docs/Api/BookkeepingApi.md#rundunningapi) | **POST** /api/v1/bookkeeping/dunning | 
*BudgetsApi* | [**budgetsApi**](docs/Api/BudgetsApi.md#budgetsapi) | **GET** /api/v1/bookkeeping/budgets | 
*BudgetsApi* | [**upsertBudgetGoalApi**](docs/Api/BudgetsApi.md#upsertbudgetgoalapi) | **PUT** /api/v1/bookkeeping/budgets/goals/{category} | 
*ComplianceTrainingApi* | [**createComplianceTraining**](docs/Api/ComplianceTrainingApi.md#createcompliancetraining) | **POST** /api/v1/compliance-trainings | 
*ComplianceTrainingApi* | [**deleteComplianceTraining**](docs/Api/ComplianceTrainingApi.md#deletecompliancetraining) | **DELETE** /api/v1/compliance-trainings/{id} | 
*ComplianceTrainingApi* | [**getComplianceTraining**](docs/Api/ComplianceTrainingApi.md#getcompliancetraining) | **GET** /api/v1/compliance-trainings/{id} | 
*ComplianceTrainingApi* | [**getComplianceTrainings**](docs/Api/ComplianceTrainingApi.md#getcompliancetrainings) | **GET** /api/v1/compliance-trainings/ | 
*ComplianceTrainingApi* | [**updateComplianceTraining**](docs/Api/ComplianceTrainingApi.md#updatecompliancetraining) | **PUT** /api/v1/compliance-trainings/{id} | 
*ContactApi* | [**contactSchema**](docs/Api/ContactApi.md#contactschema) | **GET** /api/v1/contacts/schema | Serve JSON Schema for client-side validation
*ContactApi* | [**contactTimeline**](docs/Api/ContactApi.md#contacttimeline) | **GET** /api/v1/contacts/{contact_id}/timeline | Get the full per-contact timeline (Xentral §4.6/4.7).
*ContactApi* | [**createContact**](docs/Api/ContactApi.md#createcontact) | **POST** /api/v1/contacts | Create contact
*ContactApi* | [**deleteContact**](docs/Api/ContactApi.md#deletecontact) | **DELETE** /api/v1/contacts/{contact_id} | Soft-delete contact
*ContactApi* | [**getContact**](docs/Api/ContactApi.md#getcontact) | **GET** /api/v1/contacts/{contact_id} | Get single contact
*ContactApi* | [**listContacts**](docs/Api/ContactApi.md#listcontacts) | **GET** /api/v1/contacts | List contacts with search, type filter, and pagination
*ContactApi* | [**salesVolume**](docs/Api/ContactApi.md#salesvolume) | **GET** /api/v1/contacts/sales-volume | Sales volume per contact
*ContactApi* | [**updateContact**](docs/Api/ContactApi.md#updatecontact) | **PUT** /api/v1/contacts/{contact_id} | Update contact
*CouponApi* | [**couponRestore**](docs/Api/CouponApi.md#couponrestore) | **POST** /api/v1/coupons/{coupon_id}/restore | 
*CouponApi* | [**createCoupon**](docs/Api/CouponApi.md#createcoupon) | **POST** /api/v1/coupons | 
*CouponApi* | [**deleteCoupon**](docs/Api/CouponApi.md#deletecoupon) | **DELETE** /api/v1/coupons/{coupon_id} | 
*CouponApi* | [**getCoupon**](docs/Api/CouponApi.md#getcoupon) | **GET** /api/v1/coupons/{coupon_id} | 
*CouponApi* | [**listCoupons**](docs/Api/CouponApi.md#listcoupons) | **GET** /api/v1/coupons/ | 
*CouponApi* | [**updateCoupon**](docs/Api/CouponApi.md#updatecoupon) | **PUT** /api/v1/coupons/{coupon_id} | 
*CreateSepaDirectDebitApi* | [**createSepaDirectDebitApi**](docs/Api/CreateSepaDirectDebitApi.md#createsepadirectdebitapi) | **POST** /api/v1/bookkeeping/sepa-direct-debit | 
*CreditNoteApi* | [**createCreditNote**](docs/Api/CreditNoteApi.md#createcreditnote) | **POST** /api/v1/credit-notes | 
*CreditNoteApi* | [**downloadCreditNotePdf**](docs/Api/CreditNoteApi.md#downloadcreditnotepdf) | **GET** /api/v1/credit-notes/{credit_note_id}/pdf | 
*CreditNoteApi* | [**getCreditNote**](docs/Api/CreditNoteApi.md#getcreditnote) | **GET** /api/v1/credit-notes/{credit_note_id} | 
*CreditNoteApi* | [**listCreditNotes**](docs/Api/CreditNoteApi.md#listcreditnotes) | **GET** /api/v1/credit-notes/ | 
*CustomerApi* | [**createCustomer**](docs/Api/CustomerApi.md#createcustomer) | **POST** /api/v1/customers | 
*CustomerApi* | [**customerRestore**](docs/Api/CustomerApi.md#customerrestore) | **POST** /api/v1/customers/{customer_id}/restore | 
*CustomerApi* | [**deleteCustomer**](docs/Api/CustomerApi.md#deletecustomer) | **DELETE** /api/v1/customers/{customer_id} | 
*CustomerApi* | [**getCustomer**](docs/Api/CustomerApi.md#getcustomer) | **GET** /api/v1/customers/{customer_id} | 
*CustomerApi* | [**getCustomers**](docs/Api/CustomerApi.md#getcustomers) | **GET** /api/v1/customers/ | 
*CustomerApi* | [**updateCustomer**](docs/Api/CustomerApi.md#updatecustomer) | **PUT** /api/v1/customers/{customer_id} | 
*CustomerCommunicationApi* | [**createCommunication**](docs/Api/CustomerCommunicationApi.md#createcommunication) | **POST** /api/v1/communications | 
*CustomerCommunicationApi* | [**customercommunicationRestore**](docs/Api/CustomerCommunicationApi.md#customercommunicationrestore) | **POST** /api/v1/communications/{communication_id}/restore | 
*CustomerCommunicationApi* | [**deleteCommunication**](docs/Api/CustomerCommunicationApi.md#deletecommunication) | **DELETE** /api/v1/communications/{communication_id} | 
*CustomerCommunicationApi* | [**getCommunication**](docs/Api/CustomerCommunicationApi.md#getcommunication) | **GET** /api/v1/communications/{communication_id} | 
*CustomerCommunicationApi* | [**getContactHistory**](docs/Api/CustomerCommunicationApi.md#getcontacthistory) | **GET** /api/v1/contacts/{contact_id}/communications | 
*CustomerCommunicationApi* | [**listCommunications**](docs/Api/CustomerCommunicationApi.md#listcommunications) | **GET** /api/v1/communications/ | 
*CustomerCommunicationApi* | [**updateCommunication**](docs/Api/CustomerCommunicationApi.md#updatecommunication) | **PUT** /api/v1/communications/{communication_id} | 
*CustomerGroupApi* | [**addGroupMembers**](docs/Api/CustomerGroupApi.md#addgroupmembers) | **POST** /api/v1/customer-groups/{customer_group_id}/members | 
*CustomerGroupApi* | [**createCustomerGroup**](docs/Api/CustomerGroupApi.md#createcustomergroup) | **POST** /api/v1/customer-groups | 
*CustomerGroupApi* | [**deleteCustomerGroup**](docs/Api/CustomerGroupApi.md#deletecustomergroup) | **DELETE** /api/v1/customer-groups/{customer_group_id} | 
*CustomerGroupApi* | [**getCustomerGroup**](docs/Api/CustomerGroupApi.md#getcustomergroup) | **GET** /api/v1/customer-groups/{customer_group_id} | 
*CustomerGroupApi* | [**listCustomerGroups**](docs/Api/CustomerGroupApi.md#listcustomergroups) | **GET** /api/v1/customer-groups/ | 
*CustomerGroupApi* | [**updateCustomerGroup**](docs/Api/CustomerGroupApi.md#updatecustomergroup) | **PUT** /api/v1/customer-groups/{customer_group_id} | 
*DatevApi* | [**datevExportApi**](docs/Api/DatevApi.md#datevexportapi) | **GET** /api/v1/bookkeeping/datev/export | Export bookkeeping data as DATEV CSV
*DatevApi* | [**datevPreviewApi**](docs/Api/DatevApi.md#datevpreviewapi) | **GET** /api/v1/bookkeeping/datev/preview | Exported_datev_bookings: returns formed bookings for review
*DatevImportApi* | [**datevImportApi**](docs/Api/DatevImportApi.md#datevimportapi) | **POST** /api/v1/bookkeeping/datev/import | 
*DeclarationApi* | [**createDeclaration**](docs/Api/DeclarationApi.md#createdeclaration) | **POST** /api/v1/declarations | 
*DeclarationApi* | [**declarationRestore**](docs/Api/DeclarationApi.md#declarationrestore) | **POST** /api/v1/declarations/{id}/restore | 
*DeclarationApi* | [**deleteDeclaration**](docs/Api/DeclarationApi.md#deletedeclaration) | **DELETE** /api/v1/declarations/{id} | 
*DeclarationApi* | [**getDeclaration**](docs/Api/DeclarationApi.md#getdeclaration) | **GET** /api/v1/declarations/{id} | 
*DeclarationApi* | [**getDeclarations**](docs/Api/DeclarationApi.md#getdeclarations) | **GET** /api/v1/declarations/ | 
*DeclarationApi* | [**updateDeclaration**](docs/Api/DeclarationApi.md#updatedeclaration) | **PUT** /api/v1/declarations/{id} | 
*DeliveryAppointmentApi* | [**createDeliveryAppointment**](docs/Api/DeliveryAppointmentApi.md#createdeliveryappointment) | **POST** /api/v1/delivery-appointments | 
*DeliveryAppointmentApi* | [**deleteDeliveryAppointment**](docs/Api/DeliveryAppointmentApi.md#deletedeliveryappointment) | **DELETE** /api/v1/delivery-appointments/{appointment_id} | 
*DeliveryAppointmentApi* | [**getDeliveryAppointment**](docs/Api/DeliveryAppointmentApi.md#getdeliveryappointment) | **GET** /api/v1/delivery-appointments/{appointment_id} | 
*DeliveryAppointmentApi* | [**getPublicDeliveryAppointmentStatus**](docs/Api/DeliveryAppointmentApi.md#getpublicdeliveryappointmentstatus) | **GET** /api/v1/public/delivery-appointments/status | Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
*DeliveryAppointmentApi* | [**listDeliveryAppointments**](docs/Api/DeliveryAppointmentApi.md#listdeliveryappointments) | **GET** /api/v1/delivery-appointments | 
*DeliveryAppointmentApi* | [**requestPublicDeliveryAppointment**](docs/Api/DeliveryAppointmentApi.md#requestpublicdeliveryappointment) | **POST** /api/v1/public/delivery-appointments/request | Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by &#x60;code&#x60; — never from the request.
*DeliveryAppointmentApi* | [**updateDeliveryAppointment**](docs/Api/DeliveryAppointmentApi.md#updatedeliveryappointment) | **PUT** /api/v1/delivery-appointments/{appointment_id} | 
*DeliveryAppointmentApi* | [**updateDeliveryAppointmentStatus**](docs/Api/DeliveryAppointmentApi.md#updatedeliveryappointmentstatus) | **PUT** /api/v1/delivery-appointments/{appointment_id}/status | 
*DeliveryDateApi* | [**createDeliveryDate**](docs/Api/DeliveryDateApi.md#createdeliverydate) | **POST** /api/v1/delivery-dates | 
*DeliveryDateApi* | [**deleteDeliveryDate**](docs/Api/DeliveryDateApi.md#deletedeliverydate) | **DELETE** /api/v1/delivery-dates/{delivery_date_id} | 
*DeliveryDateApi* | [**getDeliveryDate**](docs/Api/DeliveryDateApi.md#getdeliverydate) | **GET** /api/v1/delivery-dates/{delivery_date_id} | 
*DeliveryDateApi* | [**getDeliveryPerformance**](docs/Api/DeliveryDateApi.md#getdeliveryperformance) | **GET** /api/v1/delivery-dates/performance | On-time performance summary: how many promised delivery dates were met within a period.
*DeliveryDateApi* | [**listDeliveryDates**](docs/Api/DeliveryDateApi.md#listdeliverydates) | **GET** /api/v1/delivery-dates/ | 
*DeliveryDateApi* | [**updateDeliveryDate**](docs/Api/DeliveryDateApi.md#updatedeliverydate) | **PUT** /api/v1/delivery-dates/{delivery_date_id} | 
*DeliveryDateApi* | [**updateDeliveryDateStatus**](docs/Api/DeliveryDateApi.md#updatedeliverydatestatus) | **PUT** /api/v1/delivery-dates/{delivery_date_id}/status | 
*DeliveryNoteApi* | [**createDeliveryNote**](docs/Api/DeliveryNoteApi.md#createdeliverynote) | **POST** /api/v1/delivery-notes | 
*DeliveryNoteApi* | [**deleteDeliveryNote**](docs/Api/DeliveryNoteApi.md#deletedeliverynote) | **DELETE** /api/v1/delivery-notes/{delivery_note_id} | 
*DeliveryNoteApi* | [**deliverynoteRestore**](docs/Api/DeliveryNoteApi.md#deliverynoterestore) | **POST** /api/v1/delivery-notes/{delivery_note_id}/restore | 
*DeliveryNoteApi* | [**downloadDeliveryNotePdf**](docs/Api/DeliveryNoteApi.md#downloaddeliverynotepdf) | **GET** /api/v1/delivery-notes/{delivery_note_id}/pdf | 
*DeliveryNoteApi* | [**getDeliveryNote**](docs/Api/DeliveryNoteApi.md#getdeliverynote) | **GET** /api/v1/delivery-notes/{delivery_note_id} | 
*DeliveryNoteApi* | [**listDeliveryNotes**](docs/Api/DeliveryNoteApi.md#listdeliverynotes) | **GET** /api/v1/delivery-notes/ | 
*DeliveryNoteApi* | [**pursueDeliveryNote**](docs/Api/DeliveryNoteApi.md#pursuedeliverynote) | **POST** /api/v1/delivery-notes/{delivery_note_id}/pursue | 
*DownPaymentInvoiceApi* | [**downloadDownPaymentInvoicePdf**](docs/Api/DownPaymentInvoiceApi.md#downloaddownpaymentinvoicepdf) | **GET** /api/v1/down-payment-invoices/{id}/pdf | 
*DownPaymentInvoiceApi* | [**getDownPaymentInvoice**](docs/Api/DownPaymentInvoiceApi.md#getdownpaymentinvoice) | **GET** /api/v1/down-payment-invoices/{id} | 
*DownPaymentInvoiceApi* | [**listDownPaymentInvoices**](docs/Api/DownPaymentInvoiceApi.md#listdownpaymentinvoices) | **GET** /api/v1/down-payment-invoices/ | 
*EbilanzApi* | [**ebilanzReportApi**](docs/Api/EbilanzApi.md#ebilanzreportapi) | **GET** /api/v1/bookkeeping/ebilanz | 
*EbilanzApi* | [**ebilanzXbrlExportApi**](docs/Api/EbilanzApi.md#ebilanzxbrlexportapi) | **GET** /api/v1/bookkeeping/ebilanz/xbrl | 
*EmailTemplateApi* | [**createEmailTemplate**](docs/Api/EmailTemplateApi.md#createemailtemplate) | **POST** /api/v1/email-templates | 
*EmailTemplateApi* | [**deleteEmailTemplate**](docs/Api/EmailTemplateApi.md#deleteemailtemplate) | **DELETE** /api/v1/email-templates/{email_template_id} | 
*EmailTemplateApi* | [**getEmailTemplate**](docs/Api/EmailTemplateApi.md#getemailtemplate) | **GET** /api/v1/email-templates/{email_template_id} | 
*EmailTemplateApi* | [**listEmailTemplates**](docs/Api/EmailTemplateApi.md#listemailtemplates) | **GET** /api/v1/email-templates/ | 
*EmailTemplateApi* | [**renderEmailTemplate**](docs/Api/EmailTemplateApi.md#renderemailtemplate) | **POST** /api/v1/email-templates/{email_template_id}/render | 
*EmailTemplateApi* | [**updateEmailTemplate**](docs/Api/EmailTemplateApi.md#updateemailtemplate) | **PUT** /api/v1/email-templates/{email_template_id} | 
*EmissionsApi* | [**createEmissionEntryApi**](docs/Api/EmissionsApi.md#createemissionentryapi) | **POST** /api/v1/bookkeeping/emissions/entries | 
*EmissionsApi* | [**createEmissionTargetApi**](docs/Api/EmissionsApi.md#createemissiontargetapi) | **POST** /api/v1/bookkeeping/emissions/targets | 
*EmissionsApi* | [**deleteEmissionEntryApi**](docs/Api/EmissionsApi.md#deleteemissionentryapi) | **DELETE** /api/v1/bookkeeping/emissions/entries/{id} | 
*EmissionsApi* | [**deleteEmissionTargetApi**](docs/Api/EmissionsApi.md#deleteemissiontargetapi) | **DELETE** /api/v1/bookkeeping/emissions/targets/{id} | 
*EmissionsApi* | [**emissionsEntriesApi**](docs/Api/EmissionsApi.md#emissionsentriesapi) | **GET** /api/v1/bookkeeping/emissions/entries | 
*EmissionsApi* | [**emissionsExportApi**](docs/Api/EmissionsApi.md#emissionsexportapi) | **GET** /api/v1/bookkeeping/emissions/export | 
*EmissionsApi* | [**emissionsFactorsApi**](docs/Api/EmissionsApi.md#emissionsfactorsapi) | **GET** /api/v1/bookkeeping/emissions/factors | 
*EmissionsApi* | [**emissionsReportApi**](docs/Api/EmissionsApi.md#emissionsreportapi) | **GET** /api/v1/bookkeeping/emissions/report | 
*EmissionsApi* | [**emissionsTargetsApi**](docs/Api/EmissionsApi.md#emissionstargetsapi) | **GET** /api/v1/bookkeeping/emissions/targets | 
*EmployeeApi* | [**createEmployee**](docs/Api/EmployeeApi.md#createemployee) | **POST** /api/v1/employees | 
*EmployeeApi* | [**deleteEmployee**](docs/Api/EmployeeApi.md#deleteemployee) | **DELETE** /api/v1/employees/{id} | 
*EmployeeApi* | [**employeeRestore**](docs/Api/EmployeeApi.md#employeerestore) | **POST** /api/v1/employees/{id}/restore | 
*EmployeeApi* | [**getEmployee**](docs/Api/EmployeeApi.md#getemployee) | **GET** /api/v1/employees/{id} | 
*EmployeeApi* | [**getEmployeePayrollSummary**](docs/Api/EmployeeApi.md#getemployeepayrollsummary) | **GET** /api/v1/employees/{id}/payroll-summary | 
*EmployeeApi* | [**getEmployees**](docs/Api/EmployeeApi.md#getemployees) | **GET** /api/v1/employees/ | 
*EmployeeApi* | [**updateEmployee**](docs/Api/EmployeeApi.md#updateemployee) | **PUT** /api/v1/employees/{id} | 
*EuerApi* | [**euerApi**](docs/Api/EuerApi.md#euerapi) | **GET** /api/v1/bookkeeping/euer | 
*EuerApi* | [**euerKategorienApi**](docs/Api/EuerApi.md#euerkategorienapi) | **GET** /api/v1/bookkeeping/euer/kategorien | 
*EventSubscriptionApi* | [**createEventSubscription**](docs/Api/EventSubscriptionApi.md#createeventsubscription) | **POST** /api/v1/event-subscriptions | 
*EventSubscriptionApi* | [**deleteEventSubscription**](docs/Api/EventSubscriptionApi.md#deleteeventsubscription) | **DELETE** /api/v1/event-subscriptions/{subscription_id} | 
*EventSubscriptionApi* | [**listEventSubscriptions**](docs/Api/EventSubscriptionApi.md#listeventsubscriptions) | **GET** /api/v1/event-subscriptions/ | 
*FristenApi* | [**fristenApi**](docs/Api/FristenApi.md#fristenapi) | **GET** /api/v1/bookkeeping/fristen | 
*GdprApi* | [**acceptDpa**](docs/Api/GdprApi.md#acceptdpa) | **PUT** /api/v1/gdpr/dpa | Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).
*GdprApi* | [**accountErasure**](docs/Api/GdprApi.md#accounterasure) | **POST** /api/v1/gdpr/account-erasure | Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).
*GdprApi* | [**erasureContact**](docs/Api/GdprApi.md#erasurecontact) | **POST** /api/v1/gdpr/erasure/{contact_id} | Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on &#x60;contacts&#x60; already records who/when.
*GdprApi* | [**exportContactData**](docs/Api/GdprApi.md#exportcontactdata) | **GET** /api/v1/gdpr/export/{contact_id} | Art. 15 data-subject access export for a contact.
*GdprApi* | [**exportGdpr**](docs/Api/GdprApi.md#exportgdpr) | **GET** /api/v1/gdpr/export | Export the current user&#39;s personal data (GDPR Art. 15/20).
*GdprApi* | [**getDpa**](docs/Api/GdprApi.md#getdpa) | **GET** /api/v1/gdpr/dpa | Current DPA acceptance status (from tenant_settings).
*GenerateQrcodeApi* | [**generateQrcodeApi**](docs/Api/GenerateQrcodeApi.md#generateqrcodeapi) | **GET** /api/v1/invoices/{id}/qrcode | 
*GenerateXrechnungApi* | [**generateXrechnungApi**](docs/Api/GenerateXrechnungApi.md#generatexrechnungapi) | **GET** /api/v1/invoices/{id}/xrechnung | 
*GewerbesteuerApi* | [**gewerbesteuerApi**](docs/Api/GewerbesteuerApi.md#gewerbesteuerapi) | **GET** /api/v1/bookkeeping/gewerbesteuer | 
*GewinnverwendungApi* | [**gewinnverwendungApi**](docs/Api/GewinnverwendungApi.md#gewinnverwendungapi) | **GET** /api/v1/bookkeeping/gewinnverwendung | 
*GewinnverwendungApi* | [**gewinnverwendungExportApi**](docs/Api/GewinnverwendungApi.md#gewinnverwendungexportapi) | **GET** /api/v1/bookkeeping/gewinnverwendung/export | 
*GezApi* | [**gezApi**](docs/Api/GezApi.md#gezapi) | **GET** /api/v1/bookkeeping/gez | 
*GobdExportApi* | [**buchhalterCsvApi**](docs/Api/GobdExportApi.md#buchhaltercsvapi) | **GET** /api/v1/bookkeeping/buchhalter-csv | 
*GobdExportApi* | [**gobdExportApi**](docs/Api/GobdExportApi.md#gobdexportapi) | **GET** /api/v1/bookkeeping/gobd | GoBD/GDPdU export. Default: ZIP archive (&#x60;index.xml&#x60; + CSV tables, IDEA format). &#x60;?format&#x3D;csv&#x60; returns the legacy single-journal CSV as JSON.
*GoodsReceiptApi* | [**createGoodsReceipt**](docs/Api/GoodsReceiptApi.md#creategoodsreceipt) | **POST** /api/v1/goods-receipts | 
*GoodsReceiptApi* | [**deleteGoodsReceipt**](docs/Api/GoodsReceiptApi.md#deletegoodsreceipt) | **DELETE** /api/v1/goods-receipts/{goods_receipt_id} | 
*GoodsReceiptApi* | [**getGoodsReceipt**](docs/Api/GoodsReceiptApi.md#getgoodsreceipt) | **GET** /api/v1/goods-receipts/{goods_receipt_id} | 
*GoodsReceiptApi* | [**listGoodsReceipts**](docs/Api/GoodsReceiptApi.md#listgoodsreceipts) | **GET** /api/v1/goods-receipts/ | 
*GroupFigureApi* | [**createGroupFigure**](docs/Api/GroupFigureApi.md#creategroupfigure) | **POST** /api/v1/group-figures | 
*GroupFigureApi* | [**deleteGroupFigure**](docs/Api/GroupFigureApi.md#deletegroupfigure) | **DELETE** /api/v1/group-figures/{year} | 
*GroupFigureApi* | [**getGroupFigure**](docs/Api/GroupFigureApi.md#getgroupfigure) | **GET** /api/v1/group-figures/{year} | 
*GroupFigureApi* | [**getGroupFigures**](docs/Api/GroupFigureApi.md#getgroupfigures) | **GET** /api/v1/group-figures/ | 
*GroupFigureApi* | [**updateGroupFigure**](docs/Api/GroupFigureApi.md#updategroupfigure) | **PUT** /api/v1/group-figures/{year} | 
*ImportRunnerApi* | [**getImportStatus**](docs/Api/ImportRunnerApi.md#getimportstatus) | **GET** /api/v1/import/{job_id} | 
*ImportRunnerApi* | [**startImport**](docs/Api/ImportRunnerApi.md#startimport) | **POST** /api/v1/import/start | 
*ImportRunnerApi* | [**testImportConnection**](docs/Api/ImportRunnerApi.md#testimportconnection) | **POST** /api/v1/import/test | 
*InstituteApi* | [**instituteStatusApi**](docs/Api/InstituteApi.md#institutestatusapi) | **GET** /api/v1/bookkeeping/institute/status | 
*InstituteProfileApi* | [**getInstituteProfile**](docs/Api/InstituteProfileApi.md#getinstituteprofile) | **GET** /api/v1/institute-profile | Current institute profile (created with defaults when missing).
*InstituteProfileApi* | [**updateInstituteProfile**](docs/Api/InstituteProfileApi.md#updateinstituteprofile) | **PUT** /api/v1/institute-profile | Update the institute profile (institute_type and/or kapitalmarktorientiert).
*InventoryCountApi* | [**createInventoryCount**](docs/Api/InventoryCountApi.md#createinventorycount) | **POST** /api/v1/inventory-counts | 
*InventoryCountApi* | [**deleteInventoryCount**](docs/Api/InventoryCountApi.md#deleteinventorycount) | **DELETE** /api/v1/inventory-counts/{inventory_count_id} | 
*InventoryCountApi* | [**generateInventoryCount**](docs/Api/InventoryCountApi.md#generateinventorycount) | **POST** /api/v1/inventory-counts/generate | 
*InventoryCountApi* | [**getInventoryCount**](docs/Api/InventoryCountApi.md#getinventorycount) | **GET** /api/v1/inventory-counts/{inventory_count_id} | 
*InventoryCountApi* | [**listInventoryCounts**](docs/Api/InventoryCountApi.md#listinventorycounts) | **GET** /api/v1/inventory-counts/ | 
*InventoryCountApi* | [**updateInventoryCount**](docs/Api/InventoryCountApi.md#updateinventorycount) | **PUT** /api/v1/inventory-counts/{inventory_count_id} | 
*InventoryCountApi* | [**updateInventoryCountStatus**](docs/Api/InventoryCountApi.md#updateinventorycountstatus) | **PUT** /api/v1/inventory-counts/{inventory_count_id}/status | 
*InventoryValueApi* | [**getInventoryValueApi**](docs/Api/InventoryValueApi.md#getinventoryvalueapi) | **GET** /api/v1/bookkeeping/inventory-value | 
*InventoryValueApi* | [**recordInventoryValueApi**](docs/Api/InventoryValueApi.md#recordinventoryvalueapi) | **POST** /api/v1/bookkeeping/inventory-value/record | 
*InvoiceApi* | [**createInvoice**](docs/Api/InvoiceApi.md#createinvoice) | **POST** /api/v1/invoices | 
*InvoiceApi* | [**deleteInvoice**](docs/Api/InvoiceApi.md#deleteinvoice) | **DELETE** /api/v1/invoices/{id} | 
*InvoiceApi* | [**downloadInvoicePdf**](docs/Api/InvoiceApi.md#downloadinvoicepdf) | **GET** /api/v1/invoices/{id}/pdf | 
*InvoiceApi* | [**getInvoice**](docs/Api/InvoiceApi.md#getinvoice) | **GET** /api/v1/invoices/{id} | 
*InvoiceApi* | [**getInvoicePdfUrl**](docs/Api/InvoiceApi.md#getinvoicepdfurl) | **GET** /api/v1/invoices/{id}/pdf-url | 
*InvoiceApi* | [**getInvoices**](docs/Api/InvoiceApi.md#getinvoices) | **GET** /api/v1/invoices/ | 
*InvoiceApi* | [**invoiceRestore**](docs/Api/InvoiceApi.md#invoicerestore) | **POST** /api/v1/invoices/{id}/restore | 
*InvoiceApi* | [**updateInvoice**](docs/Api/InvoiceApi.md#updateinvoice) | **PUT** /api/v1/invoices/{id} | 
*JobApplicationApi* | [**applyPublic**](docs/Api/JobApplicationApi.md#applypublic) | **POST** /api/v1/public/jobs/{posting_id}/apply | 
*JobApplicationApi* | [**deleteJobApplication**](docs/Api/JobApplicationApi.md#deletejobapplication) | **DELETE** /api/v1/job-applications/{application_id} | 
*JobApplicationApi* | [**downloadCv**](docs/Api/JobApplicationApi.md#downloadcv) | **GET** /api/v1/job-applications/{application_id}/cv | 
*JobApplicationApi* | [**getJobApplication**](docs/Api/JobApplicationApi.md#getjobapplication) | **GET** /api/v1/job-applications/{application_id} | 
*JobApplicationApi* | [**inboundEmail**](docs/Api/JobApplicationApi.md#inboundemail) | **POST** /api/v1/public/jobs/inbound-email | Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with &#x60;from&#x60;, &#x60;subject&#x60;, &#x60;body-plain&#x60; and one or more &#x60;attachment-N&#x60; file fields. The subject may reference a posting as &#x60;[JOB-&lt;posting_id&gt;]&#x60;; without one the application lands in the general inbox.
*JobApplicationApi* | [**listJobApplications**](docs/Api/JobApplicationApi.md#listjobapplications) | **GET** /api/v1/job-applications | 
*JobApplicationApi* | [**listPublicPostings**](docs/Api/JobApplicationApi.md#listpublicpostings) | **GET** /api/v1/public/jobs | 
*JobApplicationApi* | [**scoreJobApplication**](docs/Api/JobApplicationApi.md#scorejobapplication) | **POST** /api/v1/job-applications/{application_id}/score | 
*JobApplicationApi* | [**updateJobApplicationStatus**](docs/Api/JobApplicationApi.md#updatejobapplicationstatus) | **PATCH** /api/v1/job-applications/{application_id}/status | 
*JobPostingApi* | [**createJobPosting**](docs/Api/JobPostingApi.md#createjobposting) | **POST** /api/v1/job-postings | 
*JobPostingApi* | [**deleteJobPosting**](docs/Api/JobPostingApi.md#deletejobposting) | **DELETE** /api/v1/job-postings/{id} | 
*JobPostingApi* | [**getJobPosting**](docs/Api/JobPostingApi.md#getjobposting) | **GET** /api/v1/job-postings/{id} | 
*JobPostingApi* | [**listJobPostings**](docs/Api/JobPostingApi.md#listjobpostings) | **GET** /api/v1/job-postings | 
*JobPostingApi* | [**updateJobPosting**](docs/Api/JobPostingApi.md#updatejobposting) | **PUT** /api/v1/job-postings/{id} | 
*KonzernApi* | [**konzernExportApi**](docs/Api/KonzernApi.md#konzernexportapi) | **GET** /api/v1/bookkeeping/konzern/status/export | 
*KonzernApi* | [**konzernStatusApi**](docs/Api/KonzernApi.md#konzernstatusapi) | **GET** /api/v1/bookkeeping/konzern/status | 
*KostenVorschauApi* | [**kostenVorschauApi**](docs/Api/KostenVorschauApi.md#kostenvorschauapi) | **GET** /api/v1/bookkeeping/kosten-vorschau | 
*KstApi* | [**kstApi**](docs/Api/KstApi.md#kstapi) | **GET** /api/v1/bookkeeping/kst | 
*KycRecordApi* | [**createKycRecord**](docs/Api/KycRecordApi.md#createkycrecord) | **POST** /api/v1/kyc-records | 
*KycRecordApi* | [**deleteKycRecord**](docs/Api/KycRecordApi.md#deletekycrecord) | **DELETE** /api/v1/kyc-records/{id} | 
*KycRecordApi* | [**getKycRecord**](docs/Api/KycRecordApi.md#getkycrecord) | **GET** /api/v1/kyc-records/{id} | 
*KycRecordApi* | [**getKycRecords**](docs/Api/KycRecordApi.md#getkycrecords) | **GET** /api/v1/kyc-records/ | 
*KycRecordApi* | [**updateKycRecord**](docs/Api/KycRecordApi.md#updatekycrecord) | **PUT** /api/v1/kyc-records/{id} | 
*LeadApi* | [**listLeadsApi**](docs/Api/LeadApi.md#listleadsapi) | **GET** /api/v1/support/leads | 
*LeadApi* | [**updateLeadApi**](docs/Api/LeadApi.md#updateleadapi) | **PUT** /api/v1/support/leads/{lead_id} | 
*LegalDocumentApi* | [**getLegalDocuments**](docs/Api/LegalDocumentApi.md#getlegaldocuments) | **GET** /api/v1/legal/documents | List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.
*LegalDocumentApi* | [**resetLegalDocuments**](docs/Api/LegalDocumentApi.md#resetlegaldocuments) | **POST** /api/v1/legal/documents/reset | Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.
*LegalDocumentApi* | [**upsertLegalDocuments**](docs/Api/LegalDocumentApi.md#upsertlegaldocuments) | **PUT** /api/v1/legal/documents | Upsert legal documents per (doc_type, lang). Returns the full tenant list.
*ListOpenItemsApi* | [**listOpenItemsApi**](docs/Api/ListOpenItemsApi.md#listopenitemsapi) | **GET** /api/v1/bookkeeping/open-items | 
*MarketplaceApiApi* | [**createConnectionApi**](docs/Api/MarketplaceApiApi.md#createconnectionapi) | **POST** /api/v1/marketplace/connections | Create a new connection (for API-key based platforms)
*MarketplaceApiApi* | [**deleteConnectionApi**](docs/Api/MarketplaceApiApi.md#deleteconnectionapi) | **DELETE** /api/v1/marketplace/connections/{connection_id} | Soft-delete a connection
*MarketplaceApiApi* | [**getConnectionApi**](docs/Api/MarketplaceApiApi.md#getconnectionapi) | **GET** /api/v1/marketplace/connections/{connection_id} | Get a single connection
*MarketplaceApiApi* | [**getSyncDirectionApi**](docs/Api/MarketplaceApiApi.md#getsyncdirectionapi) | **GET** /api/v1/marketplace/connections/{connection_id}/directions | Get current sync direction configuration for a connection
*MarketplaceApiApi* | [**getSyncLogsApi**](docs/Api/MarketplaceApiApi.md#getsynclogsapi) | **GET** /api/v1/marketplace/connections/{connection_id}/logs | Get sync logs for a connection
*MarketplaceApiApi* | [**listConnectionsApi**](docs/Api/MarketplaceApiApi.md#listconnectionsapi) | **GET** /api/v1/marketplace/connections | List connections for the current tenant
*MarketplaceApiApi* | [**listPlatformsApi**](docs/Api/MarketplaceApiApi.md#listplatformsapi) | **GET** /api/v1/marketplace/platforms | List all supported platforms
*MarketplaceApiApi* | [**oauthAuthorizeApi**](docs/Api/MarketplaceApiApi.md#oauthauthorizeapi) | **POST** /api/v1/marketplace/oauth/authorize | OAuth: initiate authorization flow
*MarketplaceApiApi* | [**oauthCallbackApi**](docs/Api/MarketplaceApiApi.md#oauthcallbackapi) | **POST** /api/v1/marketplace/oauth/callback | OAuth: handle callback after authorization
*MarketplaceApiApi* | [**triggerSyncApi**](docs/Api/MarketplaceApiApi.md#triggersyncapi) | **POST** /api/v1/marketplace/connections/{connection_id}/sync | Trigger sync for a connection
*MarketplaceApiApi* | [**updateConnectionApi**](docs/Api/MarketplaceApiApi.md#updateconnectionapi) | **PUT** /api/v1/marketplace/connections/{connection_id} | Update a connection
*MarketplaceApiApi* | [**updateSyncDirectionApi**](docs/Api/MarketplaceApiApi.md#updatesyncdirectionapi) | **PUT** /api/v1/marketplace/connections/{connection_id}/directions | Update per-entity sync direction configuration for a connection
*MarketplaceApiApi* | [**webhookReceiverApi**](docs/Api/MarketplaceApiApi.md#webhookreceiverapi) | **POST** /api/v1/marketplace/webhook/{platform}/{connection_id} | Webhook receiver
*NotificationsApi* | [**deleteNotification**](docs/Api/NotificationsApi.md#deletenotification) | **DELETE** /api/v1/notifications/{id} | 
*NotificationsApi* | [**listNotifications**](docs/Api/NotificationsApi.md#listnotifications) | **GET** /api/v1/notifications | 
*NotificationsApi* | [**markAllRead**](docs/Api/NotificationsApi.md#markallread) | **PUT** /api/v1/notifications/read-all | 
*NotificationsApi* | [**markAsRead**](docs/Api/NotificationsApi.md#markasread) | **PUT** /api/v1/notifications/{id}/read | 
*NotificationsApi* | [**unreadCount**](docs/Api/NotificationsApi.md#unreadcount) | **GET** /api/v1/notifications/unread-count | 
*OffenlegungApi* | [**offenlegungApi**](docs/Api/OffenlegungApi.md#offenlegungapi) | **GET** /api/v1/bookkeeping/offenlegung | 
*OnlineshopApi* | [**getSmtpConfigApi**](docs/Api/OnlineshopApi.md#getsmtpconfigapi) | **GET** /api/v1/settings/smtp | 
*OnlineshopApi* | [**saveSmtpConfigApi**](docs/Api/OnlineshopApi.md#savesmtpconfigapi) | **PUT** /api/v1/settings/smtp | 
*OrderApi* | [**addOrderTags**](docs/Api/OrderApi.md#addordertags) | **POST** /api/v1/orders/{order_id}/tags | 
*OrderApi* | [**findOrderByExternalRef**](docs/Api/OrderApi.md#findorderbyexternalref) | **GET** /api/v1/orders/by-ext-ref/{ext_ref} | 
*OrderApi* | [**getOrder**](docs/Api/OrderApi.md#getorder) | **GET** /api/v1/order/{order_number} | 
*OrderApi* | [**getOrders**](docs/Api/OrderApi.md#getorders) | **GET** /api/v1/orders | 
*OrderApi* | [**patchOrder**](docs/Api/OrderApi.md#patchorder) | **PATCH** /api/v1/orders/{order_id} | 
*OrderApi* | [**replaceOrderTags**](docs/Api/OrderApi.md#replaceordertags) | **PUT** /api/v1/orders/{order_id}/tags | 
*OrderApi* | [**updateOrderState**](docs/Api/OrderApi.md#updateorderstate) | **PUT** /api/v1/orders/{order_id}/state | 
*OrderConfirmationApi* | [**createConfirmation**](docs/Api/OrderConfirmationApi.md#createconfirmation) | **POST** /api/v1/order-confirmations | 
*OrderConfirmationApi* | [**deleteConfirmation**](docs/Api/OrderConfirmationApi.md#deleteconfirmation) | **DELETE** /api/v1/order-confirmations/{confirmation_id} | 
*OrderConfirmationApi* | [**downloadConfirmationPdf**](docs/Api/OrderConfirmationApi.md#downloadconfirmationpdf) | **GET** /api/v1/order-confirmations/{confirmation_id}/pdf | 
*OrderConfirmationApi* | [**getConfirmation**](docs/Api/OrderConfirmationApi.md#getconfirmation) | **GET** /api/v1/order-confirmations/{confirmation_id} | 
*OrderConfirmationApi* | [**listConfirmations**](docs/Api/OrderConfirmationApi.md#listconfirmations) | **GET** /api/v1/order-confirmations/ | 
*OrderConfirmationApi* | [**orderconfirmationRestore**](docs/Api/OrderConfirmationApi.md#orderconfirmationrestore) | **POST** /api/v1/order-confirmations/{confirmation_id}/restore | 
*OrderConfirmationApi* | [**pursueConfirmation**](docs/Api/OrderConfirmationApi.md#pursueconfirmation) | **POST** /api/v1/order-confirmations/{confirmation_id}/pursue | 
*OssReportApi* | [**ossReportApi**](docs/Api/OssReportApi.md#ossreportapi) | **GET** /api/v1/bookkeeping/oss | 
*PackingApi* | [**completePacking**](docs/Api/PackingApi.md#completepacking) | **POST** /api/v1/packing/{order_number}/complete | Mark packing as complete and transition order to shipped
*PackingApi* | [**getPackingQueue**](docs/Api/PackingApi.md#getpackingqueue) | **GET** /api/v1/packing/queue | Get the packing queue - orders ready for packing
*PackingApi* | [**printDeliveryNote**](docs/Api/PackingApi.md#printdeliverynote) | **POST** /api/v1/packing/{order_number}/print-delivery-note | Print delivery note (Lieferschein) for an order
*PackingApi* | [**printLabel**](docs/Api/PackingApi.md#printlabel) | **POST** /api/v1/packing/{order_number}/print-label | Print shipping label for an order
*PackingApi* | [**recordPackingVideo**](docs/Api/PackingApi.md#recordpackingvideo) | **POST** /api/v1/packing/{order_number}/record-video | Record video of packing process
*ParticipationApi* | [**createParticipation**](docs/Api/ParticipationApi.md#createparticipation) | **POST** /api/v1/participations | 
*ParticipationApi* | [**deleteParticipation**](docs/Api/ParticipationApi.md#deleteparticipation) | **DELETE** /api/v1/participations/{id} | 
*ParticipationApi* | [**getParticipation**](docs/Api/ParticipationApi.md#getparticipation) | **GET** /api/v1/participations/{id} | 
*ParticipationApi* | [**getParticipations**](docs/Api/ParticipationApi.md#getparticipations) | **GET** /api/v1/participations/ | 
*ParticipationApi* | [**updateParticipation**](docs/Api/ParticipationApi.md#updateparticipation) | **PUT** /api/v1/participations/{id} | 
*PaygapApi* | [**paygapAuskunftApi**](docs/Api/PaygapApi.md#paygapauskunftapi) | **GET** /api/v1/bookkeeping/paygap/auskunft/{employee_id} | 
*PaygapApi* | [**paygapExportApi**](docs/Api/PaygapApi.md#paygapexportapi) | **GET** /api/v1/bookkeeping/paygap/export | 
*PaygapApi* | [**paygapReportApi**](docs/Api/PaygapApi.md#paygapreportapi) | **GET** /api/v1/bookkeeping/paygap/report | 
*PaymentApi* | [**createPayment**](docs/Api/PaymentApi.md#createpayment) | **POST** /api/v1/payments | 
*PaymentApi* | [**deletePayment**](docs/Api/PaymentApi.md#deletepayment) | **DELETE** /api/v1/payments/{id} | 
*PaymentApi* | [**getPayment**](docs/Api/PaymentApi.md#getpayment) | **GET** /api/v1/payments/{id} | 
*PaymentApi* | [**getPayments**](docs/Api/PaymentApi.md#getpayments) | **GET** /api/v1/payments/ | 
*PaymentApi* | [**paymentRestore**](docs/Api/PaymentApi.md#paymentrestore) | **POST** /api/v1/payments/{id}/restore | 
*PaymentApi* | [**updatePayment**](docs/Api/PaymentApi.md#updatepayment) | **PUT** /api/v1/payments/{id} | 
*PaymentConditionApi* | [**listPaymentConditionsApi**](docs/Api/PaymentConditionApi.md#listpaymentconditionsapi) | **GET** /api/v1/payment-conditions | 
*PaymentGatewayApi* | [**createPaymentGatewayApi**](docs/Api/PaymentGatewayApi.md#createpaymentgatewayapi) | **POST** /api/v1/payment-gateways | 
*PaymentGatewayApi* | [**deletePaymentGatewayApi**](docs/Api/PaymentGatewayApi.md#deletepaymentgatewayapi) | **DELETE** /api/v1/payment-gateways/{gateway_id} | 
*PaymentGatewayApi* | [**listPaymentGatewaysApi**](docs/Api/PaymentGatewayApi.md#listpaymentgatewaysapi) | **GET** /api/v1/payment-gateways/ | 
*PaymentGatewayApi* | [**oauthAuthorizeApi**](docs/Api/PaymentGatewayApi.md#oauthauthorizeapi) | **POST** /api/v1/payment-gateways/oauth/authorize | 
*PaymentGatewayApi* | [**oauthCallbackApi**](docs/Api/PaymentGatewayApi.md#oauthcallbackapi) | **POST** /api/v1/payment-gateways/oauth/callback | 
*PaymentGatewayApi* | [**updatePaymentGatewayApi**](docs/Api/PaymentGatewayApi.md#updatepaymentgatewayapi) | **PUT** /api/v1/payment-gateways/{gateway_id} | 
*PayrollApi* | [**payrollApprove**](docs/Api/PayrollApi.md#payrollapprove) | **POST** /api/v1/payroll/{id}/approve | 
*PayrollApi* | [**payrollAutopay**](docs/Api/PayrollApi.md#payrollautopay) | **POST** /api/v1/payroll/{id}/autopay | 
*PayrollApi* | [**payrollCalculate**](docs/Api/PayrollApi.md#payrollcalculate) | **POST** /api/v1/payroll/{id}/calculate | 
*PayrollApi* | [**payrollCreate**](docs/Api/PayrollApi.md#payrollcreate) | **POST** /api/v1/payroll | 
*PayrollApi* | [**payrollDelete**](docs/Api/PayrollApi.md#payrolldelete) | **DELETE** /api/v1/payroll/{id} | 
*PayrollApi* | [**payrollElsterExport**](docs/Api/PayrollApi.md#payrollelsterexport) | **POST** /api/v1/payroll/{id}/elster-export | 
*PayrollApi* | [**payrollEmail**](docs/Api/PayrollApi.md#payrollemail) | **POST** /api/v1/payroll/{id}/email | 
*PayrollApi* | [**payrollEntryPdf**](docs/Api/PayrollApi.md#payrollentrypdf) | **GET** /api/v1/payroll/{id}/entries/{entry_id}/pdf | 
*PayrollApi* | [**payrollGet**](docs/Api/PayrollApi.md#payrollget) | **GET** /api/v1/payroll/{id} | 
*PayrollApi* | [**payrollList**](docs/Api/PayrollApi.md#payrolllist) | **GET** /api/v1/payroll | 
*PayrollApi* | [**payrollPay**](docs/Api/PayrollApi.md#payrollpay) | **POST** /api/v1/payroll/{id}/pay | 
*PayrollApi* | [**payrollPdf**](docs/Api/PayrollApi.md#payrollpdf) | **GET** /api/v1/payroll/{id}/pdf | 
*PayrollApi* | [**payrollSummary**](docs/Api/PayrollApi.md#payrollsummary) | **GET** /api/v1/payroll/summary/{year} | 
*PayrollApi* | [**payrollSvMeldungen**](docs/Api/PayrollApi.md#payrollsvmeldungen) | **POST** /api/v1/payroll/{id}/sv-meldungen | 
*PeppolApi* | [**peppolApi**](docs/Api/PeppolApi.md#peppolapi) | **GET** /api/v1/invoices/{id}/peppol | 
*PlausibilityApi* | [**plausibilityCheckApi**](docs/Api/PlausibilityApi.md#plausibilitycheckapi) | **GET** /api/v1/bookkeeping/plausibility | 
*PosApi* | [**posBilling**](docs/Api/PosApi.md#posbilling) | **GET** /api/pos/billing | 
*PosApi* | [**posCreateOrder**](docs/Api/PosApi.md#poscreateorder) | **POST** /api/pos/orders | 
*PosApi* | [**posCreateRegister**](docs/Api/PosApi.md#poscreateregister) | **POST** /api/pos/registers | 
*PosApi* | [**posCreateTable**](docs/Api/PosApi.md#poscreatetable) | **POST** /api/pos/tables | 
*PosApi* | [**posDisableRegister**](docs/Api/PosApi.md#posdisableregister) | **POST** /api/pos/registers/{id}/disable | 
*PosApi* | [**posFreeTable**](docs/Api/PosApi.md#posfreetable) | **POST** /api/pos/tables/{id}/free | 
*PosApi* | [**posKasseClosing**](docs/Api/PosApi.md#poskasseclosing) | **POST** /api/pos/kasse/closing | 
*PosApi* | [**posKasseEntries**](docs/Api/PosApi.md#poskasseentries) | **GET** /api/pos/kasse/entries | 
*PosApi* | [**posKasseExport**](docs/Api/PosApi.md#poskasseexport) | **GET** /api/pos/kasse/export | 
*PosApi* | [**posKassePayInOut**](docs/Api/PosApi.md#poskassepayinout) | **POST** /api/pos/kasse/pay-in-out | 
*PosApi* | [**posListOrders**](docs/Api/PosApi.md#poslistorders) | **GET** /api/pos/orders | 
*PosApi* | [**posListProducts**](docs/Api/PosApi.md#poslistproducts) | **GET** /api/pos/products | 
*PosApi* | [**posListRegisters**](docs/Api/PosApi.md#poslistregisters) | **GET** /api/pos/registers | 
*PosApi* | [**posListTables**](docs/Api/PosApi.md#poslisttables) | **GET** /api/pos/tables | 
*PosApi* | [**posOrderPrint**](docs/Api/PosApi.md#posorderprint) | **GET** /api/pos/orders/{order_number}/print | 
*PosApi* | [**posOrderReceipt**](docs/Api/PosApi.md#posorderreceipt) | **GET** /api/pos/orders/{order_number}/receipt | 
*PosApi* | [**posPayOrder**](docs/Api/PosApi.md#pospayorder) | **POST** /api/pos/orders/{order_number}/pay | 
*PosApi* | [**posSumupCheckout**](docs/Api/PosApi.md#possumupcheckout) | **POST** /api/pos/sumup/checkout | 
*PostingCategoryApi* | [**createPostingCategory**](docs/Api/PostingCategoryApi.md#createpostingcategory) | **POST** /api/v1/posting-categories | 
*PostingCategoryApi* | [**deletePostingCategory**](docs/Api/PostingCategoryApi.md#deletepostingcategory) | **DELETE** /api/v1/posting-categories/{category_id} | 
*PostingCategoryApi* | [**listPostingCategories**](docs/Api/PostingCategoryApi.md#listpostingcategories) | **GET** /api/v1/posting-categories | 
*PostingCategoryApi* | [**seedPostingCategories**](docs/Api/PostingCategoryApi.md#seedpostingcategories) | **POST** /api/v1/posting-categories/seed/{skr_version} | 
*PostingCategoryApi* | [**updatePostingCategory**](docs/Api/PostingCategoryApi.md#updatepostingcategory) | **PUT** /api/v1/posting-categories/{category_id} | 
*PriceTierApi* | [**createPriceTier**](docs/Api/PriceTierApi.md#createpricetier) | **POST** /api/v1/price-tiers | 
*PriceTierApi* | [**deletePriceTier**](docs/Api/PriceTierApi.md#deletepricetier) | **DELETE** /api/v1/price-tiers/{price_tier_id} | 
*PriceTierApi* | [**getPriceTier**](docs/Api/PriceTierApi.md#getpricetier) | **GET** /api/v1/price-tiers/{price_tier_id} | 
*PriceTierApi* | [**getResolvedPrice**](docs/Api/PriceTierApi.md#getresolvedprice) | **GET** /api/v1/price-tiers/resolved | 
*PriceTierApi* | [**listPriceTiers**](docs/Api/PriceTierApi.md#listpricetiers) | **GET** /api/v1/price-tiers/ | 
*PriceTierApi* | [**updatePriceTier**](docs/Api/PriceTierApi.md#updatepricetier) | **PUT** /api/v1/price-tiers/{price_tier_id} | 
*ProductApi* | [**createProductApi**](docs/Api/ProductApi.md#createproductapi) | **POST** /api/v1/products | 
*ProductApi* | [**deleteProductApi**](docs/Api/ProductApi.md#deleteproductapi) | **DELETE** /api/v1/products/{product_id} | 
*ProductApi* | [**getProductApi**](docs/Api/ProductApi.md#getproductapi) | **GET** /api/v1/products/{product_id} | 
*ProductApi* | [**getProductStockApi**](docs/Api/ProductApi.md#getproductstockapi) | **GET** /api/v1/products/{product_id}/stock | 
*ProductApi* | [**getProductsApi**](docs/Api/ProductApi.md#getproductsapi) | **GET** /api/v1/products/ | 
*ProductApi* | [**listLowStockProductsApi**](docs/Api/ProductApi.md#listlowstockproductsapi) | **GET** /api/v1/products/low-stock | 
*ProductApi* | [**productRestore**](docs/Api/ProductApi.md#productrestore) | **POST** /api/v1/products/{product_id}/restore | 
*ProductApi* | [**updateProductApi**](docs/Api/ProductApi.md#updateproductapi) | **PUT** /api/v1/products/{product_id} | 
*ProductApi* | [**updateProductStockApi**](docs/Api/ProductApi.md#updateproductstockapi) | **PUT** /api/v1/products/{product_id}/stock | 
*ProductAttributeApi* | [**createProductAttribute**](docs/Api/ProductAttributeApi.md#createproductattribute) | **POST** /api/v1/product-attributes | 
*ProductAttributeApi* | [**deleteProductAttribute**](docs/Api/ProductAttributeApi.md#deleteproductattribute) | **DELETE** /api/v1/product-attributes/{attribute_id} | 
*ProductAttributeApi* | [**getProductAttribute**](docs/Api/ProductAttributeApi.md#getproductattribute) | **GET** /api/v1/product-attributes/{attribute_id} | 
*ProductAttributeApi* | [**listProductAttributes**](docs/Api/ProductAttributeApi.md#listproductattributes) | **GET** /api/v1/product-attributes/ | 
*ProductAttributeApi* | [**updateProductAttribute**](docs/Api/ProductAttributeApi.md#updateproductattribute) | **PUT** /api/v1/product-attributes/{attribute_id} | 
*ProductCategoryApi* | [**createProductCategory**](docs/Api/ProductCategoryApi.md#createproductcategory) | **POST** /api/v1/product-categories | 
*ProductCategoryApi* | [**deleteProductCategory**](docs/Api/ProductCategoryApi.md#deleteproductcategory) | **DELETE** /api/v1/product-categories/{category_id} | 
*ProductCategoryApi* | [**getProductCategory**](docs/Api/ProductCategoryApi.md#getproductcategory) | **GET** /api/v1/product-categories/{category_id} | 
*ProductCategoryApi* | [**listProductCategories**](docs/Api/ProductCategoryApi.md#listproductcategories) | **GET** /api/v1/product-categories | 
*ProductCategoryApi* | [**updateProductCategory**](docs/Api/ProductCategoryApi.md#updateproductcategory) | **PUT** /api/v1/product-categories/{category_id} | 
*ProductVariantApi* | [**createProductVariant**](docs/Api/ProductVariantApi.md#createproductvariant) | **POST** /api/v1/product-variants | 
*ProductVariantApi* | [**deleteProductVariant**](docs/Api/ProductVariantApi.md#deleteproductvariant) | **DELETE** /api/v1/product-variants/{variant_id} | 
*ProductVariantApi* | [**generateProductVariants**](docs/Api/ProductVariantApi.md#generateproductvariants) | **POST** /api/v1/product-variants/generate | 
*ProductVariantApi* | [**getProductVariant**](docs/Api/ProductVariantApi.md#getproductvariant) | **GET** /api/v1/product-variants/{variant_id} | 
*ProductVariantApi* | [**listProductVariants**](docs/Api/ProductVariantApi.md#listproductvariants) | **GET** /api/v1/product-variants/ | 
*ProductVariantApi* | [**updateProductVariant**](docs/Api/ProductVariantApi.md#updateproductvariant) | **PUT** /api/v1/product-variants/{variant_id} | 
*ProductionOrderApi* | [**createProductionOrder**](docs/Api/ProductionOrderApi.md#createproductionorder) | **POST** /api/v1/production-orders | 
*ProductionOrderApi* | [**deleteProductionOrder**](docs/Api/ProductionOrderApi.md#deleteproductionorder) | **DELETE** /api/v1/production-orders/{production_order_id} | 
*ProductionOrderApi* | [**getProductionOrder**](docs/Api/ProductionOrderApi.md#getproductionorder) | **GET** /api/v1/production-orders/{production_order_id} | 
*ProductionOrderApi* | [**listProductionOrders**](docs/Api/ProductionOrderApi.md#listproductionorders) | **GET** /api/v1/production-orders/ | 
*ProductionOrderApi* | [**productionOrderCosting**](docs/Api/ProductionOrderApi.md#productionordercosting) | **GET** /api/v1/production-orders/{production_order_id}/costing | Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product&#39;s sale price.
*ProductionOrderApi* | [**updateProductionOrder**](docs/Api/ProductionOrderApi.md#updateproductionorder) | **PUT** /api/v1/production-orders/{production_order_id} | 
*ProductionOrderApi* | [**updateProductionOrderStatus**](docs/Api/ProductionOrderApi.md#updateproductionorderstatus) | **PUT** /api/v1/production-orders/{production_order_id}/status | 
*ProformaInvoiceApi* | [**convertProformaToInvoice**](docs/Api/ProformaInvoiceApi.md#convertproformatoinvoice) | **POST** /api/v1/proforma-invoices/{proforma_id}/convert | 
*ProformaInvoiceApi* | [**createProformaInvoice**](docs/Api/ProformaInvoiceApi.md#createproformainvoice) | **POST** /api/v1/proforma-invoices | 
*ProformaInvoiceApi* | [**deleteProformaInvoice**](docs/Api/ProformaInvoiceApi.md#deleteproformainvoice) | **DELETE** /api/v1/proforma-invoices/{proforma_id} | 
*ProformaInvoiceApi* | [**getProformaInvoice**](docs/Api/ProformaInvoiceApi.md#getproformainvoice) | **GET** /api/v1/proforma-invoices/{proforma_id} | 
*ProformaInvoiceApi* | [**listProformaInvoices**](docs/Api/ProformaInvoiceApi.md#listproformainvoices) | **GET** /api/v1/proforma-invoices/ | 
*ProformaInvoiceApi* | [**updateProformaInvoice**](docs/Api/ProformaInvoiceApi.md#updateproformainvoice) | **PUT** /api/v1/proforma-invoices/{proforma_id} | 
*ProposeAssignmentsApi* | [**proposeAssignmentsApi**](docs/Api/ProposeAssignmentsApi.md#proposeassignmentsapi) | **GET** /api/v1/bookkeeping/propose-assignments | 
*PublicReturnsApi* | [**getPublicReturnStatus**](docs/Api/PublicReturnsApi.md#getpublicreturnstatus) | **GET** /api/v1/public/returns/status | Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches.
*PublicReturnsApi* | [**listPublicReturns**](docs/Api/PublicReturnsApi.md#listpublicreturns) | **GET** /api/v1/public/returns/list | List all returns for an order (public, no auth).
*PublicReturnsApi* | [**requestPublicReturn**](docs/Api/PublicReturnsApi.md#requestpublicreturn) | **POST** /api/v1/public/returns/request | Customer requests a return for an order (public, no auth).
*PurchaseOrderApi* | [**createPurchaseOrder**](docs/Api/PurchaseOrderApi.md#createpurchaseorder) | **POST** /api/v1/purchase-orders | 
*PurchaseOrderApi* | [**deletePurchaseOrder**](docs/Api/PurchaseOrderApi.md#deletepurchaseorder) | **DELETE** /api/v1/purchase-orders/{purchase_order_id} | 
*PurchaseOrderApi* | [**getPurchaseOrder**](docs/Api/PurchaseOrderApi.md#getpurchaseorder) | **GET** /api/v1/purchase-orders/{purchase_order_id} | 
*PurchaseOrderApi* | [**listPurchaseOrders**](docs/Api/PurchaseOrderApi.md#listpurchaseorders) | **GET** /api/v1/purchase-orders/ | 
*PurchaseOrderApi* | [**matchInvoice**](docs/Api/PurchaseOrderApi.md#matchinvoice) | **POST** /api/v1/purchase-orders/{purchase_order_id}/match-invoice | 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.
*PurchaseOrderApi* | [**updatePurchaseOrder**](docs/Api/PurchaseOrderApi.md#updatepurchaseorder) | **PUT** /api/v1/purchase-orders/{purchase_order_id} | 
*PurchaseOrderApi* | [**updatePurchaseOrderStatus**](docs/Api/PurchaseOrderApi.md#updatepurchaseorderstatus) | **PUT** /api/v1/purchase-orders/{purchase_order_id}/status | 
*QuotationApi* | [**createQuotation**](docs/Api/QuotationApi.md#createquotation) | **POST** /api/v1/quotations | 
*QuotationApi* | [**deleteQuotation**](docs/Api/QuotationApi.md#deletequotation) | **DELETE** /api/v1/quotations/{quotation_id} | 
*QuotationApi* | [**downloadQuotationPdf**](docs/Api/QuotationApi.md#downloadquotationpdf) | **GET** /api/v1/quotations/{quotation_id}/pdf | 
*QuotationApi* | [**getQuotation**](docs/Api/QuotationApi.md#getquotation) | **GET** /api/v1/quotations/{quotation_id} | 
*QuotationApi* | [**listQuotations**](docs/Api/QuotationApi.md#listquotations) | **GET** /api/v1/quotations/ | 
*QuotationApi* | [**pursueQuotation**](docs/Api/QuotationApi.md#pursuequotation) | **POST** /api/v1/quotations/{quotation_id}/pursue | 
*QuotationApi* | [**quotationRestore**](docs/Api/QuotationApi.md#quotationrestore) | **POST** /api/v1/quotations/{quotation_id}/restore | 
*QuotationApi* | [**updateQuotation**](docs/Api/QuotationApi.md#updatequotation) | **PUT** /api/v1/quotations/{quotation_id} | 
*RecurringTemplateApi* | [**createRecurringTemplate**](docs/Api/RecurringTemplateApi.md#createrecurringtemplate) | **POST** /api/v1/recurring-templates | 
*RecurringTemplateApi* | [**deleteRecurringTemplate**](docs/Api/RecurringTemplateApi.md#deleterecurringtemplate) | **DELETE** /api/v1/recurring-templates/{template_id} | 
*RecurringTemplateApi* | [**getRecurringTemplate**](docs/Api/RecurringTemplateApi.md#getrecurringtemplate) | **GET** /api/v1/recurring-templates/{template_id} | 
*RecurringTemplateApi* | [**listRecurringTemplates**](docs/Api/RecurringTemplateApi.md#listrecurringtemplates) | **GET** /api/v1/recurring-templates/ | 
*ReorderProposalApi* | [**applyReorderProposal**](docs/Api/ReorderProposalApi.md#applyreorderproposal) | **POST** /api/v1/reorder-proposals/apply | Convert a reorder proposal into a draft purchase order.
*ReorderProposalApi* | [**getReorderProposal**](docs/Api/ReorderProposalApi.md#getreorderproposal) | **GET** /api/v1/reorder-proposals | 
*ReplenishmentApi* | [**applyReplenishments**](docs/Api/ReplenishmentApi.md#applyreplenishments) | **POST** /api/v1/replenishments/apply | Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
*ReplenishmentApi* | [**getReplenishments**](docs/Api/ReplenishmentApi.md#getreplenishments) | **GET** /api/v1/replenishments | 
*ReportsApi* | [**bilanzReportApi**](docs/Api/ReportsApi.md#bilanzreportapi) | **GET** /api/v1/bookkeeping/reports/bilanz | Bilanz (Balance Sheet)
*ReportsApi* | [**guvReportApi**](docs/Api/ReportsApi.md#guvreportapi) | **GET** /api/v1/bookkeeping/reports/guv | Gewinn- und Verlustrechnung (P&amp;L statement)
*ReportsApi* | [**kontenansichtReportApi**](docs/Api/ReportsApi.md#kontenansichtreportapi) | **GET** /api/v1/bookkeeping/reports/kontenansicht | Kontenansicht (Account Overview)
*ReportsApi* | [**umsatzsteuerReportApi**](docs/Api/ReportsApi.md#umsatzsteuerreportapi) | **GET** /api/v1/bookkeeping/reports/umsatzsteuer | Umsatzsteuer-Voranmeldung (VAT report)
*ReturnOrderApi* | [**createReturnOrder**](docs/Api/ReturnOrderApi.md#createreturnorder) | **POST** /api/v1/returns | 
*ReturnOrderApi* | [**deleteReturnOrder**](docs/Api/ReturnOrderApi.md#deletereturnorder) | **DELETE** /api/v1/returns/{return_order_id} | 
*ReturnOrderApi* | [**getReturnOrder**](docs/Api/ReturnOrderApi.md#getreturnorder) | **GET** /api/v1/returns/{return_order_id} | 
*ReturnOrderApi* | [**listReturnOrders**](docs/Api/ReturnOrderApi.md#listreturnorders) | **GET** /api/v1/returns/ | 
*ReturnOrderApi* | [**returnLogisticsQueue**](docs/Api/ReturnOrderApi.md#returnlogisticsqueue) | **GET** /api/v1/returns/logistics-queue | 
*ReturnOrderApi* | [**returnLogisticsSummary**](docs/Api/ReturnOrderApi.md#returnlogisticssummary) | **GET** /api/v1/returns/logistics-summary | Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.
*ReturnOrderApi* | [**updateReturnOrder**](docs/Api/ReturnOrderApi.md#updatereturnorder) | **PUT** /api/v1/returns/{return_order_id} | 
*ReturnOrderApi* | [**updateReturnOrderStatus**](docs/Api/ReturnOrderApi.md#updatereturnorderstatus) | **PUT** /api/v1/returns/{return_order_id}/status | 
*RfqApi* | [**convertRfq**](docs/Api/RfqApi.md#convertrfq) | **POST** /api/v1/rfqs/{rfq_id}/convert | Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as &#x60;converted&#x60;.
*RfqApi* | [**createRfq**](docs/Api/RfqApi.md#createrfq) | **POST** /api/v1/rfqs | 
*RfqApi* | [**deleteRfq**](docs/Api/RfqApi.md#deleterfq) | **DELETE** /api/v1/rfqs/{rfq_id} | 
*RfqApi* | [**getRfq**](docs/Api/RfqApi.md#getrfq) | **GET** /api/v1/rfqs/{rfq_id} | 
*RfqApi* | [**listRfqs**](docs/Api/RfqApi.md#listrfqs) | **GET** /api/v1/rfqs/ | 
*RfqApi* | [**updateRfq**](docs/Api/RfqApi.md#updaterfq) | **PUT** /api/v1/rfqs/{rfq_id} | 
*RfqApi* | [**updateRfqStatus**](docs/Api/RfqApi.md#updaterfqstatus) | **PUT** /api/v1/rfqs/{rfq_id}/status | 
*SearchApi* | [**globalSearch**](docs/Api/SearchApi.md#globalsearch) | **GET** /api/v1/search | GET /api/v1/search?q&#x3D;...
*SearchApi* | [**myPermissions**](docs/Api/SearchApi.md#mypermissions) | **GET** /api/v1/me/permissions | GET /api/v1/me/permissions — resolved permissions from the auth token, used by the frontend to show/hide admin navigation.
*ServiceAssignmentApi* | [**createServiceAssignment**](docs/Api/ServiceAssignmentApi.md#createserviceassignment) | **POST** /api/v1/service-assignments | 
*ServiceAssignmentApi* | [**deleteServiceAssignment**](docs/Api/ServiceAssignmentApi.md#deleteserviceassignment) | **DELETE** /api/v1/service-assignments/{id} | 
*ServiceAssignmentApi* | [**getServiceAssignment**](docs/Api/ServiceAssignmentApi.md#getserviceassignment) | **GET** /api/v1/service-assignments/{id} | 
*ServiceAssignmentApi* | [**getServiceAssignments**](docs/Api/ServiceAssignmentApi.md#getserviceassignments) | **GET** /api/v1/service-assignments/ | 
*ServiceAssignmentApi* | [**updateServiceAssignment**](docs/Api/ServiceAssignmentApi.md#updateserviceassignment) | **PUT** /api/v1/service-assignments/{id} | 
*ServiceJobApi* | [**createServiceJob**](docs/Api/ServiceJobApi.md#createservicejob) | **POST** /api/v1/service-jobs | 
*ServiceJobApi* | [**deleteServiceJob**](docs/Api/ServiceJobApi.md#deleteservicejob) | **DELETE** /api/v1/service-jobs/{id} | 
*ServiceJobApi* | [**getServiceJob**](docs/Api/ServiceJobApi.md#getservicejob) | **GET** /api/v1/service-jobs/{id} | 
*ServiceJobApi* | [**getServiceJobs**](docs/Api/ServiceJobApi.md#getservicejobs) | **GET** /api/v1/service-jobs/ | 
*ServiceJobApi* | [**updateServiceJob**](docs/Api/ServiceJobApi.md#updateservicejob) | **PUT** /api/v1/service-jobs/{id} | 
*ShareholderApi* | [**createShareholder**](docs/Api/ShareholderApi.md#createshareholder) | **POST** /api/v1/shareholders | 
*ShareholderApi* | [**deleteShareholder**](docs/Api/ShareholderApi.md#deleteshareholder) | **DELETE** /api/v1/shareholders/{id} | 
*ShareholderApi* | [**getShareholder**](docs/Api/ShareholderApi.md#getshareholder) | **GET** /api/v1/shareholders/{id} | 
*ShareholderApi* | [**getShareholders**](docs/Api/ShareholderApi.md#getshareholders) | **GET** /api/v1/shareholders/ | 
*ShareholderApi* | [**updateShareholder**](docs/Api/ShareholderApi.md#updateshareholder) | **PUT** /api/v1/shareholders/{id} | 
*ShipmentApi* | [**createShipment**](docs/Api/ShipmentApi.md#createshipment) | **POST** /api/v1/shipments | 
*ShipmentApi* | [**createShipmentFromOrder**](docs/Api/ShipmentApi.md#createshipmentfromorder) | **POST** /api/v1/orders/{order_number}/shipments | Create a real shipment for an order: calls the configured carrier&#39;s label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.
*ShipmentApi* | [**deleteShipment**](docs/Api/ShipmentApi.md#deleteshipment) | **DELETE** /api/v1/shipments/{shipment_id} | 
*ShipmentApi* | [**getShipment**](docs/Api/ShipmentApi.md#getshipment) | **GET** /api/v1/shipments/{shipment_id} | 
*ShipmentApi* | [**listShipments**](docs/Api/ShipmentApi.md#listshipments) | **GET** /api/v1/shipments | 
*ShipmentApi* | [**trackOrderPublic**](docs/Api/ShipmentApi.md#trackorderpublic) | **POST** /api/v1/public/track | Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).
*ShipmentApi* | [**trackShipmentApi**](docs/Api/ShipmentApi.md#trackshipmentapi) | **GET** /api/v1/shipments/{shipment_id}/tracking | 
*ShipmentApi* | [**updateShipmentStatus**](docs/Api/ShipmentApi.md#updateshipmentstatus) | **PUT** /api/v1/shipments/{shipment_id}/status | 
*ShippingApi* | [**getCredentialsApi**](docs/Api/ShippingApi.md#getcredentialsapi) | **GET** /api/v1/shipping/credentials | 
*ShippingApi* | [**getRatesApi**](docs/Api/ShippingApi.md#getratesapi) | **POST** /api/v1/shipping/rates | 
*ShippingApi* | [**listProvidersApi**](docs/Api/ShippingApi.md#listprovidersapi) | **GET** /api/v1/shipping/providers | 
*ShippingApi* | [**saveCredentialsApi**](docs/Api/ShippingApi.md#savecredentialsapi) | **PUT** /api/v1/shipping/credentials | 
*ShippingRuleApi* | [**createShippingRule**](docs/Api/ShippingRuleApi.md#createshippingrule) | **POST** /api/v1/shipping-rules | 
*ShippingRuleApi* | [**deleteShippingRule**](docs/Api/ShippingRuleApi.md#deleteshippingrule) | **DELETE** /api/v1/shipping-rules/{rule_id} | 
*ShippingRuleApi* | [**getShippingRule**](docs/Api/ShippingRuleApi.md#getshippingrule) | **GET** /api/v1/shipping-rules/{rule_id} | 
*ShippingRuleApi* | [**listShippingRules**](docs/Api/ShippingRuleApi.md#listshippingrules) | **GET** /api/v1/shipping-rules/ | 
*ShippingRuleApi* | [**updateShippingRule**](docs/Api/ShippingRuleApi.md#updateshippingrule) | **PUT** /api/v1/shipping-rules/{rule_id} | 
*ShippingThresholdApi* | [**createShippingThreshold**](docs/Api/ShippingThresholdApi.md#createshippingthreshold) | **POST** /api/v1/shipping-thresholds | 
*ShippingThresholdApi* | [**deleteShippingThreshold**](docs/Api/ShippingThresholdApi.md#deleteshippingthreshold) | **DELETE** /api/v1/shipping-thresholds/{threshold_id} | 
*ShippingThresholdApi* | [**getDeliverable**](docs/Api/ShippingThresholdApi.md#getdeliverable) | **GET** /api/v1/shipping-thresholds/deliverable | 
*ShippingThresholdApi* | [**getShippingThreshold**](docs/Api/ShippingThresholdApi.md#getshippingthreshold) | **GET** /api/v1/shipping-thresholds/{threshold_id} | 
*ShippingThresholdApi* | [**listShippingThresholds**](docs/Api/ShippingThresholdApi.md#listshippingthresholds) | **GET** /api/v1/shipping-thresholds/ | 
*ShippingThresholdApi* | [**updateShippingThreshold**](docs/Api/ShippingThresholdApi.md#updateshippingthreshold) | **PUT** /api/v1/shipping-thresholds/{threshold_id} | 
*ShopApi* | [**shopEditorSave**](docs/Api/ShopApi.md#shopeditorsave) | **POST** /api/v1/shop/editor | 
*SilentPartnerApi* | [**createSilentPartner**](docs/Api/SilentPartnerApi.md#createsilentpartner) | **POST** /api/v1/silent-partners | 
*SilentPartnerApi* | [**deleteSilentPartner**](docs/Api/SilentPartnerApi.md#deletesilentpartner) | **DELETE** /api/v1/silent-partners/{id} | 
*SilentPartnerApi* | [**getSilentPartner**](docs/Api/SilentPartnerApi.md#getsilentpartner) | **GET** /api/v1/silent-partners/{id} | 
*SilentPartnerApi* | [**getSilentPartners**](docs/Api/SilentPartnerApi.md#getsilentpartners) | **GET** /api/v1/silent-partners/ | 
*SilentPartnerApi* | [**updateSilentPartner**](docs/Api/SilentPartnerApi.md#updatesilentpartner) | **PUT** /api/v1/silent-partners/{id} | 
*StilleApi* | [**stilleExportApi**](docs/Api/StilleApi.md#stilleexportapi) | **GET** /api/v1/bookkeeping/stille/export | 
*StilleApi* | [**stilleReportApi**](docs/Api/StilleApi.md#stillereportapi) | **GET** /api/v1/bookkeeping/stille/report | 
*StockMovementApi* | [**getStockMovement**](docs/Api/StockMovementApi.md#getstockmovement) | **GET** /api/v1/stock-movements/{movement_id} | 
*StockMovementApi* | [**listStockMovements**](docs/Api/StockMovementApi.md#liststockmovements) | **GET** /api/v1/stock-movements/ | 
*StockTransferApi* | [**createStockTransfer**](docs/Api/StockTransferApi.md#createstocktransfer) | **POST** /api/v1/stock-transfers | 
*StockTransferApi* | [**deleteStockTransfer**](docs/Api/StockTransferApi.md#deletestocktransfer) | **DELETE** /api/v1/stock-transfers/{stock_transfer_id} | 
*StockTransferApi* | [**getStockTransfer**](docs/Api/StockTransferApi.md#getstocktransfer) | **GET** /api/v1/stock-transfers/{stock_transfer_id} | 
*StockTransferApi* | [**listStockTransfers**](docs/Api/StockTransferApi.md#liststocktransfers) | **GET** /api/v1/stock-transfers/ | 
*StockTransferApi* | [**updateStockTransferStatus**](docs/Api/StockTransferApi.md#updatestocktransferstatus) | **PUT** /api/v1/stock-transfers/{stock_transfer_id}/status | 
*SuitabilityApi* | [**shippingSuitabilityApi**](docs/Api/SuitabilityApi.md#shippingsuitabilityapi) | **POST** /api/v1/shipping/suitability | 
*SupplierConditionApi* | [**createSupplierCondition**](docs/Api/SupplierConditionApi.md#createsuppliercondition) | **POST** /api/v1/supplier-conditions | 
*SupplierConditionApi* | [**deleteSupplierCondition**](docs/Api/SupplierConditionApi.md#deletesuppliercondition) | **DELETE** /api/v1/supplier-conditions/{supplier_condition_id} | 
*SupplierConditionApi* | [**getSupplierCondition**](docs/Api/SupplierConditionApi.md#getsuppliercondition) | **GET** /api/v1/supplier-conditions/{supplier_condition_id} | 
*SupplierConditionApi* | [**listSupplierConditions**](docs/Api/SupplierConditionApi.md#listsupplierconditions) | **GET** /api/v1/supplier-conditions/ | 
*SupplierConditionApi* | [**updateSupplierCondition**](docs/Api/SupplierConditionApi.md#updatesuppliercondition) | **PUT** /api/v1/supplier-conditions/{supplier_condition_id} | 
*SupplierInvoiceApi* | [**createSupplierInvoice**](docs/Api/SupplierInvoiceApi.md#createsupplierinvoice) | **POST** /api/v1/supplier-invoices | 
*SupplierInvoiceApi* | [**deleteSupplierInvoice**](docs/Api/SupplierInvoiceApi.md#deletesupplierinvoice) | **DELETE** /api/v1/supplier-invoices/{supplier_invoice_id} | 
*SupplierInvoiceApi* | [**getSupplierInvoice**](docs/Api/SupplierInvoiceApi.md#getsupplierinvoice) | **GET** /api/v1/supplier-invoices/{supplier_invoice_id} | 
*SupplierInvoiceApi* | [**listSupplierInvoices**](docs/Api/SupplierInvoiceApi.md#listsupplierinvoices) | **GET** /api/v1/supplier-invoices/ | 
*SupplierInvoiceApi* | [**updateSupplierInvoice**](docs/Api/SupplierInvoiceApi.md#updatesupplierinvoice) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id} | 
*SupplierInvoiceApi* | [**updateSupplierInvoiceStatus**](docs/Api/SupplierInvoiceApi.md#updatesupplierinvoicestatus) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id}/status | 
*SupportChannelApi* | [**createChannelApi**](docs/Api/SupportChannelApi.md#createchannelapi) | **POST** /api/v1/support/channels | 
*SupportChannelApi* | [**deleteChannelApi**](docs/Api/SupportChannelApi.md#deletechannelapi) | **DELETE** /api/v1/support/channels/{channel_id} | 
*SupportChannelApi* | [**listChannelsApi**](docs/Api/SupportChannelApi.md#listchannelsapi) | **GET** /api/v1/support/channels | 
*SupportChannelApi* | [**updateChannelApi**](docs/Api/SupportChannelApi.md#updatechannelapi) | **PUT** /api/v1/support/channels/{channel_id} | 
*SupportTicketApi* | [**createTicketApi**](docs/Api/SupportTicketApi.md#createticketapi) | **POST** /api/v1/support/tickets | 
*SupportTicketApi* | [**deleteTicketApi**](docs/Api/SupportTicketApi.md#deleteticketapi) | **DELETE** /api/v1/support/tickets/{ticket_id} | 
*SupportTicketApi* | [**getTicketApi**](docs/Api/SupportTicketApi.md#getticketapi) | **GET** /api/v1/support/tickets/{ticket_id} | 
*SupportTicketApi* | [**listTicketsApi**](docs/Api/SupportTicketApi.md#listticketsapi) | **GET** /api/v1/support/tickets | 
*SupportTicketApi* | [**updateTicketApi**](docs/Api/SupportTicketApi.md#updateticketapi) | **PUT** /api/v1/support/tickets/{ticket_id} | 
*TaxApi* | [**createTaxRate**](docs/Api/TaxApi.md#createtaxrate) | **POST** /api/v1/tax-rates | Create a tax rate (&#x60;admin:settings&#x60;).
*TaxApi* | [**deleteTaxRate**](docs/Api/TaxApi.md#deletetaxrate) | **DELETE** /api/v1/tax-rates/{id} | Delete a tax rate by id (&#x60;admin:settings&#x60;).
*TaxApi* | [**listTaxRates**](docs/Api/TaxApi.md#listtaxrates) | **GET** /api/v1/tax-rates | List the calling tenant&#39;s tax rates.
*TaxApi* | [**updateTaxRate**](docs/Api/TaxApi.md#updatetaxrate) | **PUT** /api/v1/tax-rates/{id} | Update a tax rate by id (&#x60;admin:settings&#x60;). Replaces all body fields.
*TenantSettingsApi* | [**getTenantSettings**](docs/Api/TenantSettingsApi.md#gettenantsettings) | **GET** /api/v1/settings/tenant | 
*TenantSettingsApi* | [**updateTenantSettings**](docs/Api/TenantSettingsApi.md#updatetenantsettings) | **PUT** /api/v1/settings/tenant | 
*TicketMessageApi* | [**listMessagesApi**](docs/Api/TicketMessageApi.md#listmessagesapi) | **GET** /api/v1/support/tickets/{ticket_id}/messages | 
*TicketMessageApi* | [**sendMessageApi**](docs/Api/TicketMessageApi.md#sendmessageapi) | **POST** /api/v1/support/tickets/{ticket_id}/messages | 
*TimeEntriesApi* | [**clockInTimeEntry**](docs/Api/TimeEntriesApi.md#clockintimeentry) | **POST** /api/v1/time-entries | Clock in for the authenticated user (resolved via their employee profile).
*TimeEntriesApi* | [**clockOutTimeEntry**](docs/Api/TimeEntriesApi.md#clockouttimeentry) | **PATCH** /api/v1/time-entries/{id} | Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;.
*TimeEntriesApi* | [**getLaborCosts**](docs/Api/TimeEntriesApi.md#getlaborcosts) | **GET** /api/v1/labor-costs | Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate.
*TimeEntriesApi* | [**listTimeEntries**](docs/Api/TimeEntriesApi.md#listtimeentries) | **GET** /api/v1/time-entries | List time entries with optional date-range / active / employee filters.
*TrainingAssignmentApi* | [**createTrainingAssignment**](docs/Api/TrainingAssignmentApi.md#createtrainingassignment) | **POST** /api/v1/training-assignments | 
*TrainingAssignmentApi* | [**deleteTrainingAssignment**](docs/Api/TrainingAssignmentApi.md#deletetrainingassignment) | **DELETE** /api/v1/training-assignments/{id} | 
*TrainingAssignmentApi* | [**getTrainingAssignment**](docs/Api/TrainingAssignmentApi.md#gettrainingassignment) | **GET** /api/v1/training-assignments/{id} | 
*TrainingAssignmentApi* | [**getTrainingAssignments**](docs/Api/TrainingAssignmentApi.md#gettrainingassignments) | **GET** /api/v1/training-assignments/ | 
*TrainingAssignmentApi* | [**updateTrainingAssignment**](docs/Api/TrainingAssignmentApi.md#updatetrainingassignment) | **PUT** /api/v1/training-assignments/{id} | 
*TrainingsApi* | [**getMyTrainings**](docs/Api/TrainingsApi.md#getmytrainings) | **GET** /api/v1/trainings/me | 
*TrainingsApi* | [**getTrainingContent**](docs/Api/TrainingsApi.md#gettrainingcontent) | **GET** /api/v1/trainings/content/{code} | 
*TrainingsApi* | [**getTrainingOverview**](docs/Api/TrainingsApi.md#gettrainingoverview) | **GET** /api/v1/trainings/overview | 
*TrainingsApi* | [**submitTrainingResult**](docs/Api/TrainingsApi.md#submittrainingresult) | **POST** /api/v1/trainings/submit-result | 
*UserApi* | [**changePassword**](docs/Api/UserApi.md#changepassword) | **POST** /user/change-password | Change the current user&#39;s password (requires the current password).
*UserApi* | [**createTeam**](docs/Api/UserApi.md#createteam) | **POST** /user/teams | Create a new team within the current tenant
*UserApi* | [**generateApiKey**](docs/Api/UserApi.md#generateapikey) | **POST** /user/api-key | Generate a new API key for the current user
*UserApi* | [**inviteUser**](docs/Api/UserApi.md#inviteuser) | **POST** /user/invite | Invite a user to the current tenant/organization
*UserApi* | [**listTeams**](docs/Api/UserApi.md#listteams) | **GET** /user/teams | List all teams in the current tenant
*UserApi* | [**removeUserFromOrg**](docs/Api/UserApi.md#removeuserfromorg) | **DELETE** /user/remove | Remove a user from the current organization
*UserApi* | [**updateProfile**](docs/Api/UserApi.md#updateprofile) | **PUT** /user/profile | Update the current user&#39;s profile
*UserApi* | [**userProfile**](docs/Api/UserApi.md#userprofile) | **GET** /user/profile | Get the current user&#39;s profile
*UserApi* | [**userTenants**](docs/Api/UserApi.md#usertenants) | **GET** /user/tenants | List all tenants (organizations) the current user belongs to
*UserManagementApi* | [**getUser**](docs/Api/UserManagementApi.md#getuser) | **GET** /api/v1/users/{user_id} | 
*UserManagementApi* | [**listUsers**](docs/Api/UserManagementApi.md#listusers) | **GET** /api/v1/users | 
*UserManagementApi* | [**removeUser**](docs/Api/UserManagementApi.md#removeuser) | **DELETE** /api/v1/users/{user_id} | 
*UserManagementApi* | [**updateUserPermissions**](docs/Api/UserManagementApi.md#updateuserpermissions) | **PUT** /api/v1/users/{user_id}/permissions | 
*UserManagementApi* | [**updateUserRole**](docs/Api/UserManagementApi.md#updateuserrole) | **PUT** /api/v1/users/{user_id}/role | 
*UstvaApi* | [**jahresustApi**](docs/Api/UstvaApi.md#jahresustapi) | **GET** /api/v1/bookkeeping/jahresust | 
*UstvaApi* | [**ustvaApi**](docs/Api/UstvaApi.md#ustvaapi) | **GET** /api/v1/bookkeeping/ustva | 
*VoucherApi* | [**createVoucher**](docs/Api/VoucherApi.md#createvoucher) | **POST** /api/v1/vouchers | 
*VoucherApi* | [**deleteVoucher**](docs/Api/VoucherApi.md#deletevoucher) | **DELETE** /api/v1/vouchers/{voucher_id} | 
*VoucherApi* | [**getVoucher**](docs/Api/VoucherApi.md#getvoucher) | **GET** /api/v1/vouchers/{voucher_id} | 
*VoucherApi* | [**listVouchers**](docs/Api/VoucherApi.md#listvouchers) | **GET** /api/v1/vouchers/ | 
*VoucherApi* | [**updateVoucher**](docs/Api/VoucherApi.md#updatevoucher) | **PUT** /api/v1/vouchers/{voucher_id} | 
*VoucherApi* | [**voucherRestore**](docs/Api/VoucherApi.md#voucherrestore) | **POST** /api/v1/vouchers/{voucher_id}/restore | 
*WarehouseApi* | [**createWarehouse**](docs/Api/WarehouseApi.md#createwarehouse) | **POST** /api/v1/warehouses | 
*WarehouseApi* | [**deleteWarehouse**](docs/Api/WarehouseApi.md#deletewarehouse) | **DELETE** /api/v1/warehouses/{warehouse_id} | 
*WarehouseApi* | [**getWarehouse**](docs/Api/WarehouseApi.md#getwarehouse) | **GET** /api/v1/warehouses/{warehouse_id} | 
*WarehouseApi* | [**listWarehouses**](docs/Api/WarehouseApi.md#listwarehouses) | **GET** /api/v1/warehouses/ | 
*WarehouseApi* | [**updateWarehouse**](docs/Api/WarehouseApi.md#updatewarehouse) | **PUT** /api/v1/warehouses/{warehouse_id} | 
*WarehouseStockApi* | [**createWarehouseStock**](docs/Api/WarehouseStockApi.md#createwarehousestock) | **POST** /api/v1/warehouses/{warehouse_id}/stock | 
*WarehouseStockApi* | [**deleteWarehouseStock**](docs/Api/WarehouseStockApi.md#deletewarehousestock) | **DELETE** /api/v1/warehouses/{warehouse_id}/stock/{product_id} | 
*WarehouseStockApi* | [**listWarehouseStock**](docs/Api/WarehouseStockApi.md#listwarehousestock) | **GET** /api/v1/warehouses/{warehouse_id}/stock | 
*WarehouseStockApi* | [**updateWarehouseStock**](docs/Api/WarehouseStockApi.md#updatewarehousestock) | **PUT** /api/v1/warehouses/{warehouse_id}/stock/{product_id} | 
*WebhooksApi* | [**createSubscription**](docs/Api/WebhooksApi.md#createsubscription) | **POST** /api/v1/webhook-subscriptions | Create a webhook subscription (outbound hook).
*WebhooksApi* | [**deleteSubscription**](docs/Api/WebhooksApi.md#deletesubscription) | **DELETE** /api/v1/webhook-subscriptions/{subscription_id} | Delete a webhook subscription.
*WebhooksApi* | [**emitApi**](docs/Api/WebhooksApi.md#emitapi) | **POST** /api/v1/webhooks/emit | Manually fire an event against matching hooks (for testing/flows).
*WebhooksApi* | [**listEvent**](docs/Api/WebhooksApi.md#listevent) | **GET** /api/v1/webhook-events | List webhook events (inbound + outbound log).
*WebhooksApi* | [**listSubscriptions**](docs/Api/WebhooksApi.md#listsubscriptions) | **GET** /api/v1/webhook-subscriptions | List webhook subscriptions for the tenant.
*WebhooksApi* | [**updateSubscription**](docs/Api/WebhooksApi.md#updatesubscription) | **PUT** /api/v1/webhook-subscriptions/{subscription_id} | Update a webhook subscription.
*WorkflowsApi* | [**listWorkflowsApi**](docs/Api/WorkflowsApi.md#listworkflowsapi) | **GET** /api/v1/workflows | 
*WorkflowsApi* | [**setWorkflowEnabledApi**](docs/Api/WorkflowsApi.md#setworkflowenabledapi) | **PUT** /api/v1/workflows/{workflow_id}/enabled | 
*ZugferdApi* | [**generateZugferdApi**](docs/Api/ZugferdApi.md#generatezugferdapi) | **GET** /api/v1/invoices/{id}/zugferd | 

## Models

- [Absence](docs/Model/Absence.md)
- [AbsenceCreate](docs/Model/AbsenceCreate.md)
- [AbsenceStatus](docs/Model/AbsenceStatus.md)
- [AbsenceType](docs/Model/AbsenceType.md)
- [AbsenceUpdate](docs/Model/AbsenceUpdate.md)
- [AcceptInviteRequest](docs/Model/AcceptInviteRequest.md)
- [AccountOverview](docs/Model/AccountOverview.md)
- [Activity](docs/Model/Activity.md)
- [ActivityCreate](docs/Model/ActivityCreate.md)
- [ActivityStatus](docs/Model/ActivityStatus.md)
- [ActivityStatusUpdate](docs/Model/ActivityStatusUpdate.md)
- [ActivityType](docs/Model/ActivityType.md)
- [ActivityUpdate](docs/Model/ActivityUpdate.md)
- [Address](docs/Model/Address.md)
- [AiConfigDto](docs/Model/AiConfigDto.md)
- [AiSuggestion](docs/Model/AiSuggestion.md)
- [AiSuggestionRequest](docs/Model/AiSuggestionRequest.md)
- [AiWorkerConfig](docs/Model/AiWorkerConfig.md)
- [AllocatePaymentRequest](docs/Model/AllocatePaymentRequest.md)
- [AnlageGErgebnis](docs/Model/AnlageGErgebnis.md)
- [AnlageGKfzHinweis](docs/Model/AnlageGKfzHinweis.md)
- [AnlageSErgebnis](docs/Model/AnlageSErgebnis.md)
- [AnlageSKfzHinweis](docs/Model/AnlageSKfzHinweis.md)
- [ApiResponseGdprExport](docs/Model/ApiResponseGdprExport.md)
- [ApiResponseGdprExportData](docs/Model/ApiResponseGdprExportData.md)
- [ApiResponseString](docs/Model/ApiResponseString.md)
- [ApiResponseSubscriptionOverview](docs/Model/ApiResponseSubscriptionOverview.md)
- [ApiResponseSubscriptionOverviewData](docs/Model/ApiResponseSubscriptionOverviewData.md)
- [ApiResponseTeam](docs/Model/ApiResponseTeam.md)
- [ApiResponseTeamData](docs/Model/ApiResponseTeamData.md)
- [ApiResponseUserProfile](docs/Model/ApiResponseUserProfile.md)
- [ApiResponseUserProfileData](docs/Model/ApiResponseUserProfileData.md)
- [ApiResponseVecPlan](docs/Model/ApiResponseVecPlan.md)
- [ApiResponseVecPlanDataInner](docs/Model/ApiResponseVecPlanDataInner.md)
- [ApiResponseVecTeam](docs/Model/ApiResponseVecTeam.md)
- [ApiResponseVecUserTenantInfo](docs/Model/ApiResponseVecUserTenantInfo.md)
- [ApiResponseVecUserTenantInfoDataInner](docs/Model/ApiResponseVecUserTenantInfoDataInner.md)
- [ApplicationFilter](docs/Model/ApplicationFilter.md)
- [ApplicationStatus](docs/Model/ApplicationStatus.md)
- [ApplicationStatusDto](docs/Model/ApplicationStatusDto.md)
- [AppointmentStatusUpdate](docs/Model/AppointmentStatusUpdate.md)
- [AssignmentStatus](docs/Model/AssignmentStatus.md)
- [Attachment](docs/Model/Attachment.md)
- [AttachmentCreate](docs/Model/AttachmentCreate.md)
- [AttachmentVersion](docs/Model/AttachmentVersion.md)
- [AuthResponse](docs/Model/AuthResponse.md)
- [Automation](docs/Model/Automation.md)
- [AutomationDto](docs/Model/AutomationDto.md)
- [BWAExpenses](docs/Model/BWAExpenses.md)
- [BWAReport](docs/Model/BWAReport.md)
- [BWARevenue](docs/Model/BWARevenue.md)
- [BWASummary](docs/Model/BWASummary.md)
- [BalanceItem](docs/Model/BalanceItem.md)
- [BalanceSheet](docs/Model/BalanceSheet.md)
- [BankLookup](docs/Model/BankLookup.md)
- [Betriebsstaette](docs/Model/Betriebsstaette.md)
- [BetriebsstaettenDetail](docs/Model/BetriebsstaettenDetail.md)
- [BilanzItem](docs/Model/BilanzItem.md)
- [BilanzReport](docs/Model/BilanzReport.md)
- [Bom](docs/Model/Bom.md)
- [BomCreate](docs/Model/BomCreate.md)
- [BomStatus](docs/Model/BomStatus.md)
- [BomUpdate](docs/Model/BomUpdate.md)
- [BoxFit](docs/Model/BoxFit.md)
- [Budget](docs/Model/Budget.md)
- [BudgetErgebnis](docs/Model/BudgetErgebnis.md)
- [BudgetGoalRequest](docs/Model/BudgetGoalRequest.md)
- [BudgetKategorie](docs/Model/BudgetKategorie.md)
- [CartItemInput](docs/Model/CartItemInput.md)
- [CashflowReport](docs/Model/CashflowReport.md)
- [CategoryTotal](docs/Model/CategoryTotal.md)
- [ChangePasswordRequest](docs/Model/ChangePasswordRequest.md)
- [ChangelogEntry](docs/Model/ChangelogEntry.md)
- [CheckStatus](docs/Model/CheckStatus.md)
- [CommunicationChannel](docs/Model/CommunicationChannel.md)
- [CommunicationDirection](docs/Model/CommunicationDirection.md)
- [CompanyType](docs/Model/CompanyType.md)
- [ComplianceEntry](docs/Model/ComplianceEntry.md)
- [ComplianceTraining](docs/Model/ComplianceTraining.md)
- [ComplianceTrainingCreate](docs/Model/ComplianceTrainingCreate.md)
- [ComplianceTrainingUpdate](docs/Model/ComplianceTrainingUpdate.md)
- [ConfigFieldInfo](docs/Model/ConfigFieldInfo.md)
- [ConfigFieldKind](docs/Model/ConfigFieldKind.md)
- [ConfigFieldKindOneOf](docs/Model/ConfigFieldKindOneOf.md)
- [ConfigFieldKindOneOf1](docs/Model/ConfigFieldKindOneOf1.md)
- [ConfigFieldKindOneOf2](docs/Model/ConfigFieldKindOneOf2.md)
- [ConfigFieldKindOneOf3](docs/Model/ConfigFieldKindOneOf3.md)
- [ConfigFieldKindOneOf4](docs/Model/ConfigFieldKindOneOf4.md)
- [ConnectorType](docs/Model/ConnectorType.md)
- [Contact](docs/Model/Contact.md)
- [ContactCreate](docs/Model/ContactCreate.md)
- [ContactHistoryResponse](docs/Model/ContactHistoryResponse.md)
- [ContactInfo](docs/Model/ContactInfo.md)
- [ContactTimelineResponse](docs/Model/ContactTimelineResponse.md)
- [ContactType](docs/Model/ContactType.md)
- [ContactUpdate](docs/Model/ContactUpdate.md)
- [ConvertResponse](docs/Model/ConvertResponse.md)
- [CostingLine](docs/Model/CostingLine.md)
- [CountryCode](docs/Model/CountryCode.md)
- [Coupon](docs/Model/Coupon.md)
- [CouponCreate](docs/Model/CouponCreate.md)
- [CouponUpdate](docs/Model/CouponUpdate.md)
- [CouponValidation](docs/Model/CouponValidation.md)
- [CreateChannelDto](docs/Model/CreateChannelDto.md)
- [CreateConnectionRequest](docs/Model/CreateConnectionRequest.md)
- [CreateEmissionEntry](docs/Model/CreateEmissionEntry.md)
- [CreateEmissionTarget](docs/Model/CreateEmissionTarget.md)
- [CreateShipmentRequest](docs/Model/CreateShipmentRequest.md)
- [CreateSubscriptionRequest](docs/Model/CreateSubscriptionRequest.md)
- [CreateTicketRequest](docs/Model/CreateTicketRequest.md)
- [CurrencyCode](docs/Model/CurrencyCode.md)
- [CurrentInventoryValue](docs/Model/CurrentInventoryValue.md)
- [Customer](docs/Model/Customer.md)
- [CustomerCommunication](docs/Model/CustomerCommunication.md)
- [CustomerCommunicationCreate](docs/Model/CustomerCommunicationCreate.md)
- [CustomerCommunicationUpdate](docs/Model/CustomerCommunicationUpdate.md)
- [CustomerCreate](docs/Model/CustomerCreate.md)
- [CustomerGroup](docs/Model/CustomerGroup.md)
- [CustomerGroupCreate](docs/Model/CustomerGroupCreate.md)
- [CustomerGroupUpdate](docs/Model/CustomerGroupUpdate.md)
- [CustomerInfo](docs/Model/CustomerInfo.md)
- [CustomerUpdate](docs/Model/CustomerUpdate.md)
- [DataQuality](docs/Model/DataQuality.md)
- [DatevBookingPreview](docs/Model/DatevBookingPreview.md)
- [DatevExportResponse](docs/Model/DatevExportResponse.md)
- [DatevImportResponse](docs/Model/DatevImportResponse.md)
- [DatevImportRow](docs/Model/DatevImportRow.md)
- [Declaration](docs/Model/Declaration.md)
- [DeclarationCreate](docs/Model/DeclarationCreate.md)
- [DeclarationType](docs/Model/DeclarationType.md)
- [DeclarationUpdate](docs/Model/DeclarationUpdate.md)
- [DeliverableResponse](docs/Model/DeliverableResponse.md)
- [DeliveryAppointment](docs/Model/DeliveryAppointment.md)
- [DeliveryAppointmentCreate](docs/Model/DeliveryAppointmentCreate.md)
- [DeliveryAppointmentStatus](docs/Model/DeliveryAppointmentStatus.md)
- [DeliveryDate](docs/Model/DeliveryDate.md)
- [DeliveryDateCreate](docs/Model/DeliveryDateCreate.md)
- [DeliveryDateStatus](docs/Model/DeliveryDateStatus.md)
- [DeliveryDateStatusUpdate](docs/Model/DeliveryDateStatusUpdate.md)
- [DeliveryDateUpdate](docs/Model/DeliveryDateUpdate.md)
- [DeliveryNote](docs/Model/DeliveryNote.md)
- [DeliveryNoteCreate](docs/Model/DeliveryNoteCreate.md)
- [DhlCredentials](docs/Model/DhlCredentials.md)
- [DiscountType](docs/Model/DiscountType.md)
- [DocumentType](docs/Model/DocumentType.md)
- [DownPaymentInvoice](docs/Model/DownPaymentInvoice.md)
- [DpaAcceptRequest](docs/Model/DpaAcceptRequest.md)
- [DpaStatus](docs/Model/DpaStatus.md)
- [DunningResult](docs/Model/DunningResult.md)
- [EBilanzReport](docs/Model/EBilanzReport.md)
- [EksErgebnis](docs/Model/EksErgebnis.md)
- [EksMonatsWert](docs/Model/EksMonatsWert.md)
- [ElsterStatus](docs/Model/ElsterStatus.md)
- [EmailTemplate](docs/Model/EmailTemplate.md)
- [EmailTemplateCreate](docs/Model/EmailTemplateCreate.md)
- [EmailTemplateStatus](docs/Model/EmailTemplateStatus.md)
- [EmailTemplateUpdate](docs/Model/EmailTemplateUpdate.md)
- [EmissionEntry](docs/Model/EmissionEntry.md)
- [EmissionFactorResponse](docs/Model/EmissionFactorResponse.md)
- [EmissionMethod](docs/Model/EmissionMethod.md)
- [EmissionTarget](docs/Model/EmissionTarget.md)
- [EmissionTargetScope](docs/Model/EmissionTargetScope.md)
- [EmissionsExportResponse](docs/Model/EmissionsExportResponse.md)
- [EmissionsReport](docs/Model/EmissionsReport.md)
- [EmitEventRequest](docs/Model/EmitEventRequest.md)
- [Employee](docs/Model/Employee.md)
- [EmployeeCreate](docs/Model/EmployeeCreate.md)
- [EmployeeStatus](docs/Model/EmployeeStatus.md)
- [EmployeeUpdate](docs/Model/EmployeeUpdate.md)
- [EmploymentType](docs/Model/EmploymentType.md)
- [EuerDetailErgebnis](docs/Model/EuerDetailErgebnis.md)
- [EuerErgebnis](docs/Model/EuerErgebnis.md)
- [EuerKatSumme](docs/Model/EuerKatSumme.md)
- [EuerZeile](docs/Model/EuerZeile.md)
- [EuerZeileDetail](docs/Model/EuerZeileDetail.md)
- [EventSubscription](docs/Model/EventSubscription.md)
- [ExecutionStatus](docs/Model/ExecutionStatus.md)
- [ExpenseItem](docs/Model/ExpenseItem.md)
- [ExtraPayment](docs/Model/ExtraPayment.md)
- [FeatureSettings](docs/Model/FeatureSettings.md)
- [ForgotPasswordRequest](docs/Model/ForgotPasswordRequest.md)
- [FristEintrag](docs/Model/FristEintrag.md)
- [FristenErgebnis](docs/Model/FristenErgebnis.md)
- [GatewayOAuthAuthorizeRequest](docs/Model/GatewayOAuthAuthorizeRequest.md)
- [GatewayOAuthAuthorizeResponse](docs/Model/GatewayOAuthAuthorizeResponse.md)
- [GatewayOAuthCallbackRequest](docs/Model/GatewayOAuthCallbackRequest.md)
- [GatewayType](docs/Model/GatewayType.md)
- [GdprActivity](docs/Model/GdprActivity.md)
- [GdprApiKey](docs/Model/GdprApiKey.md)
- [GdprBillingInfo](docs/Model/GdprBillingInfo.md)
- [GdprExport](docs/Model/GdprExport.md)
- [GdprNotification](docs/Model/GdprNotification.md)
- [GdprRefreshToken](docs/Model/GdprRefreshToken.md)
- [GdprTenant](docs/Model/GdprTenant.md)
- [GdprUsageEvent](docs/Model/GdprUsageEvent.md)
- [GdprUser](docs/Model/GdprUser.md)
- [Gender](docs/Model/Gender.md)
- [GenerateCountRequest](docs/Model/GenerateCountRequest.md)
- [GenerateVariantsRequest](docs/Model/GenerateVariantsRequest.md)
- [GewerbesteuerErgebnis](docs/Model/GewerbesteuerErgebnis.md)
- [GewinnverwendungsExportResponse](docs/Model/GewinnverwendungsExportResponse.md)
- [GewinnverwendungsReport](docs/Model/GewinnverwendungsReport.md)
- [GewinnverwendungsZeile](docs/Model/GewinnverwendungsZeile.md)
- [GezReport](docs/Model/GezReport.md)
- [GhgScope](docs/Model/GhgScope.md)
- [GoBDExportResponse](docs/Model/GoBDExportResponse.md)
- [GoodsReceipt](docs/Model/GoodsReceipt.md)
- [GroupFigure](docs/Model/GroupFigure.md)
- [GroupFigureCreate](docs/Model/GroupFigureCreate.md)
- [GroupFigureUpdate](docs/Model/GroupFigureUpdate.md)
- [GuVItem](docs/Model/GuVItem.md)
- [GuVReport](docs/Model/GuVReport.md)
- [HebesatzLookup](docs/Model/HebesatzLookup.md)
- [HrTrainingOverview](docs/Model/HrTrainingOverview.md)
- [ImportJobStatus](docs/Model/ImportJobStatus.md)
- [ImportStartRequest](docs/Model/ImportStartRequest.md)
- [ImportStartResponse](docs/Model/ImportStartResponse.md)
- [ImportTestRequest](docs/Model/ImportTestRequest.md)
- [ImportTestResponse](docs/Model/ImportTestResponse.md)
- [IncomeStatement](docs/Model/IncomeStatement.md)
- [InstituteCheckItem](docs/Model/InstituteCheckItem.md)
- [InstituteDeadlines](docs/Model/InstituteDeadlines.md)
- [InstituteProfile](docs/Model/InstituteProfile.md)
- [InstituteProfileUpdate](docs/Model/InstituteProfileUpdate.md)
- [InstituteStatus](docs/Model/InstituteStatus.md)
- [InstituteType](docs/Model/InstituteType.md)
- [InstrumentType](docs/Model/InstrumentType.md)
- [InventoryCount](docs/Model/InventoryCount.md)
- [InventoryCountCreate](docs/Model/InventoryCountCreate.md)
- [InventoryCountStatus](docs/Model/InventoryCountStatus.md)
- [InventoryCountStatusUpdate](docs/Model/InventoryCountStatusUpdate.md)
- [InventoryCountUpdate](docs/Model/InventoryCountUpdate.md)
- [InventoryValuePoint](docs/Model/InventoryValuePoint.md)
- [InviteRequest](docs/Model/InviteRequest.md)
- [Invoice](docs/Model/Invoice.md)
- [InvoiceCreate](docs/Model/InvoiceCreate.md)
- [InvoiceLineItem](docs/Model/InvoiceLineItem.md)
- [InvoiceMatchRequest](docs/Model/InvoiceMatchRequest.md)
- [InvoicePdfUrlResponse](docs/Model/InvoicePdfUrlResponse.md)
- [InvoiceStatus](docs/Model/InvoiceStatus.md)
- [InvoiceType](docs/Model/InvoiceType.md)
- [JahresUstErgebnis](docs/Model/JahresUstErgebnis.md)
- [Job](docs/Model/Job.md)
- [JobApplication](docs/Model/JobApplication.md)
- [JobPosting](docs/Model/JobPosting.md)
- [JobPostingCreate](docs/Model/JobPostingCreate.md)
- [JobPostingFilter](docs/Model/JobPostingFilter.md)
- [JobPostingStatus](docs/Model/JobPostingStatus.md)
- [JobPostingUpdate](docs/Model/JobPostingUpdate.md)
- [JobStatus](docs/Model/JobStatus.md)
- [JobTitleGap](docs/Model/JobTitleGap.md)
- [KontoItem](docs/Model/KontoItem.md)
- [KontoReport](docs/Model/KontoReport.md)
- [KonzernBeteiligung](docs/Model/KonzernBeteiligung.md)
- [KonzernExportResponse](docs/Model/KonzernExportResponse.md)
- [KonzernStatus](docs/Model/KonzernStatus.md)
- [KonzernThresholds](docs/Model/KonzernThresholds.md)
- [KostenEintrag](docs/Model/KostenEintrag.md)
- [KostenVorschau](docs/Model/KostenVorschau.md)
- [KstErgebnis](docs/Model/KstErgebnis.md)
- [KycRecord](docs/Model/KycRecord.md)
- [KycRecordCreate](docs/Model/KycRecordCreate.md)
- [KycRecordUpdate](docs/Model/KycRecordUpdate.md)
- [LaborCostRow](docs/Model/LaborCostRow.md)
- [LanguageCode](docs/Model/LanguageCode.md)
- [Lead](docs/Model/Lead.md)
- [LeadStatus](docs/Model/LeadStatus.md)
- [LeadUpdate](docs/Model/LeadUpdate.md)
- [LegalDocType](docs/Model/LegalDocType.md)
- [LegalDocument](docs/Model/LegalDocument.md)
- [LegalDocumentReset](docs/Model/LegalDocumentReset.md)
- [LegalDocumentUpsert](docs/Model/LegalDocumentUpsert.md)
- [LiquidityPosition](docs/Model/LiquidityPosition.md)
- [LoginRequest](docs/Model/LoginRequest.md)
- [MagicLinkRequest](docs/Model/MagicLinkRequest.md)
- [MagicLinkVerifyRequest](docs/Model/MagicLinkVerifyRequest.md)
- [MarketplaceConnection](docs/Model/MarketplaceConnection.md)
- [MarketplaceSyncLog](docs/Model/MarketplaceSyncLog.md)
- [MarketplaceWebhookEvent](docs/Model/MarketplaceWebhookEvent.md)
- [MessageDirection](docs/Model/MessageDirection.md)
- [MessageType](docs/Model/MessageType.md)
- [MeteredUsage](docs/Model/MeteredUsage.md)
- [MethodSuitability](docs/Model/MethodSuitability.md)
- [MirrorTriggerResponse](docs/Model/MirrorTriggerResponse.md)
- [Model](docs/Model/Model.md)
- [MovementType](docs/Model/MovementType.md)
- [MyTrainingItem](docs/Model/MyTrainingItem.md)
- [NewVersionRequest](docs/Model/NewVersionRequest.md)
- [NotificationDto](docs/Model/NotificationDto.md)
- [OAuthAuthorizeRequest](docs/Model/OAuthAuthorizeRequest.md)
- [OAuthAuthorizeResponse](docs/Model/OAuthAuthorizeResponse.md)
- [OAuthCallbackRequest](docs/Model/OAuthCallbackRequest.md)
- [OcrTextRequest](docs/Model/OcrTextRequest.md)
- [OffenlegungItem](docs/Model/OffenlegungItem.md)
- [OffenlegungReport](docs/Model/OffenlegungReport.md)
- [OpenItem](docs/Model/OpenItem.md)
- [Order](docs/Model/Order.md)
- [OrderConfirmation](docs/Model/OrderConfirmation.md)
- [OrderConfirmationCreate](docs/Model/OrderConfirmationCreate.md)
- [OrderCreate](docs/Model/OrderCreate.md)
- [OrderStateUpdate](docs/Model/OrderStateUpdate.md)
- [OrderStatus](docs/Model/OrderStatus.md)
- [OrderTagsRequest](docs/Model/OrderTagsRequest.md)
- [OrderUpdate](docs/Model/OrderUpdate.md)
- [OssDependency](docs/Model/OssDependency.md)
- [OssReport](docs/Model/OssReport.md)
- [Package](docs/Model/Package.md)
- [PackingCompleteRequest](docs/Model/PackingCompleteRequest.md)
- [PackingCompleteResponse](docs/Model/PackingCompleteResponse.md)
- [PackingQueue](docs/Model/PackingQueue.md)
- [PackingQueueItem](docs/Model/PackingQueueItem.md)
- [PackingVideoResponse](docs/Model/PackingVideoResponse.md)
- [PartialFeatureSettings](docs/Model/PartialFeatureSettings.md)
- [Participation](docs/Model/Participation.md)
- [ParticipationCreate](docs/Model/ParticipationCreate.md)
- [ParticipationUpdate](docs/Model/ParticipationUpdate.md)
- [PayGapExportResponse](docs/Model/PayGapExportResponse.md)
- [PayGapInfoResponse](docs/Model/PayGapInfoResponse.md)
- [PayGapReport](docs/Model/PayGapReport.md)
- [Payment](docs/Model/Payment.md)
- [PaymentCondition](docs/Model/PaymentCondition.md)
- [PaymentCreate](docs/Model/PaymentCreate.md)
- [PaymentGateway](docs/Model/PaymentGateway.md)
- [PaymentGatewayCreate](docs/Model/PaymentGatewayCreate.md)
- [PaymentGatewayUpdate](docs/Model/PaymentGatewayUpdate.md)
- [PaymentMethod](docs/Model/PaymentMethod.md)
- [PaymentStatus](docs/Model/PaymentStatus.md)
- [PayrollAutopayPayload](docs/Model/PayrollAutopayPayload.md)
- [PayrollCreatePayload](docs/Model/PayrollCreatePayload.md)
- [PayrollEntryApi](docs/Model/PayrollEntryApi.md)
- [PayrollMonth](docs/Model/PayrollMonth.md)
- [PayrollPayPayload](docs/Model/PayrollPayPayload.md)
- [PayrollRunApi](docs/Model/PayrollRunApi.md)
- [PayrollRunStatus](docs/Model/PayrollRunStatus.md)
- [PayrollSummary](docs/Model/PayrollSummary.md)
- [PayrollSummaryItem](docs/Model/PayrollSummaryItem.md)
- [PeppolResponse](docs/Model/PeppolResponse.md)
- [Plan](docs/Model/Plan.md)
- [PlanFeatures](docs/Model/PlanFeatures.md)
- [PlanLimits](docs/Model/PlanLimits.md)
- [PlatformInfo](docs/Model/PlatformInfo.md)
- [PlausibilityCheck](docs/Model/PlausibilityCheck.md)
- [PlausibilityReport](docs/Model/PlausibilityReport.md)
- [PlausibilitySummary](docs/Model/PlausibilitySummary.md)
- [PluginError](docs/Model/PluginError.md)
- [PluginErrorOneOf](docs/Model/PluginErrorOneOf.md)
- [PluginErrorOneOf1](docs/Model/PluginErrorOneOf1.md)
- [PluginErrorOneOf2](docs/Model/PluginErrorOneOf2.md)
- [PluginErrorOneOf3](docs/Model/PluginErrorOneOf3.md)
- [PluginErrorOneOf4](docs/Model/PluginErrorOneOf4.md)
- [PluginErrorOneOf5](docs/Model/PluginErrorOneOf5.md)
- [PluginErrorOneOf6](docs/Model/PluginErrorOneOf6.md)
- [PluginPricing](docs/Model/PluginPricing.md)
- [PluginPricingOneOf](docs/Model/PluginPricingOneOf.md)
- [PluginPricingOneOf1](docs/Model/PluginPricingOneOf1.md)
- [PluginPricingOneOf2](docs/Model/PluginPricingOneOf2.md)
- [PnLItem](docs/Model/PnLItem.md)
- [PosRegister](docs/Model/PosRegister.md)
- [PosRegisterCreate](docs/Model/PosRegisterCreate.md)
- [PosRegisterStatus](docs/Model/PosRegisterStatus.md)
- [PosTable](docs/Model/PosTable.md)
- [PosTableCreate](docs/Model/PosTableCreate.md)
- [PosTableStatus](docs/Model/PosTableStatus.md)
- [PostingCategory](docs/Model/PostingCategory.md)
- [PostingCategoryCreate](docs/Model/PostingCategoryCreate.md)
- [PostingCategoryType](docs/Model/PostingCategoryType.md)
- [PostingCategoryUpdate](docs/Model/PostingCategoryUpdate.md)
- [PrecedingSalesVoucherType](docs/Model/PrecedingSalesVoucherType.md)
- [PriceTier](docs/Model/PriceTier.md)
- [PriceTierCreate](docs/Model/PriceTierCreate.md)
- [PriceTierUpdate](docs/Model/PriceTierUpdate.md)
- [PrintDeliveryNoteResponse](docs/Model/PrintDeliveryNoteResponse.md)
- [PrintLabelResponse](docs/Model/PrintLabelResponse.md)
- [Product](docs/Model/Product.md)
- [ProductAttribute](docs/Model/ProductAttribute.md)
- [ProductAttributeCreate](docs/Model/ProductAttributeCreate.md)
- [ProductAttributeUpdate](docs/Model/ProductAttributeUpdate.md)
- [ProductCategory](docs/Model/ProductCategory.md)
- [ProductCategoryCreate](docs/Model/ProductCategoryCreate.md)
- [ProductCategoryUpdate](docs/Model/ProductCategoryUpdate.md)
- [ProductCreate](docs/Model/ProductCreate.md)
- [ProductStock](docs/Model/ProductStock.md)
- [ProductUpdate](docs/Model/ProductUpdate.md)
- [ProductVariant](docs/Model/ProductVariant.md)
- [ProductVariantCreate](docs/Model/ProductVariantCreate.md)
- [ProductVariantUpdate](docs/Model/ProductVariantUpdate.md)
- [ProductionOrder](docs/Model/ProductionOrder.md)
- [ProductionOrderCosting](docs/Model/ProductionOrderCosting.md)
- [ProductionOrderStatus](docs/Model/ProductionOrderStatus.md)
- [ProductionOrderStatusUpdate](docs/Model/ProductionOrderStatusUpdate.md)
- [ProformaInvoice](docs/Model/ProformaInvoice.md)
- [ProformaInvoiceCreate](docs/Model/ProformaInvoiceCreate.md)
- [ProformaInvoiceStatus](docs/Model/ProformaInvoiceStatus.md)
- [ProformaInvoiceUpdate](docs/Model/ProformaInvoiceUpdate.md)
- [ProposedAssignment](docs/Model/ProposedAssignment.md)
- [ProviderInfo](docs/Model/ProviderInfo.md)
- [PublicDeliveryAppointmentRequest](docs/Model/PublicDeliveryAppointmentRequest.md)
- [PublicDeliveryAppointmentResponse](docs/Model/PublicDeliveryAppointmentResponse.md)
- [PublicDeliveryAppointmentStatusResponse](docs/Model/PublicDeliveryAppointmentStatusResponse.md)
- [PublicPosting](docs/Model/PublicPosting.md)
- [PublicReturnItem](docs/Model/PublicReturnItem.md)
- [PublicReturnRequest](docs/Model/PublicReturnRequest.md)
- [PublicReturnResponse](docs/Model/PublicReturnResponse.md)
- [PublicReturnStatusResponse](docs/Model/PublicReturnStatusResponse.md)
- [PurchaseOrder](docs/Model/PurchaseOrder.md)
- [PurchaseOrderCreate](docs/Model/PurchaseOrderCreate.md)
- [PurchaseOrderStatus](docs/Model/PurchaseOrderStatus.md)
- [PurchaseOrderStatusUpdate](docs/Model/PurchaseOrderStatusUpdate.md)
- [PurchaseOrderUpdate](docs/Model/PurchaseOrderUpdate.md)
- [QRCodeResponse](docs/Model/QRCodeResponse.md)
- [QuartileBand](docs/Model/QuartileBand.md)
- [QuizQuestion](docs/Model/QuizQuestion.md)
- [QuotaOverride](docs/Model/QuotaOverride.md)
- [QuotaOverrideFeatures](docs/Model/QuotaOverrideFeatures.md)
- [QuotaOverview](docs/Model/QuotaOverview.md)
- [Quotation](docs/Model/Quotation.md)
- [QuotationCreate](docs/Model/QuotationCreate.md)
- [RateRequest](docs/Model/RateRequest.md)
- [RateResponse](docs/Model/RateResponse.md)
- [RecurringTemplate](docs/Model/RecurringTemplate.md)
- [RecurringTemplateCreate](docs/Model/RecurringTemplateCreate.md)
- [RecurringTemplateType](docs/Model/RecurringTemplateType.md)
- [RecurringTemplateUpdate](docs/Model/RecurringTemplateUpdate.md)
- [ReferenceType](docs/Model/ReferenceType.md)
- [RegisterRequest](docs/Model/RegisterRequest.md)
- [ReminderLevel](docs/Model/ReminderLevel.md)
- [RemoveUserRequest](docs/Model/RemoveUserRequest.md)
- [ReorderProposalLine](docs/Model/ReorderProposalLine.md)
- [ReorderProposalResponse](docs/Model/ReorderProposalResponse.md)
- [ReplenishmentResponse](docs/Model/ReplenishmentResponse.md)
- [ReplenishmentSuggestionLine](docs/Model/ReplenishmentSuggestionLine.md)
- [ResetPasswordRequest](docs/Model/ResetPasswordRequest.md)
- [ResolvedPriceResponse](docs/Model/ResolvedPriceResponse.md)
- [ReturnLogisticsQueueItem](docs/Model/ReturnLogisticsQueueItem.md)
- [ReturnLogisticsSummary](docs/Model/ReturnLogisticsSummary.md)
- [ReturnOrder](docs/Model/ReturnOrder.md)
- [ReturnOrderStatus](docs/Model/ReturnOrderStatus.md)
- [ReturnOrderStatusUpdate](docs/Model/ReturnOrderStatusUpdate.md)
- [ReturnWarehouseSummary](docs/Model/ReturnWarehouseSummary.md)
- [RevenueItem](docs/Model/RevenueItem.md)
- [Rfq](docs/Model/Rfq.md)
- [RfqCreate](docs/Model/RfqCreate.md)
- [RfqStatus](docs/Model/RfqStatus.md)
- [RfqStatusUpdate](docs/Model/RfqStatusUpdate.md)
- [RfqUpdate](docs/Model/RfqUpdate.md)
- [SalesVolumeItem](docs/Model/SalesVolumeItem.md)
- [SalesVolumeReport](docs/Model/SalesVolumeReport.md)
- [ScopeTotal](docs/Model/ScopeTotal.md)
- [Section](docs/Model/Section.md)
- [SendMessageDto](docs/Model/SendMessageDto.md)
- [SepaDirectDebitResponse](docs/Model/SepaDirectDebitResponse.md)
- [SepaSequenceType](docs/Model/SepaSequenceType.md)
- [ServiceAssignment](docs/Model/ServiceAssignment.md)
- [ServiceAssignmentCreate](docs/Model/ServiceAssignmentCreate.md)
- [ServiceAssignmentStatus](docs/Model/ServiceAssignmentStatus.md)
- [ServiceAssignmentUpdate](docs/Model/ServiceAssignmentUpdate.md)
- [ServiceJob](docs/Model/ServiceJob.md)
- [ServiceJobCreate](docs/Model/ServiceJobCreate.md)
- [ServiceJobStatus](docs/Model/ServiceJobStatus.md)
- [ServiceJobUpdate](docs/Model/ServiceJobUpdate.md)
- [Severity](docs/Model/Severity.md)
- [Shareholder](docs/Model/Shareholder.md)
- [ShareholderCreate](docs/Model/ShareholderCreate.md)
- [ShareholderUpdate](docs/Model/ShareholderUpdate.md)
- [Shipment](docs/Model/Shipment.md)
- [ShipmentStatusUpdate](docs/Model/ShipmentStatusUpdate.md)
- [ShippingCredentials](docs/Model/ShippingCredentials.md)
- [ShippingRate](docs/Model/ShippingRate.md)
- [ShippingRule](docs/Model/ShippingRule.md)
- [ShippingRuleCreate](docs/Model/ShippingRuleCreate.md)
- [ShippingRuleUpdate](docs/Model/ShippingRuleUpdate.md)
- [ShippingThreshold](docs/Model/ShippingThreshold.md)
- [ShippingThresholdCreate](docs/Model/ShippingThresholdCreate.md)
- [ShippingThresholdUpdate](docs/Model/ShippingThresholdUpdate.md)
- [SilentPartner](docs/Model/SilentPartner.md)
- [SilentPartnerCreate](docs/Model/SilentPartnerCreate.md)
- [SilentPartnerUpdate](docs/Model/SilentPartnerUpdate.md)
- [SmtpConfig](docs/Model/SmtpConfig.md)
- [SmtpEncryption](docs/Model/SmtpEncryption.md)
- [StilleExportResponse](docs/Model/StilleExportResponse.md)
- [StillePartnerZeile](docs/Model/StillePartnerZeile.md)
- [StilleReport](docs/Model/StilleReport.md)
- [StockAdjustment](docs/Model/StockAdjustment.md)
- [StockMovement](docs/Model/StockMovement.md)
- [StockTransfer](docs/Model/StockTransfer.md)
- [StockTransferStatus](docs/Model/StockTransferStatus.md)
- [StockTransferStatusUpdate](docs/Model/StockTransferStatusUpdate.md)
- [StockUpdateRequest](docs/Model/StockUpdateRequest.md)
- [SubmitResultDto](docs/Model/SubmitResultDto.md)
- [SubmitResultResponse](docs/Model/SubmitResultResponse.md)
- [SubscriptionOverview](docs/Model/SubscriptionOverview.md)
- [SuitabilityRequest](docs/Model/SuitabilityRequest.md)
- [SuitabilityResult](docs/Model/SuitabilityResult.md)
- [SupplierCondition](docs/Model/SupplierCondition.md)
- [SupplierConditionCreate](docs/Model/SupplierConditionCreate.md)
- [SupplierConditionUpdate](docs/Model/SupplierConditionUpdate.md)
- [SupplierInvoice](docs/Model/SupplierInvoice.md)
- [SupplierInvoiceCreate](docs/Model/SupplierInvoiceCreate.md)
- [SupplierInvoiceStatus](docs/Model/SupplierInvoiceStatus.md)
- [SupplierInvoiceStatusUpdate](docs/Model/SupplierInvoiceStatusUpdate.md)
- [SupplierInvoiceUpdate](docs/Model/SupplierInvoiceUpdate.md)
- [SupportChannel](docs/Model/SupportChannel.md)
- [SupportChannelType](docs/Model/SupportChannelType.md)
- [SupportTicket](docs/Model/SupportTicket.md)
- [SupportTicketStatus](docs/Model/SupportTicketStatus.md)
- [SupportTicketUpdate](docs/Model/SupportTicketUpdate.md)
- [SyncLog](docs/Model/SyncLog.md)
- [SyncLogStatus](docs/Model/SyncLogStatus.md)
- [SyncStatus](docs/Model/SyncStatus.md)
- [SyncSummary](docs/Model/SyncSummary.md)
- [SyncType](docs/Model/SyncType.md)
- [TargetProgress](docs/Model/TargetProgress.md)
- [TaxRateCreate](docs/Model/TaxRateCreate.md)
- [Team](docs/Model/Team.md)
- [TeamCreate](docs/Model/TeamCreate.md)
- [TenantSettings](docs/Model/TenantSettings.md)
- [TenantUser](docs/Model/TenantUser.md)
- [TicketMessage](docs/Model/TicketMessage.md)
- [TicketPriority](docs/Model/TicketPriority.md)
- [TimeEntryClockIn](docs/Model/TimeEntryClockIn.md)
- [TimeEntryClockOut](docs/Model/TimeEntryClockOut.md)
- [TimeEntryDto](docs/Model/TimeEntryDto.md)
- [TimelineEvent](docs/Model/TimelineEvent.md)
- [TotpEnableRequest](docs/Model/TotpEnableRequest.md)
- [TotpSetupResponse](docs/Model/TotpSetupResponse.md)
- [TrackOrderRequest](docs/Model/TrackOrderRequest.md)
- [TrackOrderResponse](docs/Model/TrackOrderResponse.md)
- [TrackedShipment](docs/Model/TrackedShipment.md)
- [TrackingEvent](docs/Model/TrackingEvent.md)
- [TrackingInfo](docs/Model/TrackingInfo.md)
- [TrainingAssignment](docs/Model/TrainingAssignment.md)
- [TrainingAssignmentCreate](docs/Model/TrainingAssignmentCreate.md)
- [TrainingAssignmentUpdate](docs/Model/TrainingAssignmentUpdate.md)
- [TrainingContent](docs/Model/TrainingContent.md)
- [TrainingSource](docs/Model/TrainingSource.md)
- [UmsatzsteuerReport](docs/Model/UmsatzsteuerReport.md)
- [UpdateAutomation](docs/Model/UpdateAutomation.md)
- [UpdateChannelDto](docs/Model/UpdateChannelDto.md)
- [UpdateConnectionRequest](docs/Model/UpdateConnectionRequest.md)
- [UpdatePermissionsPayload](docs/Model/UpdatePermissionsPayload.md)
- [UpdateProfileRequest](docs/Model/UpdateProfileRequest.md)
- [UpdateRolePayload](docs/Model/UpdateRolePayload.md)
- [UpdateSubscriptionRequest](docs/Model/UpdateSubscriptionRequest.md)
- [UpdateSyncDirectionRequest](docs/Model/UpdateSyncDirectionRequest.md)
- [UpdateTenantSettings](docs/Model/UpdateTenantSettings.md)
- [UpsCredentials](docs/Model/UpsCredentials.md)
- [UsageSnapshot](docs/Model/UsageSnapshot.md)
- [UserProfile](docs/Model/UserProfile.md)
- [UserTenantInfo](docs/Model/UserTenantInfo.md)
- [UstvaErgebnis](docs/Model/UstvaErgebnis.md)
- [VatDetail](docs/Model/VatDetail.md)
- [VatItem](docs/Model/VatItem.md)
- [VatSummary](docs/Model/VatSummary.md)
- [Verfahrensdokumentation](docs/Model/Verfahrensdokumentation.md)
- [VerifyEmailRequest](docs/Model/VerifyEmailRequest.md)
- [Voucher](docs/Model/Voucher.md)
- [VoucherCreate](docs/Model/VoucherCreate.md)
- [VoucherStatus](docs/Model/VoucherStatus.md)
- [VoucherType](docs/Model/VoucherType.md)
- [Warehouse](docs/Model/Warehouse.md)
- [WarehouseCreate](docs/Model/WarehouseCreate.md)
- [WarehouseStock](docs/Model/WarehouseStock.md)
- [WarehouseUpdate](docs/Model/WarehouseUpdate.md)
- [WebhookDirection](docs/Model/WebhookDirection.md)
- [WebhookEvent](docs/Model/WebhookEvent.md)
- [WebhookEventStatus](docs/Model/WebhookEventStatus.md)
- [WebhookSubscription](docs/Model/WebhookSubscription.md)
- [Workflow](docs/Model/Workflow.md)
- [WorkflowAction](docs/Model/WorkflowAction.md)
- [WorkflowEnabledUpdate](docs/Model/WorkflowEnabledUpdate.md)
- [XRechnungResponse](docs/Model/XRechnungResponse.md)
- [YearTotal](docs/Model/YearTotal.md)
- [YearlyPayrollSummary](docs/Model/YearlyPayrollSummary.md)

## Authorization

Authentication schemes defined for the API:
### bearer_token

- **Type**: Bearer authentication (JWT)

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

support@simplebilly.com

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `0.1.0`
    - Generator version: `7.25.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`

---

## SimpleBilly API SDK

This client was generated automatically from the [SimpleBilly OpenAPI specification](https://simplebilly.com/api/docs).

- **Homepage:** https://simplebilly.com
- **API documentation:** https://simplebilly.com/api/docs
- **OpenAPI specification:** https://api.simplebilly.com/openapi.json
- **SDK sources:** https://github.com/simplebilly

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) — do not edit generated code by hand.

## Security

See [SECURITY.md](SECURITY.md) for reporting vulnerabilities.

## License

[MIT](LICENSE) — Copyright (c) SimpleBilly GmbH.

SimpleBilly is the first bookkeeping, CRM, online shop and ERP that follows the mantra: "just do it"

*Generated by the SimpleBilly SDK pipeline — do not edit manually.*
