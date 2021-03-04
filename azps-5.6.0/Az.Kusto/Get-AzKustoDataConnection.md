---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 06c824c140f18c81ca3ce1547257e4765a2543b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886941"
---
# <span data-ttu-id="ef1df-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="ef1df-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="ef1df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef1df-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1df-103">Retorna uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="ef1df-103">Returns a data connection.</span></span>

## <span data-ttu-id="ef1df-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ef1df-104">SYNTAX</span></span>

### <span data-ttu-id="ef1df-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ef1df-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ef1df-106">Obter</span><span class="sxs-lookup"><span data-stu-id="ef1df-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ef1df-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ef1df-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ef1df-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ef1df-108">DESCRIPTION</span></span>
<span data-ttu-id="ef1df-109">Retorna uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="ef1df-109">Returns a data connection.</span></span>

## <span data-ttu-id="ef1df-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef1df-110">EXAMPLES</span></span>

### <span data-ttu-id="ef1df-111">Exemplo 1: listar todas as conexões de dados em um banco de dados específico</span><span class="sxs-lookup"><span data-stu-id="ef1df-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="ef1df-112">O comando acima retorna todos os bancos de dados kusto no cluster "testnewkustocluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="ef1df-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ef1df-113">Exemplo 2: Obter uma conexão de dados específica pelo nome</span><span class="sxs-lookup"><span data-stu-id="ef1df-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="ef1df-114">O comando acima retorna a conexão de dados chamada "mykustodataconnection" no banco de dados "mykustodatabase" do cluster existente "testnewkustocluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="ef1df-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="ef1df-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ef1df-115">PARAMETERS</span></span>

### <span data-ttu-id="ef1df-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ef1df-116">-ClusterName</span></span>
<span data-ttu-id="ef1df-117">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ef1df-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ef1df-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef1df-118">-DatabaseName</span></span>
<span data-ttu-id="ef1df-119">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ef1df-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ef1df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef1df-120">-DefaultProfile</span></span>
<span data-ttu-id="ef1df-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef1df-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef1df-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef1df-122">-InputObject</span></span>
<span data-ttu-id="ef1df-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ef1df-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ef1df-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ef1df-124">-Name</span></span>
<span data-ttu-id="ef1df-125">O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="ef1df-125">The name of the data connection.</span></span>

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

### <span data-ttu-id="ef1df-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef1df-126">-ResourceGroupName</span></span>
<span data-ttu-id="ef1df-127">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ef1df-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ef1df-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef1df-128">-SubscriptionId</span></span>
<span data-ttu-id="ef1df-129">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ef1df-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef1df-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ef1df-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ef1df-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1df-131">CommonParameters</span></span>
<span data-ttu-id="ef1df-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef1df-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1df-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef1df-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1df-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef1df-134">INPUTS</span></span>

### <span data-ttu-id="ef1df-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ef1df-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ef1df-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ef1df-136">OUTPUTS</span></span>

### <span data-ttu-id="ef1df-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="ef1df-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="ef1df-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="ef1df-138">NOTES</span></span>

<span data-ttu-id="ef1df-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ef1df-139">ALIASES</span></span>

<span data-ttu-id="ef1df-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="ef1df-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ef1df-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ef1df-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef1df-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ef1df-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ef1df-143">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="ef1df-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ef1df-144">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="ef1df-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ef1df-145">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ef1df-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ef1df-146">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="ef1df-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ef1df-147">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ef1df-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ef1df-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ef1df-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ef1df-149">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef1df-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ef1df-150">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="ef1df-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ef1df-151">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ef1df-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ef1df-152">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ef1df-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ef1df-153">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ef1df-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ef1df-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef1df-154">RELATED LINKS</span></span>

