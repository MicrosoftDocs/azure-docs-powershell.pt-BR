---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: e1fee17e7f7bf58785c96c28bc6e1f3f66136bb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113028"
---
# <span data-ttu-id="1302f-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="1302f-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="1302f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1302f-102">SYNOPSIS</span></span>
<span data-ttu-id="1302f-103">Retorna uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="1302f-103">Returns a data connection.</span></span>

## <span data-ttu-id="1302f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1302f-104">SYNTAX</span></span>

### <span data-ttu-id="1302f-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1302f-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1302f-106">Obter</span><span class="sxs-lookup"><span data-stu-id="1302f-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1302f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1302f-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1302f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1302f-108">DESCRIPTION</span></span>
<span data-ttu-id="1302f-109">Retorna uma conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="1302f-109">Returns a data connection.</span></span>

## <span data-ttu-id="1302f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1302f-110">EXAMPLES</span></span>

### <span data-ttu-id="1302f-111">Exemplo 1: Listar todas as conexões de dados em um banco de dados específico</span><span class="sxs-lookup"><span data-stu-id="1302f-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1302f-112">O comando acima retorna todos os bancos de dados do Kusto no cluster "testnewkustocluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="1302f-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="1302f-113">Exemplo 2: Obter uma conexão de dados específica por nome</span><span class="sxs-lookup"><span data-stu-id="1302f-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="1302f-114">O comando acima retorna a conexão de dados chamada "mykustodataconnection" no banco de dados "mykustodatabase" do cluster existente "testnewkustocluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="1302f-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="1302f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1302f-115">PARAMETERS</span></span>

### <span data-ttu-id="1302f-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1302f-116">-ClusterName</span></span>
<span data-ttu-id="1302f-117">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="1302f-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1302f-118">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="1302f-118">-DatabaseName</span></span>
<span data-ttu-id="1302f-119">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="1302f-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="1302f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1302f-120">-DefaultProfile</span></span>
<span data-ttu-id="1302f-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1302f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1302f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1302f-122">-InputObject</span></span>
<span data-ttu-id="1302f-123">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="1302f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1302f-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1302f-124">-Name</span></span>
<span data-ttu-id="1302f-125">O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="1302f-125">The name of the data connection.</span></span>

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

### <span data-ttu-id="1302f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1302f-126">-ResourceGroupName</span></span>
<span data-ttu-id="1302f-127">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="1302f-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1302f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1302f-128">-SubscriptionId</span></span>
<span data-ttu-id="1302f-129">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1302f-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1302f-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="1302f-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1302f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1302f-131">CommonParameters</span></span>
<span data-ttu-id="1302f-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1302f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1302f-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1302f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1302f-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="1302f-134">INPUTS</span></span>

### <span data-ttu-id="1302f-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1302f-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1302f-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="1302f-136">OUTPUTS</span></span>

### <span data-ttu-id="1302f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="1302f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="1302f-138">Notas</span><span class="sxs-lookup"><span data-stu-id="1302f-138">NOTES</span></span>

<span data-ttu-id="1302f-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="1302f-139">ALIASES</span></span>

<span data-ttu-id="1302f-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="1302f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1302f-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="1302f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1302f-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1302f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1302f-143">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="1302f-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1302f-144">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="1302f-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1302f-145">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="1302f-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1302f-146">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="1302f-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1302f-147">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="1302f-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1302f-148">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="1302f-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1302f-149">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="1302f-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1302f-150">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="1302f-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1302f-151">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="1302f-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1302f-152">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1302f-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1302f-153">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="1302f-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1302f-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1302f-154">RELATED LINKS</span></span>

