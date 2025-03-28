# Schema.org Simplified Vocabulary

`<https://example.org/schema>`

```
@prefix schema: <https://schema.org/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@base <https://example.org/schema> .
```

This document describes a simplified subset of Schema.org vocabulary, designed to be particularly LLM-friendly. Each entity includes human-readable descriptions and examples to help language models understand the concepts better.

## Person

`schema:Person`

A person (alive, dead, undead, or fictional) with associated properties that describe their attributes and relationships.

### Description

`rdfs:comment`

- `"A Person represents a human being, real or fictional. The Person type includes properties for describing attributes like name, birthdate, and address, as well as relationships to organizations, other people, and creative works."`

### Has Name

`schema:name`

- `"John Doe"` - A person's full name as commonly used for identification
- `"Jane Smith"` - Names should be provided in the format most commonly used

### Has Given Name

`schema:givenName`

- `"John"` - A person's first name or given name
- `"Jane"` - The name that appears first in a person's full name

### Has Family Name

`schema:familyName`

- `"Doe"` - A person's last name or family name
- `"Smith"` - The name that appears last in a person's full name

### Has Birth Date

`schema:birthDate`

- `"1990-01-01"^^xsd:date` - The date of birth in ISO 8601 format (YYYY-MM-DD)
- `"2000-12-31"^^xsd:date` - Always use the full year, month, and day when known

### Has Job Title

`schema:jobTitle`

- `"Software Engineer"` - A person's job title or position
- `"Chief Executive Officer"` - The role a person plays in an organization

### Works For

`schema:worksFor`

- `schema:Organization` - The organization that employs the person
- A link to the organization where the person is employed

## Organization

`schema:Organization`

An organization such as a school, NGO, corporation, club, or any other group of people with a formal or informal structure.

### Description

`rdfs:comment`

- `"An Organization represents a collection of people organized together into a community or other social, commercial or political structure. Organizations can be corporations, schools, government agencies, clubs, etc."`

### Has Name

`schema:name`

- `"Acme Corporation"` - The official name of the organization
- `"State University"` - Use the full, formal name when possible

### Has Legal Name

`schema:legalName`

- `"Acme Corporation, Inc."` - The official name as registered in legal documents
- `"State University Foundation"` - May include legal designations like Inc., LLC, etc.

### Has URL

`schema:url`

- `"https://example.com"` - The organization's official website URL
- `"https://university.edu"` - Should be the primary or canonical URL

### Has Address

`schema:address`

- `schema:PostalAddress` - The physical location of the organization
- Links to a postal address that contains street, city, and other details

## PostalAddress

`schema:PostalAddress`

The mailing address for a person, organization, or place.

### Description

`rdfs:comment`

- `"A PostalAddress represents a physical address, typically consisting of street address, locality (city), region, postal code, and country."`

### Has Street Address

`schema:streetAddress`

- `"123 Main St."` - The street number, name, and unit or apartment number
- `"456 Park Ave, Suite 789"` - Should include all details needed for mail delivery

### Has City

`schema:addressLocality`

- `"New York"` - The city or locality name
- `"San Francisco"` - Use the common name of the city, not abbreviations

### Has Region

`schema:addressRegion`

- `"NY"` - The state, province, or region, often abbreviated
- `"California"` - Can be full name or standard abbreviation depending on locale

### Has Postal Code

`schema:postalCode`

- `"10001"` - The postal or zip code
- `"94103"` - Format varies by country

### Has Country

`schema:addressCountry`

- `"US"` - The country, preferably as an ISO 3166-1 alpha-2 code
- `"United States"` - Can also be the full country name
