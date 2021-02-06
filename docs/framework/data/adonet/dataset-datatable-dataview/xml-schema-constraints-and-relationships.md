---
description: 了解更多： XML 架构约束和关系
title: XML 架构约束和关系
ms.date: 03/30/2017
ms.assetid: 165bc2bc-60a1-40e0-9b89-7c68ef979079
ms.openlocfilehash: c7847691537c4b754abcbacdeb367b1d92365ef3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99651309"
---
# <a name="xml-schema-constraints-and-relationships"></a><span data-ttu-id="c56b4-103">XML 架构约束和关系</span><span class="sxs-lookup"><span data-stu-id="c56b4-103">XML Schema Constraints and Relationships</span></span>

<span data-ttu-id="c56b4-104">在 (XSD) 架构的 XML 架构定义语言中，可以使用 **msdata： Relationship** 批注 (指定 (unique、key 和 keyref 约束) 和关系的约束。</span><span class="sxs-lookup"><span data-stu-id="c56b4-104">In an XML Schema definition language (XSD) schema, you can specify constraints (unique, key, and keyref constraints) and relationships (using the **msdata:Relationship** annotation).</span></span> <span data-ttu-id="c56b4-105">本主题说明如何解释在 XML 架构中指定的约束和关系，以生成 <xref:System.Data.DataSet>。</span><span class="sxs-lookup"><span data-stu-id="c56b4-105">This topic explains how the constraints and relationships specified in an XML Schema are interpreted to generate the <xref:System.Data.DataSet>.</span></span>  
  
 <span data-ttu-id="c56b4-106">通常，在 XML 架构中，如果只想在 **DataSet** 中生成关系，则可指定 **msdata： Relationship** 批注。</span><span class="sxs-lookup"><span data-stu-id="c56b4-106">In general, in an XML Schema, you specify the **msdata:Relationship** annotation if you want to generate only relationships in the **DataSet**.</span></span> <span data-ttu-id="c56b4-107">有关详细信息，请参阅 [从 XML 架构生成数据集关系 (XSD) ](generating-dataset-relations-from-xml-schema-xsd.md)。</span><span class="sxs-lookup"><span data-stu-id="c56b4-107">For more information, see [Generating DataSet Relations from XML Schema (XSD)](generating-dataset-relations-from-xml-schema-xsd.md).</span></span> <span data-ttu-id="c56b4-108">如果要在 **DataSet** 中生成约束，请 (unique、key 和 keyref) 指定约束。</span><span class="sxs-lookup"><span data-stu-id="c56b4-108">You specify constraints (unique, key, and keyref) if you want to generate constraints in the **DataSet**.</span></span> <span data-ttu-id="c56b4-109">请注意，如本主题稍后所述，键和 keyref 约束也可用于生成关系。</span><span class="sxs-lookup"><span data-stu-id="c56b4-109">Note that the key and keyref constraints are also used to generate relationships, as explained later in this topic.</span></span>  
  
## <a name="generating-a-relationship-from-key-and-keyref-constraints"></a><span data-ttu-id="c56b4-110">从键和 keyref 约束生成关系</span><span class="sxs-lookup"><span data-stu-id="c56b4-110">Generating a Relationship from key and keyref Constraints</span></span>  

 <span data-ttu-id="c56b4-111">您可以不指定 **msdata： Relationship** 批注，而是指定在 XML 架构映射过程中使用的键和 keyref 约束，以便不仅生成约束，还生成 **数据集中** 的关系。</span><span class="sxs-lookup"><span data-stu-id="c56b4-111">Instead of specifying the **msdata:Relationship** annotation, you can specify key and keyref constraints, which are used during the XML Schema mapping process to generate not only the constraints but also the relationship in the **DataSet**.</span></span> <span data-ttu-id="c56b4-112">但是，如果 `msdata:ConstraintOnly="true"` 在 **keyref** 元素中指定，则 **数据集会** 只包含约束，而不包括关系。</span><span class="sxs-lookup"><span data-stu-id="c56b4-112">However, if you specify `msdata:ConstraintOnly="true"` in the **keyref** element, the **DataSet** will include only the constraints and will not include the relationship.</span></span>  
  
 <span data-ttu-id="c56b4-113">下面的示例显示一个 XML 架构，该架构包含不嵌套的 **Order** 和 **OrderDetail** 元素。</span><span class="sxs-lookup"><span data-stu-id="c56b4-113">The following example shows an XML Schema that includes **Order** and **OrderDetail** elements, which are not nested.</span></span> <span data-ttu-id="c56b4-114">该架构还指定键约束和 keyref 约束。</span><span class="sxs-lookup"><span data-stu-id="c56b4-114">The schema also specifies key and keyref constraints.</span></span>  
  
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
           <xs:element name="OrderNo" type="xs:integer" />  
           <xs:element name="ItemNo" type="xs:string" />  
         </xs:sequence>  
       </xs:complexType>  
      </xs:element>  
      <xs:element name="Order">  
        <xs:complexType>  
          <xs:sequence>  
            <xs:element name="OrderNumber" type="xs:integer" />  
            <xs:element name="EmpNumber" type="xs:integer" />  
          </xs:sequence>  
        </xs:complexType>  
      </xs:element>  
    </xs:choice>  
  </xs:complexType>  
  
  <xs:key name="OrderNumberKey"  >  
    <xs:selector xpath=".//Order" />  
    <xs:field xpath="OrderNumber" />  
  </xs:key>  
  
  <xs:keyref name="OrderNoRef" refer="OrderNumberKey">  
    <xs:selector xpath=".//OrderDetail" />  
    <xs:field xpath="OrderNo" />  
  </xs:keyref>  
 </xs:element>  
</xs:schema>  
```  
  
 <span data-ttu-id="c56b4-115">在 XML 架构映射过程中生成的 **数据集** 包含 **Order** 和 **OrderDetail** 表。</span><span class="sxs-lookup"><span data-stu-id="c56b4-115">The **DataSet** that is generated during the XML Schema mapping process includes the **Order** and **OrderDetail** tables.</span></span> <span data-ttu-id="c56b4-116">此外， **数据集** 还包括关系和约束。</span><span class="sxs-lookup"><span data-stu-id="c56b4-116">In addition, the **DataSet** includes relationships and constraints.</span></span> <span data-ttu-id="c56b4-117">以下示例将显示这些关系和约束。</span><span class="sxs-lookup"><span data-stu-id="c56b4-117">The following example shows these relationships and constraints.</span></span> <span data-ttu-id="c56b4-118">请注意，架构未指定 **msdata： Relationship** 批注;相反，键和 keyref 约束用于生成关系。</span><span class="sxs-lookup"><span data-stu-id="c56b4-118">Note that the schema does not specify the **msdata:Relationship** annotation; instead, the key and keyref constraints are used to generate the relation.</span></span>  
  
```text
....ConstraintName: OrderNumberKey  
....Type: UniqueConstraint  
....Table: Order  
....Columns: OrderNumber  
....IsPrimaryKey: False  
  
....ConstraintName: OrderNoRef  
....Type: ForeignKeyConstraint  
....Table: OrderDetail  
....Columns: OrderNo  
....RelatedTable: Order  
....RelatedColumns: OrderNumber  
  
..RelationName: OrderNoRef  
..ParentTable: Order  
..ParentColumns: OrderNumber  
..ChildTable: OrderDetail  
..ChildColumns: OrderNo  
..ParentKeyConstraint: OrderNumberKey  
..ChildKeyConstraint: OrderNoRef  
..Nested: False  
```  
  
 <span data-ttu-id="c56b4-119">在上面的架构示例中， **Order** 和 **OrderDetail** 元素不嵌套。</span><span class="sxs-lookup"><span data-stu-id="c56b4-119">In the previous schema example, the **Order** and **OrderDetail** elements are not nested.</span></span> <span data-ttu-id="c56b4-120">在以下架构示例中，这些元素嵌套。</span><span class="sxs-lookup"><span data-stu-id="c56b4-120">In the following schema example, these elements are nested.</span></span> <span data-ttu-id="c56b4-121">但未指定 **msdata： Relationship** 批注;因此，假定使用隐式关系。</span><span class="sxs-lookup"><span data-stu-id="c56b4-121">However, no **msdata:Relationship** annotation is specified; therefore, an implicit relation is assumed.</span></span> <span data-ttu-id="c56b4-122">有关详细信息，请参阅 [映射嵌套架构元素之间的隐式关系](map-implicit-relations-between-nested-schema-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="c56b4-122">For more information, see [Map Implicit Relations Between Nested Schema Elements](map-implicit-relations-between-nested-schema-elements.md).</span></span> <span data-ttu-id="c56b4-123">该架构还指定键约束和 keyref 约束。</span><span class="sxs-lookup"><span data-stu-id="c56b4-123">The schema also specifies key and keyref constraints.</span></span>  
  
```xml  
<xs:schema id="MyDataSet" xmlns=""
            xmlns:xs="http://www.w3.org/2001/XMLSchema"
            xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
  
 <xs:element name="MyDataSet" msdata:IsDataSet="true">  
  <xs:complexType>  
    <xs:choice maxOccurs="unbounded">  
  
      <xs:element name="Order">  
        <xs:complexType>  
          <xs:sequence>  
            <xs:element name="OrderNumber" type="xs:integer" />  
            <xs:element name="EmpNumber" type="xs:integer" />  
  
            <xs:element name="OrderDetail">  
              <xs:complexType>  
                <xs:sequence>  
                  <xs:element name="OrderNo" type="xs:integer" />  
                  <xs:element name="ItemNo" type="xs:string" />  
                </xs:sequence>  
              </xs:complexType>  
            </xs:element>  
          </xs:sequence>  
        </xs:complexType>  
      </xs:element>  
    </xs:choice>  
  </xs:complexType>  
  
  <xs:key name="OrderNumberKey"  >  
    <xs:selector xpath=".//Order" />  
    <xs:field xpath="OrderNumber" />  
  </xs:key>  
  
  <xs:keyref name="OrderNoRef" refer="OrderNumberKey">  
    <xs:selector xpath=".//OrderDetail" />  
    <xs:field xpath="OrderNo" />  
  </xs:keyref>  
 </xs:element>  
</xs:schema>  
```  
  
 <span data-ttu-id="c56b4-124">XML 架构映射过程中生成的 **数据集** 包括两个表：</span><span class="sxs-lookup"><span data-stu-id="c56b4-124">The **DataSet** resulting from the XML Schema mapping process includes two tables:</span></span>  
  
```text  
Order(OrderNumber, EmpNumber, Order_Id)  
OrderDetail(OrderNumber, ItemNumber, Order_Id)  
```  
  
 <span data-ttu-id="c56b4-125">**数据集** 还包括两个关系 (一个基于 **msdata： relationship** 批注，另一个基于键和 keyref 约束) 和各种约束。</span><span class="sxs-lookup"><span data-stu-id="c56b4-125">The **DataSet** also includes the two relationships (one based on the **msdata:relationship** annotation and the other based on the key and keyref constraints) and various constraints.</span></span> <span data-ttu-id="c56b4-126">以下示例将显示这些关系和约束。</span><span class="sxs-lookup"><span data-stu-id="c56b4-126">The following example shows the relations and constraints.</span></span>  
  
```text
..RelationName: Order_OrderDetail  
..ParentTable: Order  
..ParentColumns: Order_Id  
..ChildTable: OrderDetail  
..ChildColumns: Order_Id  
..ParentKeyConstraint: Constraint1  
..ChildKeyConstraint: Order_OrderDetail  
..Nested: True  
  
..RelationName: OrderNoRef  
..ParentTable: Order  
..ParentColumns: OrderNumber  
..ChildTable: OrderDetail  
..ChildColumns: OrderNo  
..ParentKeyConstraint: OrderNumberKey  
..ChildKeyConstraint: OrderNoRef  
..Nested: False  
  
..ConstraintName: OrderNumberKey  
..Type: UniqueConstraint  
..Table: Order  
..Columns: OrderNumber  
..IsPrimaryKey: False  
  
..ConstraintName: Constraint1  
..Type: UniqueConstraint  
..Table: Order  
..Columns: Order_Id  
..IsPrimaryKey: True  
  
..ConstraintName: Order_OrderDetail  
..Type: ForeignKeyConstraint  
..Table: OrderDetail  
..Columns: Order_Id  
..RelatedTable: Order  
..RelatedColumns: Order_Id  
  
..ConstraintName: OrderNoRef  
..Type: ForeignKeyConstraint  
..Table: OrderDetail  
..Columns: OrderNo  
..RelatedTable: Order  
..RelatedColumns: OrderNumber  
```  
  
 <span data-ttu-id="c56b4-127">如果引用嵌套表的 keyref 约束包含 **msdata： IsNested = "true"** 批注，则该 **数据集** 将创建基于 keyref 约束的单个嵌套关系以及相关的 unique/key 约束。</span><span class="sxs-lookup"><span data-stu-id="c56b4-127">If a keyref constraint referring to a nested table contains the **msdata:IsNested="true"** annotation, the **DataSet** will create a single nested relationship that is based on the keyref constraint and the related unique/key constraint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c56b4-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="c56b4-128">See also</span></span>

- [<span data-ttu-id="c56b4-129">从 XML 架构派生数据集关系结构 (XSD)</span><span class="sxs-lookup"><span data-stu-id="c56b4-129">Deriving DataSet Relational Structure from XML Schema (XSD)</span></span>](deriving-dataset-relational-structure-from-xml-schema-xsd.md)
- [<span data-ttu-id="c56b4-130">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="c56b4-130">ADO.NET Overview</span></span>](../ado-net-overview.md)
