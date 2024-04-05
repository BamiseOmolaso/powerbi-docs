---
title: "Max function in a Power BI paginated report"
description: Learn about the Max function in a Power BI paginated report, which returns the maximum value of all non-null numeric values specified by the expression in Report Builder.
author: maggiesMSFT
ms.author: maggies
ms.date: 04/28/2023
ms.service: powerbi
ms.subservice: report-builder
ms.topic: conceptual
ms.custom: updatefrequency5
ms.reviewer: spendrick
---
# Max function in a Power BI paginated report

[!INCLUDE [applies-yes-report-builder-no-desktop](../../includes/applies-yes-report-builder-no-desktop.md)]

  Returns the maximum value of all non-null numeric values specified by the expression, in the context of the given scope in a Power BI paginated report.  
  
## Syntax  
  
```  
  
Max(expression, scope, recursive)  
```  
  
### Parameters  
 *expression*  
 (**Variant**) The expression on which to perform the aggregation.  
  
 *scope*  
 (**String**) Optional. The name of a dataset, group, or data region that contains the report items to which to apply the aggregate function. If *scope* isn't specified, the current scope is used.  
  
 *recursive*  
 (**Enumerated Type**) Optional. **Simple** (default) or **RdlRecursive**. Specifies whether to perform the aggregation recursively.  
  
## Return type  
 Determined by the type of the expression.  
  
## Remarks  
 The set of data specified in the expression must have the same data type. To convert data that has multiple numeric data types to the same data type, use conversion functions like **CInt**, **CDbl** or **CDec**. For more information, see [Type Conversion Functions](/dotnet/visual-basic/language-reference/functions/type-conversion-functions).  
  
 The value of *scope* must be a string constant and can't be an expression. For outer aggregates or aggregates that don't specify other aggregates, *scope* must refer to the current scope or a containing scope. For aggregates of aggregates, nested aggregates can specify a child scope.  
  
 *Expression* can contain calls to nested aggregate functions with the following exceptions and conditions:  
  
-   *Scope* for nested aggregates must be the same as, or contained by, the scope of the outer aggregate. For all distinct scopes in the expression, one scope must be in a child relationship to all other scopes.  
  
-   *Scope* for nested aggregates can't be the name of a dataset.  
  
-   *Expression* must not contain **First**, **Last**, **Previous**, or **RunningValue** functions.  
  
-   *Expression* must not contain nested aggregates that specify *recursive*.  
  
 For more information, see [Aggregate Functions Reference &#40;Report Builder)](/sql/reporting-services/report-design/report-builder-functions-aggregate-functions-reference) and [Expression Scope for Totals, Aggregates, and Built-in Collections &#40;Report Builder and SSRS&#41;](/sql/reporting-services/report-design/expression-scope-for-totals-aggregates-and-built-in-collections).  
  
 For more information about recursive aggregates, see [Creating Recursive Hierarchy Groups &#40;Report Builder and SSRS&#41;](/sql/reporting-services/report-design/creating-recursive-hierarchy-groups-report-builder-and-ssrs).  
  
## Example  
 The following code example provides the highest total in the `Year` group or data region.  
  
```  
=Max(Fields!OrderTotal.Value, "Year")  
```  
  
## Related content

- [Expression uses in reports (Power BI Report Builder and service)](../expressions/expression-uses-reports-report-builder.md)   
- [Expression examples (Power BI Report Builder and service)](../expressions/report-builder-expression-examples.md)   
- [Data Types in Expressions &#40;Report Builder and SSRS&#41;](/sql/reporting-services/report-design/data-types-in-expressions-report-builder-and-ssrs)   
- [Expression Scope for Totals, Aggregates, and Built-in Collections &#40;Report Builder and SSRS&#41;](/sql/reporting-services/report-design/expression-scope-for-totals-aggregates-and-built-in-collections)  
  
