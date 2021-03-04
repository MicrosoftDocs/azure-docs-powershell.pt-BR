---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: b89327f80ec5f8e0f5faf9f66e943ee07601799e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886946"
---
# <span data-ttu-id="a912a-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="a912a-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="a912a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a912a-102">SYNOPSIS</span></span>
<span data-ttu-id="a912a-103">Obtém uma entidade de cluster KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="a912a-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="a912a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a912a-104">SYNTAX</span></span>

### <span data-ttu-id="a912a-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a912a-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a912a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a912a-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a912a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a912a-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a912a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a912a-108">DESCRIPTION</span></span>
<span data-ttu-id="a912a-109">Obtém uma entidade de cluster KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="a912a-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="a912a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a912a-110">EXAMPLES</span></span>

### <span data-ttu-id="a912a-111">Exemplo 1: Listar todas as entidades de cluster KustoAssignment</span><span class="sxs-lookup"><span data-stu-id="a912a-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="a912a-112">O comando acima lista todas as principaisAssignment no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="a912a-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="a912a-113">Exemplo 2: Obtém uma entidade de cluster KustoAssignment pelo nome</span><span class="sxs-lookup"><span data-stu-id="a912a-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="a912a-114">O comando acima retorna a entidade de cluster KustoAssignment chamada "kustoprincipal1" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="a912a-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="a912a-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a912a-115">PARAMETERS</span></span>

### <span data-ttu-id="a912a-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a912a-116">-ClusterName</span></span>
<span data-ttu-id="a912a-117">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a912a-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a912a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a912a-118">-DefaultProfile</span></span>
<span data-ttu-id="a912a-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a912a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a912a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a912a-120">-InputObject</span></span>
<span data-ttu-id="a912a-121">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a912a-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a912a-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="a912a-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="a912a-123">O nome da entidade KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="a912a-123">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a912a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a912a-124">-ResourceGroupName</span></span>
<span data-ttu-id="a912a-125">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a912a-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a912a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a912a-126">-SubscriptionId</span></span>
<span data-ttu-id="a912a-127">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a912a-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a912a-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a912a-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a912a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a912a-129">CommonParameters</span></span>
<span data-ttu-id="a912a-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a912a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a912a-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a912a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a912a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a912a-132">INPUTS</span></span>

### <span data-ttu-id="a912a-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a912a-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a912a-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a912a-134">OUTPUTS</span></span>

### <span data-ttu-id="a912a-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="a912a-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="a912a-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="a912a-136">NOTES</span></span>

<span data-ttu-id="a912a-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a912a-137">ALIASES</span></span>

<span data-ttu-id="a912a-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a912a-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a912a-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a912a-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a912a-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a912a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a912a-141">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="a912a-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a912a-142">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="a912a-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a912a-143">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a912a-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a912a-144">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="a912a-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a912a-145">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a912a-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a912a-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a912a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a912a-147">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="a912a-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a912a-148">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a912a-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a912a-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a912a-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a912a-150">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a912a-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a912a-151">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a912a-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a912a-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a912a-152">RELATED LINKS</span></span>

