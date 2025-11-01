# DBeaver Agent

- **Product ID**: `dbeaver-ee`  
- **Product Version**: `6.3`  
- **License ID**: `DB-ZS1MPZK4--FVE`

## `checkLicenseStatus`

**Response**:  
```
VALID: Ok
```

## `checkCustomerEmail`

**Response**:  
Returns a suspected user ID.

The request header contains a field named `X-Referrer` with the value `clientId`, which likely corresponds to the user ID obtained above.

## `generateTrialLicense`

**Response Format**:
```
-- DBeaver EE LICENSE - DB-ZS1MPZT9--FUB
-- Issued at Tue Jan 28 17:04:37 UTC 2020 to Mr Wu //
GcEVPtVH+fzyCX3Jw/b2iDGHIYe20IwwGGzvCaSvgN+SOLyeOfmhTgIXkhhuJsCi7Ov/7Sy2Hpk3
VdHjehLS727GlKOKKKkZ6s9C8bt+Aw4WEhDsivOJpQt5eLUjvDLhZC0ols4R9kIXHRo1KcS5AaHy
8EWhdiuxPOJdHTR01waJUvb4RdH8Ldi2m2CNB93sv1OTMvzoDX1oWUnWGN8mL7K0UU+3ksy06a0O
/AU8wueD1yaXHQp9OML5WmBDZapiuSKoQUH/dPhu6C7XRj1EAiTueNibb9rSfbhlUYKgA/1is4nW
42xwiN3+jzQrBYO1NQIYAlGHxlsJ0+IxqVLHCw==
```

**Request Format**:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<request license="utilmate" productId="dbeaver-ee" productVersion="6.3">
	<customer email="user@example.com" firstName="XXX" lastName="XXX" company=""></customer>
</request>
```

> **Note**: The `Content-Type` header must be set to `text/xml`.

## `LicenseKeyProvider`

- **Class Path**: `com/dbeaver/ee/runtime/lm/DBeaverEnterpriseLM$LicenseKeyProvider`  
- **Full Class Name**: `com.dbeaver.ee.runtime.lm.DBeaverEnterpriseLM$LicenseKeyProvider`
