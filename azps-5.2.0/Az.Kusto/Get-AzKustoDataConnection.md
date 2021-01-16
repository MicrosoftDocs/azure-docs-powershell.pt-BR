---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 6cfc5cdae87512245a573ed5c7ff9c746036c815
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260928"
---
# <span data-ttu-id="c791b-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="c791b-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="c791b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c791b-102">SYNOPSIS</span></span>
<span data-ttu-id="c791b-103">Retorna uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="c791b-103">Returns a data connection.</span></span>

## <span data-ttu-id="c791b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c791b-104">SYNTAX</span></span>

### <span data-ttu-id="c791b-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="c791b-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c791b-106">Obter</span><span class="sxs-lookup"><span data-stu-id="c791b-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c791b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c791b-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c791b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c791b-108">DESCRIPTION</span></span>
<span data-ttu-id="c791b-109">Retorna uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="c791b-109">Returns a data connection.</span></span>

## <span data-ttu-id="c791b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c791b-110">EXAMPLES</span></span>

### <span data-ttu-id="c791b-111">Exemplo 1: listar todas as conexões de dados em um banco de dados específico</span><span class="sxs-lookup"><span data-stu-id="c791b-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="c791b-112">O comando acima retorna todos os bancos de dados do Kusto no cluster "testnewkustocluster" localizado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="c791b-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="c791b-113">Exemplo 2: obter uma conexão de dados específica por nome</span><span class="sxs-lookup"><span data-stu-id="c791b-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="c791b-114">O comando acima retorna a conexão de dados chamada "mykustodataconnection" no banco de dados "mykustodatabase" do cluster existente "testnewkustocluster" encontrada no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="c791b-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="c791b-115">OS</span><span class="sxs-lookup"><span data-stu-id="c791b-115">PARAMETERS</span></span>

### <span data-ttu-id="c791b-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c791b-116">-ClusterName</span></span>
<span data-ttu-id="c791b-117">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c791b-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c791b-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c791b-118">-DatabaseName</span></span>
<span data-ttu-id="c791b-119">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c791b-119">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c791b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c791b-120">-DefaultProfile</span></span>
<span data-ttu-id="c791b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c791b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c791b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c791b-122">-InputObject</span></span>
<span data-ttu-id="c791b-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c791b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c791b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c791b-124">-Name</span></span>
<span data-ttu-id="c791b-125">O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="c791b-125">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c791b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c791b-126">-ResourceGroupName</span></span>
<span data-ttu-id="c791b-127">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c791b-127">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c791b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c791b-128">-SubscriptionId</span></span>
<span data-ttu-id="c791b-129">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c791b-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c791b-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c791b-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c791b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c791b-131">CommonParameters</span></span>
<span data-ttu-id="c791b-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c791b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c791b-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c791b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c791b-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c791b-134">INPUTS</span></span>

### <span data-ttu-id="c791b-135">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="c791b-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="c791b-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c791b-136">OUTPUTS</span></span>

### <span data-ttu-id="c791b-137">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="c791b-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="c791b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c791b-138">NOTES</span></span>

<span data-ttu-id="c791b-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c791b-139">ALIASES</span></span>

<span data-ttu-id="c791b-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c791b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c791b-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c791b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c791b-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c791b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c791b-143">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c791b-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c791b-144">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="c791b-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="c791b-145">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c791b-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="c791b-146">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="c791b-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="c791b-147">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c791b-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="c791b-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c791b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c791b-149">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="c791b-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="c791b-150">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="c791b-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="c791b-151">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c791b-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="c791b-152">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c791b-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c791b-153">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c791b-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c791b-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c791b-154">RELATED LINKS</span></span>

