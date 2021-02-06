---
description: 了解详细信息：指定没有嵌套的元素之间的关系
title: 指定无嵌套的元素之间的关系
ms.date: 03/30/2017
ms.assetid: e31325da-7691-4d33-acf4-99fccca67006
ms.openlocfilehash: 68f6edad0c282091529bf9182f5161d0808a47aa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99651621"
---
# <a name="specify-relations-between-elements-with-no-nesting"></a>指定无嵌套的元素之间的关系

当元素不嵌套时，将不创建任何隐式关系。 但是，可以使用 **msdata： Relationship** 批注显式指定未嵌套的元素之间的关系。  
  
 下面的示例显示一个 XML 架构，该架构在不嵌套的 **Order** 和 **OrderDetail** 元素之间指定 **msdata： Relationship** 批注。 **Msdata： Relationship** 批注指定为 **Schema** 元素的子元素。  
  
```xml  
<xs:schema id="MyDataSet" xmlns=""
             xmlns:xs="http://www.w3.org/2001/XMLSchema"
             xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
 <xs:element name="MyDataSet" msdata:IsDataSet="true">  
  <xs:complexType>  
    <xs:choice maxOccurs="unbounded">  
      <xs:element name="OrderDetail">  
       <xs:complexType>  
         <xs:sequence>  
           <xs:element name="OrderNo" type="xs:string" />  
           <xs:element name="ItemNo" type="xs:string" />  
         </xs:sequence>  
       </xs:complexType>  
      </xs:element>  
      <xs:element name="Order">  
       <xs:complexType>  
         <xs:sequence>  
           <xs:element name="OrderNumber" type="xs:string" />  
           <xs:element name="EmpNumber" type="xs:string" />  
         </xs:sequence>  
       </xs:complexType>  
      </xs:element>  
    </xs:choice>  
  </xs:complexType>  
  
  </xs:element>  
   <xs:annotation>  
     <xs:appinfo>  
       <msdata:Relationship name="OrdOrderDetailRelation"  
                            msdata:parent="Order"
                            msdata:child="OrderDetail"
                            msdata:parentkey="OrderNumber"
                            msdata:childkey="OrderNo"/>  
     </xs:appinfo>  
  </xs:annotation>  
</xs:schema>  
```  
  
 XML 架构定义语言 (XSD) 架构映射过程创建一个 <xref:System.Data.DataSet> With **Order** 和 **OrderDetail** 表以及这两个表之间指定的关系，如下所示。  
  
```text  
RelationName: OrdOrderDetailRelation  
ParentTable: Order  
ParentColumns: OrderNumber
ChildTable: OrderDetail  
ChildColumns: OrderNo
Nested: False  
```  
  
## <a name="see-also"></a>请参阅

- [从 XML 架构生成数据集关系 (XSD)](generating-dataset-relations-from-xml-schema-xsd.md)
- [将关键 XML 架构 (XSD) 约束映射到数据集约束](mapping-xml-schema-xsd-constraints-to-dataset-constraints.md)
- [ADO.NET 概述](../ado-net-overview.md)
