---
title: "Avg function in a Power BI paginated report"
description: Learn about the Avg function in Power BI paginated reports. It returns the average of all non-null numeric values specified by the expression in Report Builder.
author: maggiesMSFT
ms.author: maggies
ms.date: 04/28/2023
ms.service: powerbi
ms.subservice: report-builder
ms.topic: conceptual
ms.custom: updatefrequency5
ms.reviewer: spendrick
---
# Avg function in a Power BI paginated report

[!INCLUDE [applies-yes-report-builder-no-desktop](../../includes/applies-yes-report-builder-no-desktop.md)]

In Power BI paginated reports, the Avg function returns the average of all non-null numeric values specified by the expression, evaluated in the given scope.  
  
## Syntax  
  
```  
  
Avg(expression, scope, recursive)  
```  
  
### Parameters  
 *expression*  
 (**Float**) The expression on which to perform the aggregation.  
  
 *scope*  
 (**String**) Optional. The name of a dataset, group, or data region that contains the report items to which to apply the aggregate function. If *scope* isn't specified, the current scope is used.  
  
 *recursive*  
 (**Enumerated Type**) Optional. **Simple** (default) or **RdlRecursive**. Specifies whether to perform the aggregation recursively.  
  
## Return type  
 Returns a **Decimal** for decimal expressions and a **Double** for all other expressions.  
  
## Remarks  
 The set of data specified in the expression must have the same data type. To convert data that has multiple numeric data types to the same data type, use conversion functions like **CInt**, **CDbl** or **CDec**. For more information, see [Type Conversion Functions](/dotnet/visual-basic/language-reference/functions/type-conversion-functions).  
  
 The value of *scope* must be a string constant and can't be an expression. For outer aggregates or aggregates that don't specify other aggregates, *scope* must refer to the current scope or a containing scope. For aggregates of aggregates, nested aggregates can specify a child scope.  
  
 *Expression* can contain calls to nested aggregate functions with the following exceptions and conditions:  
  
-   *Scope* for nested aggregates must be the same as, or contained by, the scope of the outer aggregate. For all distinct scopes in the expression, one scope must be in a child relationship to all other scopes.  
  
-   *Scope* for nested aggregates can't be the name of a dataset.  
  
-   *Expression* must not contain **First**, **Last**, **Previous**, or **RunningValue** functions.  
  
-   *Expression* must not contain nested aggregates that specify *recursive*.  
  
 For more information, see [Aggregate Functions Reference &#40;Report Builder)](/sql/reporting-services/report-design/report-builder-functions-aggregate-functions-reference) and [Expression Scope for Totals, Aggregates, and Built-in Collections &#40;Report Builder)](/sql/reporting-services/report-design/expression-scope-for-totals-aggregates-and-built-in-collections).  
  
 For more information about recursive aggregates, see [Creating Recursive Hierarchy Groups &#40;Report Builder)](/sql/reporting-services/report-design/creating-recursive-hierarchy-groups-report-builder-and-ssrs).  
  
## Example  
 The following two code examples provide an average of all values in the `Cost` field contained in a dataset named `Inventory`.  
  
```  
=Avg(Fields!Cost.Value, "Inventory")   
  OR    
=Avg (CDbl(Fields!Cost.Value), "Inventory")  
```  
  
## Related content

- [Expression uses in reports (Power BI Report Builder and service)](../expressions/expression-uses-reports-report-builder.md)   
- [Expression examples (Power BI Report Builder and service)](../expressions/report-builder-expression-examples.md)   
- [Data Types in Expressions &#40;Report Builder)](/sql/reporting-services/report-design/data-types-in-expressions-report-builder-and-ssrs)   
- [Expression Scope for Totals, Aggregates, and Built-in Collections &#40;Report Builder)](/sql/reporting-services/report-design/expression-scope-for-totals-aggregates-and-built-in-collections)  
  
