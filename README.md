# XML & SOAP API Modeling — Content Filter for Streaming Service
 
<table>
<tr>
<td>

This repository contains XML schema updates for the SOAP-based content API of an online cinema platform.
  
Artifacts demonstrate how existing SOAP contracts were analyzed and extended to support a new business requirement without breaking current integrations.
 
The change enables filtering the catalog by exclusive titles to highlight unique value after new studio contracts.

</td>
<td width="220">
<img src="https://github.com/edmnikolaeva/xml/blob/main/xml_sample.png" 
     alt="Visual Anchor — Main Screen Prototype" 
     width="200"/>
</td>
</tr>
</table>

---

### 🧩 Main Artifacts

- 👉 [Request XML Schema](https://github.com/edmnikolaeva/xml/blob/main/GetContentListRequest.xsd)  
- 👉 [Response XML Schema](https://github.com/edmnikolaeva/xml/blob/main/GetContentListResponse.xsd)  
- 👉 [Development Ticket](https://github.com/edmnikolaeva/xml/blob/main/%D1%82%D0%B8%D0%BA%D0%B5%D1%82_%D0%BD%D0%B0_%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D1%83.pdf)

---

### 🧭 Business Context

- **Domain:** online cinema streaming service
- **Scope:** content listing endpoint (`/content/list`) & microservices architecture (Web Server / API layer → Films & Series services)
- **Goal:** enable users to filter the library by exclusive content to emphasize platform uniqueness

---

**Key Pain Points**

- Exclusive content existed but was not discoverable via filtering  
- API did not support exclusivity-based queries  
- UI could not expose the new business capability  

**Business Value**  
- Showcase exclusive studio deals → strengthen competitive positioning  
- Increase perceived value of subscription  
- Drive user engagement with unique catalog highlights

**Solution**

- Analyzed existing SOAP APIs across Web Server, Films, and Series services  
- Identified the operation requiring extension: `/content/list`  
- Extended request schema with `exclusive` parameter  
- Extended response schema to expose exclusivity flag  
- Defined backend filtering logic  

---

### ⚙️ Technical Notes

- Architecture: microservices  
- Integration style: SOAP  
- Data format: XML  
- Existing Films and Series services already expose `exclusive` attribute  
- Changes implemented at Web Server aggregation layer  

---

### 👩‍💼 My Role / Workflow

- Reviewed service architecture  
- Analyzed existing SOAP contracts  
- Identified required API changes  
- Designed XSD updates for request and response  
- Prepared implementation task for backend team  

---

### 🔗 Related Artifacts

- 👉 [JSON](https://github.com/edmnikolaeva/json)  
- 👉 [REST](https://github.com/edmnikolaeva/rest)
- 👉 [Architecture](https://github.com/edmnikolaeva/architecture)
