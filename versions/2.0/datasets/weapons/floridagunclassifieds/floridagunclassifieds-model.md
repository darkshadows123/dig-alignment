## extracted_floridagunclassifieds.json

### PyTransforms
#### _uri_
From column: _uri_
>``` python
return uri_from_url_timestamp(getValue("url"),getValue('timestamp'))
```

#### _cleanPrice_
From column: _price_
>``` python
return price_quantity_us_number(getValue("price"))
```

#### _priceCurrency_
From column: _price_
>``` python
return price_currency(getValue("price"))
```

#### _listedOnDate_
From column: _Unfold: label / listed: / Values_
>``` python
return iso8601date(getValue("Values"))
```

#### _clean_member_since_
From column: _member_since_
>``` python
return iso8601date(getValue("member_since"))
```

#### _personororganizationUri_
From column: _uri_
>``` python
return getValue("uri") + "/personOrOrganization"
```

#### _product_uri_
From column: _uri_
>``` python
return getValue("uri") + "/product"
```

#### _location_enhanced_
From column: _address_
>``` python
return getEnhancedLocation(getValue("address"))
```

#### _place_uri_
From column: _uri_
>``` python
return getValue("uri")+"/placeuri"
```

#### _clean_phone_
From column: _Unfold: label / phone number: / Values_
>``` python
return clean_phone(getValue("Values"))
```

#### _contact_point_uri_
From column: _username_
>``` python
return uri_from_fields('floridagunclassifieds/person/', getValue("username"))
```


### Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _Values_ | `schema:addressLocality` | `schema:PostalAddress1`|
| _Values_ | `schema:manufacturer` | `schema:Product1`|
| _Values_ | `schema:email` | `schema:ContactPoint1`|
| _Values_ | `schema:keywords` | `schema:Product1`|
| _cleanPrice_ | `schema:price` | `schema:Offer1`|
| _clean_member_since_ | `schema:startDate` | `schema:OrganizationRole1`|
| _clean_phone_ | `schema:name` | `memex:PhoneNumber1`|
| _contact_point_uri_ | `uri` | `schema:ContactPoint1`|
| _listedOnDate_ | `schema:availabilityStarts` | `schema:Offer1`|
| _location_enhanced_ | `schema:name` | `schema:PostalAddress1`|
| _organizationuri_ | `uri` | `schema:Organization1`|
| _personororganizationUri_ | `uri` | `memex:PersonOrOrganization1`|
| _place_uri_ | `uri` | `schema:Place1`|
| _priceCurrency_ | `schema:priceCurrency` | `schema:Offer1`|
| _product_uri_ | `uri` | `schema:Product1`|
| _rawtextdetectedlanguage_ | `schema:inLanguage` | `schema:Offer1`|
| _title_ | `schema:title` | `schema:Offer1`|
| _uri_ | `uri` | `schema:Offer1`|
| _url_ | `schema:url` | `schema:Offer1`|
| _user_id_ | `schema:name` | `memex:Identifier1`|
| _username_ | `schema:name` | `schema:ContactPoint1`|
| _values_ | `schema:description` | `schema:Offer1`|
| _values_ | `schema:name` | `schema:Product1`|


### Links
| From | Property | To |
|  --- | -------- | ---|
| `memex:PersonOrOrganization1` | `schema:contactPoint` | `schema:ContactPoint1`|
| `memex:PersonOrOrganization1` | `schema:memberOf` | `schema:OrganizationRole1`|
| `schema:ContactPoint1` | `memex:identifier` | `memex:Identifier1`|
| `schema:ContactPoint1` | `schema:telephone` | `memex:PhoneNumber1`|
| `schema:Offer1` | `schema:availableAtOrFrom` | `schema:Place1`|
| `schema:Offer1` | `schema:itemOffered` | `schema:Product1`|
| `schema:Offer1` | `schema:publisher` | `schema:Organization1`|
| `schema:Offer1` | `schema:seller` | `memex:PersonOrOrganization1`|
| `schema:Organization1` | `schema:name` | `xsd:floridagunclassifieds.com`|
| `schema:OrganizationRole1` | `schema:memberOf` | `schema:Organization1`|
| `schema:Place1` | `schema:address` | `schema:PostalAddress1`|
| `schema:Product1` | `schema:offers` | `schema:Offer1`|
