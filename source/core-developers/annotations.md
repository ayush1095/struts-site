---
layout: core-developers
title: Annotations
---

# Annotations

In many places, applications can use Java 5 annotations as an alternative to XML and Java properties configuration\. This page serves as a reference for all annotations across the framework\.

####Action Annotations####


Since 2\.1, these annotations are provided by the _Convention Plugin_ \. Codebehind and Zero Config plugins are deprecated from 2\.1 on\.

| 

Action annotations are available when the framework scans the classpath for Action classes, rather than specifying individual mappings through XML configuration\. See the _Convention Plugin_  page for information on how to set up classpath scanning to allow the use of Action annotations\.

|Annotation|Description|
|----------|-----------|
|_Actions Annotation_ |Group of @Action annotations, maps multiple URLs to the same action|
|_Action Annotation_ |Defines the URL of an action|
|_InterceptorRefs Annotation_ |Gropup of @InterceptorRef annotations|
|_InterceptorRef Annotation_ |Interceptor, or interceptor stack to be applied to at action|
|_Results Annotation_ |Group of @Result annotations|
|[Result Annotation](result-annotation.html)|Defines a result for an action|
|[Namespace Annotation](namespace-annotation.html)|Set the path of the action URL (used to overwrite the default)|
|_ResultPath Annotation_ |Set where the results are located (used to overwrite the default)|
|[ParentPackage Annotation](parent-package-annotation.html)|Set the parent package of the actions (used to overwrite the default)|
|_ExceptionMappings_ |Group of @ExceptionMapping annotations|
|_ExceptionMapping_ |Defines an exception mapping|

####Workflow Annotations####

|Annotation|Description|
|----------|-----------|
|[InputConfig Annotation](input-config-annotation.html)|Defines what method to execute, or result to be returned if there are validation errors|

####Interceptor Annotations####

To use these annotations, you have to specify the [AnnotationWorkflowInterceptor](annotation-workflow-interceptor.html) to your interceptor stack\.

|Annotation|Description|
|----------|-----------|
|[After Annotation](after-annotation.html)|Marks a action method that needs to be executed after the result\.|
|[Before Annotation](before-annotation.html)|Marks a action method that needs to be executed before the main action method\.|
|[BeforeResult Annotation](before-result-annotation.html)|Marks a action method that needs to be executed before the result\.|

####Validation Annotations####

To use annotation\-based validation, annotate the class or interface with [Validation Annotation](validation-annotation.html).

|Annotation|Description|
|----------|-----------|
|[ConversionErrorFieldValidator Annotation](conversion-error-field-validator-annotation.html)|Checks if there are any conversion errors for a field\.|
|[DateRangeFieldValidator Annotation](date-range-field-validator-annotation.html)|Checks that a date field has a value within a specified range\.|
|[DoubleRangeFieldValidator Annotation](double-range-field-validator-annotation.html)|Checks that a double field has a value within a specified range\.|
|[EmailValidator Annotation](email-validator-annotation.html)|Checks that a field is a valid e\-mail address\.|
|[ExpressionValidator Annotation](expression-validator-annotation.html)|Validates an expression\.|
|[FieldExpressionValidator Annotation](field-expression-validator-annotation.html)|Uses an OGNL expression to perform its validator\.|
|[IntRangeFieldValidator Annotation](int-range-field-validator-annotation.html)|Checks that a numeric field has a value within a specified range\.|
|[RegexFieldValidator Annotation](regex-field-validator-annotation.html)|Validates a regular expression for a field\.|
|[RequiredFieldValidator Annotation](required-field-validator-annotation.html)|Checks that a field is non\-null\.|
|[RequiredStringValidator Annotation](required-string-validator-annotation.html)|Checks that a String field is not empty\.|
|[StringLengthFieldValidator Annotation](string-length-field-validator-annotation.html)|Checks that a String field is of the right length\.|
|[UrlValidator Annotation](url-validator-annotation.html)|Checks that a field is a valid URL\.|
|[Validation Annotation](validation-annotation.html)|Marker annotation for validation at Type level\.|
|[Validations Annotation](validations-annotation.html)|Used to group validation annotations\.|
|[VisitorFieldValidator Annotation](visitor-field-validator-annotation.html)|Invokes the validation for a property's object type\.|
|[CustomValidator Annotation](custom-validator-annotation.html)|Use this annotation for your custom validator types\.|

#####Resources#####

+ [Validation using Annotations](http://arsenalist\.com/2007/05/10/struts\-2\-validation\-using\-annotations/)^[http://arsenalist\.com/2007/05/10/struts\-2\-validation\-using\-annotations/] (arsenalist)

####Type Conversion Annotations####

By default, type conversion for Maps and Collections using generics is directly supported\.

In short, instead of specifying the types found in collections and maps as documented in [Type Conversion](type-conversion.html), **the collection's generic type is used**\. By using annotations, an application should be able to avoid using any 

~~~~~~~
ClassName-conversion.properties
~~~~~~~
 files\.

To use annotation\-based type conversion, annotate the class or interface with the [Conversion Annotation](conversion-annotation.html).

|Annotation|Description|
|----------|-----------|
|[Conversion Annotation](conversion-annotation.html)|Marker annotation for type conversions at Type level\.|
|[CreateIfNull Annotation](create-if-null-annotation.html)|For Collection and Map types: Create the types within the Collection or Map, if null\.|
|[Element Annotation](element-annotation.html)|For Generic types: Specify the element type for Collection types and Map values\.|
|[Key Annotation](key-annotation.html)|For Generic types: Specify the key type for Map keys\.|
|[KeyProperty Annotation](key-property-annotation.html)|For Generic types: Specify the key property name value\.|
|[TypeConversion Annotation](type-conversion-annotation.html)|Used for class and application wide conversion rules\.|

####Tiles Annotations####

The _Tiles Plugin_  provides it's own set of Annotations\. They can be used to keep 

~~~~~~~
tiles.xml
~~~~~~~
 short\. Instead tiles definitions can be created by annotating actions\.

|Annotation|Description|
|----------|-----------|
|TilesDefinition|Represents a \<definition\> element in tiles\.xml|
|TilesDefinitions|A list of TilesDefinition Annotations|
|TilesPutAttribute|Represents a \<put\-attribute\> element in tiles\.xml|
|TilesPutListAttribute|Represents a \<put\-list\-attribute\> element in tiles\.xml|
|TilesAddAttribute|Represents a \<add\-attribute\> element in tiles\.xml|
|TilesAddListAttribute|Represents a \<add\-list\-attribute\> element in tiles\.xml|

 