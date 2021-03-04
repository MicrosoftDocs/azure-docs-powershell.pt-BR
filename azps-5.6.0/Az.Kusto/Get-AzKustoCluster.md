---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 753f2e4f2a1e2b60a12570307b518a5f2a78887b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886953"
---
# <span data-ttu-id="0624d-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="0624d-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="0624d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0624d-102">SYNOPSIS</span></span>
<span data-ttu-id="0624d-103">Obtém um cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0624d-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="0624d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0624d-104">SYNTAX</span></span>

### <span data-ttu-id="0624d-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0624d-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0624d-106">Obter</span><span class="sxs-lookup"><span data-stu-id="0624d-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0624d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0624d-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0624d-108">Listar</span><span class="sxs-lookup"><span data-stu-id="0624d-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0624d-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0624d-109">DESCRIPTION</span></span>
<span data-ttu-id="0624d-110">Obtém um cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0624d-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="0624d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0624d-111">EXAMPLES</span></span>

### <span data-ttu-id="0624d-112">Exemplo 1: Listar todos os clusters Kusto em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0624d-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="0624d-113">O comando acima lista todos os clusters Kusto no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="0624d-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="0624d-114">Exemplo 2: Obter um cluster Kusto específico pelo nome</span><span class="sxs-lookup"><span data-stu-id="0624d-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="0624d-115">O comando acima retorna o cluster Kusto chamado "testnewkustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="0624d-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="0624d-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0624d-116">PARAMETERS</span></span>

### <span data-ttu-id="0624d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0624d-117">-DefaultProfile</span></span>
<span data-ttu-id="0624d-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0624d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0624d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0624d-119">-InputObject</span></span>
<span data-ttu-id="0624d-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0624d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0624d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0624d-121">-Name</span></span>
<span data-ttu-id="0624d-122">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0624d-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0624d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0624d-123">-ResourceGroupName</span></span>
<span data-ttu-id="0624d-124">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0624d-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0624d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0624d-125">-SubscriptionId</span></span>
<span data-ttu-id="0624d-126">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0624d-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0624d-127">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0624d-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0624d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0624d-128">CommonParameters</span></span>
<span data-ttu-id="0624d-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0624d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0624d-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0624d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0624d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0624d-131">INPUTS</span></span>

### <span data-ttu-id="0624d-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0624d-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0624d-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0624d-133">OUTPUTS</span></span>

### <span data-ttu-id="0624d-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="0624d-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="0624d-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="0624d-135">NOTES</span></span>

<span data-ttu-id="0624d-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0624d-136">ALIASES</span></span>

<span data-ttu-id="0624d-137">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="0624d-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0624d-138">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0624d-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0624d-139">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0624d-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0624d-140">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="0624d-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0624d-141">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="0624d-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0624d-142">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0624d-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0624d-143">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="0624d-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0624d-144">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0624d-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0624d-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="0624d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0624d-146">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="0624d-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0624d-147">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0624d-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0624d-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0624d-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0624d-149">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0624d-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0624d-150">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0624d-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0624d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0624d-151">RELATED LINKS</span></span>

