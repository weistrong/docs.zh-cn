---
description: 了解详细信息：使用 XML web services 中的数据集
title: 使用 XML Web Services 中的数据集
ms.date: 07/14/2020
dev_langs:
- csharp
- vb
ms.assetid: 9edd6b71-0fa5-4649-ae1d-ac1c12541019
ms.openlocfilehash: 3c9112d259d5a6450a968ba87b33c4072f6dc44c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725124"
---
# <a name="consume-a-dataset-from-an-xml-web-service"></a><span data-ttu-id="eeb7f-103">使用 XML web services 中的数据集</span><span class="sxs-lookup"><span data-stu-id="eeb7f-103">Consume a DataSet from an XML web service</span></span>

<span data-ttu-id="eeb7f-104"><xref:System.Data.DataSet> 是用断开式设计来构建的，其部分目的是为了便于通过 Internet 来传输数据。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-104">The <xref:System.Data.DataSet> was architected with a disconnected design, in part to facilitate the convenient transport of data over the Internet.</span></span> <span data-ttu-id="eeb7f-105">**数据集** 是可序列化的，因为可以将其指定为 XML Web services 的输入或从 XML Web services 输出，而无需进行任何其他编码即可将 **数据集** 的内容从 XML Web service 流式传输到客户端和返回到客户端。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-105">The **DataSet** is "serializable" in that it can be specified as an input to or output from XML Web services without any additional coding required to stream the contents of the **DataSet** from an XML Web service to a client and back.</span></span> <span data-ttu-id="eeb7f-106">**数据集** 使用 DiffGram 格式隐式转换为 XML 流，并通过网络发送，然后作为接收端上的 **数据集** 从 xml 流重新构造。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-106">The **DataSet** is implicitly converted to an XML stream using the DiffGram format, sent over the network, and then reconstructed from the XML stream as a **DataSet** on the receiving end.</span></span> <span data-ttu-id="eeb7f-107">这为你提供了一种简单而灵活的方法，用于通过 XML Web services 传输和返回关系数据。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-107">This gives you a simple and flexible method for transmitting and returning relational data using XML Web services.</span></span> <span data-ttu-id="eeb7f-108">有关 DiffGram 格式的详细信息，请参阅 [diffgram](diffgrams.md)。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-108">For more information about the DiffGram format, see [DiffGrams](diffgrams.md).</span></span>  
  
 <span data-ttu-id="eeb7f-109">下面的示例演示如何创建使用 **数据集** 传输关系数据的 XML Web service 和客户端 (包括已修改的数据) 并将所有更新解析回原始数据源。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-109">The following example shows how to create an XML Web service and client that use the **DataSet** to transport relational data (including modified data) and resolve any updates back to the original data source.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="eeb7f-110">`DataSet` `DataTable` 如果输入不受信任，则作为 XML Web service 调用的一部分传输或实例是不安全的。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-110">Transmitting `DataSet` or `DataTable` instances as part of XML Web service calls is not safe if the input is not trusted.</span></span> <span data-ttu-id="eeb7f-111">有关详细信息，请参阅 [数据集和 DataTable 安全指南](security-guidance.md)。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-111">For more information, see [DataSet and DataTable security guidance](security-guidance.md).</span></span>
> <span data-ttu-id="eeb7f-112">我们还建议你在创建 XML Web service 时始终考虑安全问题。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-112">We also recommend that you always consider security implications when creating an XML Web service.</span></span> <span data-ttu-id="eeb7f-113">有关保护 XML Web service 的信息，请参阅 [保护使用 ASP.NET 创建的 XML Web Services](/previous-versions/dotnet/netframework-4.0/w67h0dw7(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-113">For information on securing an XML Web service, see [Securing XML Web Services Created Using ASP.NET](/previous-versions/dotnet/netframework-4.0/w67h0dw7(v=vs.100)).</span></span>  
  
## <a name="create-an-xml-web-service"></a><span data-ttu-id="eeb7f-114">创建 XML web services</span><span class="sxs-lookup"><span data-stu-id="eeb7f-114">Create an XML web service</span></span>
  
1. <span data-ttu-id="eeb7f-115">创建 XML Web services。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-115">Create the XML Web service.</span></span>  
  
     <span data-ttu-id="eeb7f-116">在此示例中，创建了一个用于返回数据的 XML Web service，在本例中为 **Northwind** 数据库中的客户列表，接收到数据的更新的数据 **集** ，XML Web service 解析回原始数据源。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-116">In the example, an XML Web service is created that returns data, in this case a list of customers from the **Northwind** database, and receives a **DataSet** with updates to the data, which the XML Web service resolves back to the original data source.</span></span>  
  
     <span data-ttu-id="eeb7f-117">XML Web service 公开两个方法： **GetCustomers**，用于返回客户列表和 **UpdateCustomers**，以将更新解析回数据源。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-117">The XML Web service exposes two methods: **GetCustomers**, to return the list of customers, and **UpdateCustomers**, to resolve updates back to the data source.</span></span> <span data-ttu-id="eeb7f-118">XML Web services 存储在 Web 服务器上名为 DataSetSample.asmx 的文件中。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-118">The XML Web service is stored in a file on the Web server called DataSetSample.asmx.</span></span> <span data-ttu-id="eeb7f-119">下面的代码概括了 DataSetSample.asmx 的内容。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-119">The following code outlines the contents of DataSetSample.asmx.</span></span>  
  
    ```vb  
    <% @ WebService Language = "vb" Class = "Sample" %>  
    Imports System  
    Imports System.Data  
    Imports System.Data.SqlClient  
    Imports System.Web.Services  
  
    <WebService(Namespace:="http://microsoft.com/webservices/")> _  
    Public Class Sample  
  
    Public connection As SqlConnection = New SqlConnection("Data Source=(local);Integrated Security=SSPI;Initial Catalog=Northwind")  
  
      <WebMethod( Description := "Returns Northwind Customers", EnableSession := False )> _  
      Public Function GetCustomers() As DataSet  
        Dim adapter As SqlDataAdapter = New SqlDataAdapter( _  
          "SELECT CustomerID, CompanyName FROM Customers", connection)  
  
        Dim custDS As DataSet = New DataSet()  
        adapter.MissingSchemaAction = MissingSchemaAction.AddWithKey  
        adapter.Fill(custDS, "Customers")  
  
        Return custDS  
      End Function  
  
      <WebMethod( Description := "Updates Northwind Customers", EnableSession := False )> _  
      Public Function UpdateCustomers(custDS As DataSet) As DataSet  
        Dim adapter As SqlDataAdapter = New SqlDataAdapter()  
  
        adapter.InsertCommand = New SqlCommand( _  
          "INSERT INTO Customers (CustomerID, CompanyName) " & _  
          "Values(@CustomerID, @CompanyName)", connection)  
        adapter.InsertCommand.Parameters.Add( _  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID")  
        adapter.InsertCommand.Parameters.Add( _  
          "@CompanyName", SqlDbType.NChar, 15, "CompanyName")  
  
        adapter.UpdateCommand = New SqlCommand( _  
          "UPDATE Customers Set CustomerID = @CustomerID, " & _  
          "CompanyName = @CompanyName WHERE CustomerID = " & _  
          @OldCustomerID", connection)  
        adapter.UpdateCommand.Parameters.Add( _  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID")  
        adapter.UpdateCommand.Parameters.Add( _  
          "@CompanyName", SqlDbType.NChar, 15, "CompanyName")  
  
        Dim parameter As SqlParameter = _  
          adapter.UpdateCommand.Parameters.Add( _  
          "@OldCustomerID", SqlDbType.NChar, 5, "CustomerID")  
        parameter.SourceVersion = DataRowVersion.Original  
  
        adapter.DeleteCommand = New SqlCommand( _  
          "DELETE FROM Customers WHERE CustomerID = @CustomerID", _  
          connection)  
        parameter = adapter.DeleteCommand.Parameters.Add( _  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID")  
        parameter.SourceVersion = DataRowVersion.Original  
  
        adapter.Update(custDS, "Customers")  
  
        Return custDS  
      End Function  
    End Class  
    ```  
  
    ```csharp  
    <% @ WebService Language = "C#" Class = "Sample" %>  
    using System;  
    using System.Data;  
    using System.Data.SqlClient;  
    using System.Web.Services;  
  
    [WebService(Namespace="http://microsoft.com/webservices/")]  
    public class Sample  
    {  
      public SqlConnection connection = new SqlConnection("Data Source=(local);Integrated Security=SSPI;Initial Catalog=Northwind");  
  
      [WebMethod( Description = "Returns Northwind Customers", EnableSession = false )]  
      public DataSet GetCustomers()  
      {  
        SqlDataAdapter adapter = new SqlDataAdapter(  
          "SELECT CustomerID, CompanyName FROM Customers", connection);  
  
        DataSet custDS = new DataSet();  
        adapter.MissingSchemaAction = MissingSchemaAction.AddWithKey;  
        adapter.Fill(custDS, "Customers");  
  
        return custDS;  
      }  
  
      [WebMethod( Description = "Updates Northwind Customers",  
        EnableSession = false )]  
      public DataSet UpdateCustomers(DataSet custDS)  
      {  
        SqlDataAdapter adapter = new SqlDataAdapter();  
  
        adapter.InsertCommand = new SqlCommand(  
          "INSERT INTO Customers (CustomerID, CompanyName) " +  
          "Values(@CustomerID, @CompanyName)", connection);  
        adapter.InsertCommand.Parameters.Add(  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID");  
        adapter.InsertCommand.Parameters.Add(  
          "@CompanyName", SqlDbType.NChar, 15, "CompanyName");  
  
        adapter.UpdateCommand = new SqlCommand(  
          "UPDATE Customers Set CustomerID = @CustomerID, " +  
          "CompanyName = @CompanyName WHERE CustomerID = " +  
          "@OldCustomerID", connection);  
        adapter.UpdateCommand.Parameters.Add(  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID");  
        adapter.UpdateCommand.Parameters.Add(  
          "@CompanyName", SqlDbType.NChar, 15, "CompanyName");  
        SqlParameter parameter = adapter.UpdateCommand.Parameters.Add(  
          "@OldCustomerID", SqlDbType.NChar, 5, "CustomerID");  
        parameter.SourceVersion = DataRowVersion.Original;  
  
        adapter.DeleteCommand = new SqlCommand(  
        "DELETE FROM Customers WHERE CustomerID = @CustomerID",  
         connection);  
        parameter = adapter.DeleteCommand.Parameters.Add(  
          "@CustomerID", SqlDbType.NChar, 5, "CustomerID");  
        parameter.SourceVersion = DataRowVersion.Original;  
  
        adapter.Update(custDS, "Customers");  
  
        return custDS;  
      }  
    }  
    ```  
  
     <span data-ttu-id="eeb7f-120">在典型方案中，将编写 **UpdateCustomers** 方法来捕获开放式并发冲突。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-120">In a typical scenario, the **UpdateCustomers** method would be written to catch optimistic concurrency violations.</span></span> <span data-ttu-id="eeb7f-121">为了简单起见，以上示例没有包含此方法。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-121">For simplicity, the example does not include this.</span></span> <span data-ttu-id="eeb7f-122">有关开放式并发的详细信息，请参阅 [乐观并发](../optimistic-concurrency.md)。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-122">For more information about optimistic concurrency, see [Optimistic Concurrency](../optimistic-concurrency.md).</span></span>  
  
2. <span data-ttu-id="eeb7f-123">创建 XML Web services 代理。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-123">Create an XML Web service proxy.</span></span>  
  
     <span data-ttu-id="eeb7f-124">XML Web services 的客户端将需要通过 SOAP 代理来使用公开的方法。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-124">Clients of the XML Web service require a SOAP proxy in order to consume the exposed methods.</span></span> <span data-ttu-id="eeb7f-125">可以使用 Visual Studio 生成此代理。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-125">You can have Visual Studio generate this proxy for you.</span></span> <span data-ttu-id="eeb7f-126">通过从 Visual Studio 中设置对现有 Web 服务的 Web 引用，此步骤中所述的所有行为均将透明地发生。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-126">By setting a Web reference to an existing Web service from within Visual Studio, all the behavior described in this step occurs transparently.</span></span> <span data-ttu-id="eeb7f-127">如果要自己创建代理类，请继续阅读本讨论。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-127">If you want to create the proxy class yourself, continue with this discussion.</span></span> <span data-ttu-id="eeb7f-128">但是，在大多数情况下，使用 Visual Studio 足以为客户端应用程序创建代理类。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-128">In most circumstances, however, using Visual Studio to create the proxy class for the client application is sufficient.</span></span>  
  
     <span data-ttu-id="eeb7f-129">代理可以使用 Web 服务描述语言工具来创建。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-129">A proxy can be created using the Web Services Description Language Tool.</span></span> <span data-ttu-id="eeb7f-130">例如，如果在 URL 处公开了 XML Web service，则 `http://myserver/data/DataSetSample.asmx` 发出如下所示的命令，以 Visual Basic 创建一个 DSSample 命名空间为 **WebData** 的 .net 代理，并将其存储在文件中。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-130">For example, if the XML Web service is exposed at the URL `http://myserver/data/DataSetSample.asmx`, issue a command such as the following to create a Visual Basic .NET proxy with a namespace of **WebData.DSSample** and store it in the file sample.vb.</span></span>  
  
    ```console
    wsdl /l:VB -out:sample.vb http://myserver/data/DataSetSample.asmx /n:WebData.DSSample  
    ```  
  
     <span data-ttu-id="eeb7f-131">若要在文件 sample.cs 中创建一个 C# 代理，请发出以下命令。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-131">To create a C# proxy in the file sample.cs, issue the following command.</span></span>  
  
    ```console
    wsdl -l:CS -out:sample.cs http://myserver/data/DataSetSample.asmx -n:WebData.DSSample  
    ```  
  
     <span data-ttu-id="eeb7f-132">然后，可以将该代理编译为库并导入 XML Web services 客户端。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-132">The proxy can then be compiled as a library and imported into the XML Web service client.</span></span> <span data-ttu-id="eeb7f-133">若要将 sample.vb 中存储的 Visual Basic .NET 代理代码编译为 sample.dll，请发出以下命令。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-133">To compile the Visual Basic .NET proxy code stored in sample.vb as sample.dll, issue the following command.</span></span>  
  
    ```console  
    vbc -t:library -out:sample.dll sample.vb -r:System.dll -r:System.Web.Services.dll -r:System.Data.dll -r:System.Xml.dll  
    ```  
  
     <span data-ttu-id="eeb7f-134">若要将 sample.cs 中存储的 C# 代理代码编译为 sample.dll，请发出以下命令。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-134">To compile the C# proxy code stored in sample.cs as sample.dll, issue the following command.</span></span>  
  
    ```console
    csc -t:library -out:sample.dll sample.cs -r:System.dll -r:System.Web.Services.dll -r:System.Data.dll -r:System.Xml.dll  
    ```  
  
3. <span data-ttu-id="eeb7f-135">创建 XML Web services 客户端。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-135">Create an XML Web service client.</span></span>  
  
     <span data-ttu-id="eeb7f-136">如果想让 Visual Studio 为你生成 Web 服务代理类，只需创建客户端项目，然后在 "解决方案资源管理器" 窗口中右键单击该项目，然后选择 "**添加**  >  **服务引用**"。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-136">If you want to have Visual Studio generate the Web service proxy class for you, simply create the client project, and, in the Solution Explorer window, right-click the project, and then select **Add** > **Service Reference**.</span></span> <span data-ttu-id="eeb7f-137">在 " **添加服务引用** " 对话框中，选择 " **高级**"，然后选择 " **添加 Web 引用**"。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-137">In the **Add Service Reference** dialog box, select **Advanced**, and then select **Add Web Reference**.</span></span> <span data-ttu-id="eeb7f-138">从可用 Web 服务的列表中选择 Web 服务 (如果 Web 服务在当前解决方案或当前计算机上不可用，则这可能需要提供 Web 服务终结点的地址) 。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-138">Select the Web service from the list of available Web services (this may require supplying the address of the Web service endpoint if the Web service isn't available within the current solution or on the current computer).</span></span> <span data-ttu-id="eeb7f-139">如果自己创建 XML Web services 代理（按照前面的步骤所述），可以将其导入客户端代码并使用 XML Web services 方法。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-139">If you create the XML Web service proxy yourself (as described in the previous step), you can import it into your client code and consume the XML Web service methods.</span></span>

     <span data-ttu-id="eeb7f-140">下面的示例代码导入代理库，调用 **GetCustomers** 以获取客户列表，添加新客户，然后返回 **UpdateCustomers** 更新的 **数据集**。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-140">The following sample code imports the proxy library, calls **GetCustomers** to get a list of customers, adds a new customer, and then returns a **DataSet** with the updates to **UpdateCustomers**.</span></span>  
  
     <span data-ttu-id="eeb7f-141">该示例将 **GetChanges** 返回的 **数据集** 传递给 **UpdateCustomers** ，因为只有修改的行需要传递到 **UpdateCustomers**。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-141">The example passes the **DataSet** returned by **DataSet.GetChanges** to **UpdateCustomers** because only modified rows need to be passed to **UpdateCustomers**.</span></span> <span data-ttu-id="eeb7f-142">**UpdateCustomers** 返回已解析的 **数据集**，然后你可以将其 **合并** 到现有的 **数据集中** ，以合并来自更新的已解决更改和任何行错误信息。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-142">**UpdateCustomers** returns the resolved **DataSet**, which you can then **Merge** into the existing **DataSet** to incorporate the resolved changes and any row error information from the update.</span></span> <span data-ttu-id="eeb7f-143">以下代码假定你已使用 Visual Studio 创建 Web 引用，并且已在 " **添加 Web 引用** " 对话框中将 web 引用重命名为 "DsSample"。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-143">The following code assumes that you have used Visual Studio to create the Web reference, and that you have renamed the Web reference to DsSample in the **Add Web Reference** dialog box.</span></span>  
  
    ```vb  
    Imports System  
    Imports System.Data  
  
    Public Class Client  
  
      Public Shared Sub Main()  
        Dim proxySample As New DsSample.Sample ()  ' Proxy object.  
        Dim customersDataSet As DataSet = proxySample.GetCustomers()  
        Dim customersTable As DataTable = _  
          customersDataSet.Tables("Customers")  
  
        Dim rowAs DataRow = customersTable.NewRow()  
        row("CustomerID") = "ABCDE"  
        row("CompanyName") = "New Company Name"  
        customersTable.Rows.Add(row)  
  
        Dim updateDataSet As DataSet = _  
          proxySample.UpdateCustomers(customersDataSet.GetChanges())  
  
        customersDataSet.Merge(updateDataSet)  
        customersDataSet.AcceptChanges()  
      End Sub  
    End Class  
    ```  
  
    ```csharp  
    using System;  
    using System.Data;  
  
    public class Client  
    {  
      public static void Main()  
      {  
        Sample proxySample = new DsSample.Sample();  // Proxy object.  
        DataSet customersDataSet = proxySample.GetCustomers();  
        DataTable customersTable = customersDataSet.Tables["Customers"];  
  
        DataRow row = customersTable.NewRow();  
        row["CustomerID"] = "ABCDE";  
        row["CompanyName"] = "New Company Name";  
        customersTable.Rows.Add(row);  
  
        DataSet updateDataSet = new DataSet();  
  
        updateDataSet =
          proxySample.UpdateCustomers(customersDataSet.GetChanges());  
  
        customersDataSet.Merge(updateDataSet);  
        customersDataSet.AcceptChanges();  
      }  
    }  
    ```  
  
     <span data-ttu-id="eeb7f-144">如果决定自己创建代理类，必须执行下列额外的步骤。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-144">If you decide to create the proxy class yourself, you must take the following extra steps.</span></span> <span data-ttu-id="eeb7f-145">若要编译该示例，将需要提供已创建的代理库 (sample.dll) 和相关的 .NET 库。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-145">To compile the sample, supply the proxy library that was created (sample.dll) and the related .NET libraries.</span></span> <span data-ttu-id="eeb7f-146">若要编译该示例的 Visual Basic .NET 版本（存储在文件 client.vb 中），请发出以下命令。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-146">To compile the Visual Basic .NET version of the sample, stored in the file client.vb, issue the following command.</span></span>  
  
    ```console
    vbc client.vb -r:sample.dll -r:System.dll -r:System.Data.dll -r:System.Xml.dll -r:System.Web.Services.dll  
    ```  
  
     <span data-ttu-id="eeb7f-147">若要编译该示例的 C# 版本（存储在文件 client.cs 中），请发出以下命令。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-147">To compile the C# version of the sample, stored in the file client.cs, issue the following command.</span></span>  
  
    ```console
    csc client.cs -r:sample.dll -r:System.dll -r:System.Data.dll -r:System.Xml.dll -r:System.Web.Services.dll  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="eeb7f-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="eeb7f-148">See also</span></span>

- [<span data-ttu-id="eeb7f-149">ADO.NET</span><span class="sxs-lookup"><span data-stu-id="eeb7f-149">ADO.NET</span></span>](../index.md)
- [<span data-ttu-id="eeb7f-150">数据集、数据表和数据视图</span><span class="sxs-lookup"><span data-stu-id="eeb7f-150">DataSets, DataTables, and DataViews</span></span>](index.md)
- [<span data-ttu-id="eeb7f-151">DataTables</span><span class="sxs-lookup"><span data-stu-id="eeb7f-151">DataTables</span></span>](datatables.md)
- [<span data-ttu-id="eeb7f-152">从 DataAdapter 填充数据集</span><span class="sxs-lookup"><span data-stu-id="eeb7f-152">Populating a DataSet from a DataAdapter</span></span>](../populating-a-dataset-from-a-dataadapter.md)
- [<span data-ttu-id="eeb7f-153">使用 DataAdapter 更新数据源</span><span class="sxs-lookup"><span data-stu-id="eeb7f-153">Updating Data Sources with DataAdapters</span></span>](../updating-data-sources-with-dataadapters.md)
- [<span data-ttu-id="eeb7f-154">DataAdapter 参数</span><span class="sxs-lookup"><span data-stu-id="eeb7f-154">DataAdapter Parameters</span></span>](../dataadapter-parameters.md)
- <span data-ttu-id="eeb7f-155">[Web 服务描述语言工具 ( # A0) ](/previous-versions/dotnet/netframework-4.0/7h3ystb6(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="eeb7f-155">[Web Services Description Language Tool (Wsdl.exe)](/previous-versions/dotnet/netframework-4.0/7h3ystb6(v=vs.100))</span></span>
- [<span data-ttu-id="eeb7f-156">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="eeb7f-156">ADO.NET Overview</span></span>](../ado-net-overview.md)
