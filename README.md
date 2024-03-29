## Overview

The AGID Template implements the [Municipality design kit](https://italia.github.io/design-comuni-prototipi/esempi/bootstrap-italia/template-homepage.html) by [Agenzia per l'Italia digitale (AGID)](https://www.agid.gov.it/it/design-servizi/linee-guida-design-servizi-digitali-pa).
The information architecture included in the Municipalities design kit is a starting point to create a complete UX solution and to manage contents and elements.
The template page templates, based on the [Designers Italia UI](https://designers.italia.it/modello/comuni/) Kit and the [Bootstrap Italia library](https://italia.github.io/bootstrap-italia/), serve to speed up the creation of the front-end of the site and are useful as examples of pages and contents.

**Warning:** The AGID Template is meant to be the starting point for a new site. During installation you will receive a warning that a few stock or out-of-the-box components will be overridden. If you choose to skip one or more of these components during the installation process (using the Install Plan options in the App Builder) there may be visual and/or functional side effects.
* fragment/jacms_content_viewer_list
* fragment/jacms_content_viewer
* pages/home_page

## Installation:

### Prerequisites

A working instance of Entando running on Kubernetes. See the [Entando developer site](https://developer.entando.com) for more information.

### Install via the Entando Hub

1. See the install instructions for the AGID Template in the [Entando Cloud Hub](https://hub.entando.com). You may need to first [configure your AppBuilder](https://developer.entando.com/v7.0/tutorials/solution/entando-hub.html#configuration) (7.0+) to point to the Cloud Hub.
2. Deploy and install the AGID Template

3. Navigate to your AGID Template by going to the App Builder and then `Page → Management → Home page`
   - Find the Home page
   - From the Actions pull-down menu → View Published Page

### Instructions for Search Widget

1. Navigate to `Content -> Types`
   - Click on `Edit` on each type with code ARG, CRN, NOV and SRV
   - Set the `Default content model for lists` as "Lista" followed by the content type's code (e.g. "Lista (ARG)" for the "ARG" type)
2. Go to App Builder and then `Content -> Settings`
   - Click on `Reload the references`
   - Click on `Reload the indexes`
   
### (Optional) Set portal's default language to Italian

1. Access to \*port database
2. Open sysconfig table
3. Modify lang column as it follows:

```<?xml version="1.0" encoding="UTF-8"?>
<Langs>
	<Lang>
		<code>it</code>
		<descr>Italiano</descr>
		<default>true</default>
	</Lang>
	<Lang>
		<code>en</code>
		<descr>English</descr>
	</Lang>
</Langs>
```
