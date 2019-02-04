---
title: Rendering Forms
seo-title: Rendering Forms
description: null
seo-description: null
uuid: 31915c8e-e1f7-42be-86dc-2cbbe3228890
contentOwner: admin
content-type: reference
geptopics: SG_AEMFORMS/categories/performing_service_operations_using_apis
products: SG_EXPERIENCEMANAGER/6.4/FORMS
topic-tags: operations
discoiquuid: 022490c9-ccab-49b3-af74-ea08650fa3de
index: y
internal: n
snippet: y
---

# Rendering Forms{#rendering-forms}

## Rendering Forms {#rendering-forms}

**About the Forms service**

The Forms service lets you create interactive data capture client applications that validate, process, transform, and deliver forms typically created in Designer. Form authors can develop a single form design that the Forms service renders in PDF, SWF, or HTML in various browser environments.

When an end-user requests a form, a client application sends the request to the Forms service, which returns the form in an appropriate format. As soon as the Forms service receives a request, it merges data with a form design and then delivers the form in the desired format. The Form service output is an interactive form, typically a PDF document. An interactive form enables users to fill in fields located on the form.

Depending upon the type of client application, you can write the form to a client web browser or save the form as a PDF file. A web-based application can write the form to web browser. A desktop application can save the form as a PDF file. To demonstrate how to write out to a web browser and to a PDF file, the quick starts located in the *Rendering Forms* section are organized in the following manner:

* The Java API strongly typed (SOAP mode) examples are a Java servlet.
* The web service (Java Base64) examples are a Java servlet.
* The web service (MTOM) examples are a console application (not all quick starts have a MTOM example).

  ***Note**: For information about creating a web application that uses java servlets to invoke the Forms service, see [Creating Web Applications that Renders Forms](/programming-with-aem-forms/rendering-forms-rendering-forms creating-web-applications-renders-forms#creating_web_applications_that_renders_forms). *

  You can pass a form design (an XDP file) or a PDF document to the Forms service using one of two ways:

* You can reference the form design using a URL value. This approach involves using a `URLSpec` object. The content root is passed to the Forms service using the `URLSpec` object’s `setContentRootURI` method. The Form design name ( `formQuery`) is passed as a separate parameter. The two values are concatenated to get the absolute reference to the form design. (Most of the quick starts located in the *Rendering Forms* section use this approach.)
* You can pass a `com.adobe.idp.Document` that contains the form design to the Forms service. Two new methods named `renderPDFForm2` and `renderHTMLForm2` accept a `com.adobe.idp.Document` object that contains a form design. (See [Passing Documents to the Forms Service](/programming-with-aem-forms/rendering-forms-rendering-forms passing-documents-forms-service-passing#passing_documents_to_the_forms_service).)

  You can accomplish these tasks using the Forms service:

* Render interactive PDF forms. (See [Rendering Interactive PDF Forms](/programming-with-aem-forms/rendering-forms-rendering-forms rendering-interactive-pdf-forms-rendering#rendering_interactive_pdf_forms).)
* Render forms at the client. (See [Rendering Forms at the Client](/programming-with-aem-forms/rendering-forms-rendering-forms rendering-forms-client-rendering-forms#rendering_forms_at_the_client).)
* Render forms based on fragments. (See [Rendering Forms Based on Fragments](/programming-with-aem-forms/rendering-forms-rendering-forms rendering-forms-based-fragments-rendering#rendering_forms_based_on_fragments).)
* Render rights-enabled forms. (See [Rendering Rights-Enabled Forms](/programming-with-aem-forms/rendering-forms-rendering-forms rendering-rights-enabled-forms-rendering#rendering_rights_enabled_forms).)
* Render forms as HTML. (See [Rendering Forms as HTML](/programming-with-aem-forms/rendering-forms-rendering-forms rendering-forms-html-rendering-forms rendering-forms-html-rendering-forms#rendering_forms_as_html).)
* Rendering HTML Forms Using Custom CSS Files ([Rendering HTML Forms Using Custom CSS Files](/programming-with-aem-forms/rendering-forms-rendering-forms rendering-html-forms-using-custom#rendering_html_forms_using_custom_css_files).)
* Handle submitted forms. (See [Handling Submitted Forms](/programming-with-aem-forms/rendering-forms-rendering-forms handling-submitted-forms-handling-submitted#handling_submitted_forms).)
* Creating PDF Documents with Submitted XML Data. (See [Creating PDF Documents with Submitted XML Data](/programming-with-aem-forms/rendering-forms-rendering-forms creating-pdf-documents-submitted-xml#creating_pdf_documents_with_submitted_xml_data).)
* Prepopulate forms. (See [Prepopulating Forms with Flowable Layouts](/programming-with-aem-forms/rendering-forms-rendering-forms prepopulating-forms-flowable-layouts-prepopulating#prepopulating_forms_with_flowable_layouts).)
* Passing Documents. (See [Passing Documents to the Forms Service](/programming-with-aem-forms/rendering-forms-rendering-forms passing-documents-forms-service-passing#passing_documents_to_the_forms_service).)
* Calculate form data. (See [Calculating Form Data](/programming-with-aem-forms/rendering-forms-rendering-forms calculating-form-data-calculating-form calculating-form-data-calculating-form#calculating_form_data).)
* Optimize an application. (See [Optimizing the Performance of the Forms Service](/programming-with-aem-forms/rendering-forms-rendering-forms optimizing-performance-forms-service-optimizing#optimizing_the_performance_of_the_forms_service).)

  ***Tip**: The Adobe Developer web site contains the following article that discusses how to create a ASP.NET application that invokes the Forms service and renders forms. See [Creating form rendering ASP.NET applications](http://www.adobe.com/devnet/livecycle/articles/asp_net.html)*.**

>[!MORE_LIKE_THIS]
>
>* [Quick Start (Base64): Rendering an interactive PDF form using the web service API](#unresolvedlink-lc-qs-forms-fo.xml#ws624e3cba99b79e12e69a9941333732bac8-7e44.2)
>* [Quick Start (SOAP mode): Rendering an interactive PDF form using the Java API](#unresolvedlink-lc-qs-forms-fo.xml#ws624e3cba99b79e12e69a9941333732bac8-7e45.2)
>* [Invoking Forms using Base64 encoding](#unresolvedlink-lc-in-invoke-using-web-services-iu.xml#ws624e3cba99b79e12e69a9941333732bac8-7fca.2)
>* [Including AEM Forms Java library files](#unresolvedlink-lc-in-invoke-using-java-iu.xml#ws624e3cba99b79e12e69a9941333732bac8-7b4b.2)
