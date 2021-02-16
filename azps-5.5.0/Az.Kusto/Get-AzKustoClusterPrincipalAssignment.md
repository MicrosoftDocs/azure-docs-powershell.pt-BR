---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 9ff5021e43b9d23fc79ffca81519809ae0052558
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113034"
---
# <span data-ttu-id="9ceed-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="9ceed-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="9ceed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ceed-102">SYNOPSIS</span></span>
<span data-ttu-id="9ceed-103">Obtém um cluster principal KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="9ceed-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="9ceed-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ceed-104">SYNTAX</span></span>

### <span data-ttu-id="9ceed-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9ceed-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9ceed-106">Obter</span><span class="sxs-lookup"><span data-stu-id="9ceed-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9ceed-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9ceed-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ceed-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ceed-108">DESCRIPTION</span></span>
<span data-ttu-id="9ceed-109">Obtém um cluster principal KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="9ceed-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="9ceed-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9ceed-110">EXAMPLES</span></span>

### <span data-ttu-id="9ceed-111">Exemplo 1: Listar todas as entidades de cluster Kusto</span><span class="sxs-lookup"><span data-stu-id="9ceed-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="9ceed-112">O comando acima lista todas as principaisAssignment no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="9ceed-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="9ceed-113">Exemplo 2: obtém um cluster principal KustoAssignment por nome</span><span class="sxs-lookup"><span data-stu-id="9ceed-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="9ceed-114">O comando acima retorna o cluster principal KustoAssignment chamado "kustoprincipal1" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="9ceed-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="9ceed-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ceed-115">PARAMETERS</span></span>

### <span data-ttu-id="9ceed-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9ceed-116">-ClusterName</span></span>
<span data-ttu-id="9ceed-117">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="9ceed-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9ceed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ceed-118">-DefaultProfile</span></span>
<span data-ttu-id="9ceed-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ceed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ceed-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ceed-120">-InputObject</span></span>
<span data-ttu-id="9ceed-121">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="9ceed-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9ceed-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="9ceed-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="9ceed-123">O nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9ceed-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="9ceed-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ceed-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ceed-125">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="9ceed-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9ceed-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ceed-126">-SubscriptionId</span></span>
<span data-ttu-id="9ceed-127">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9ceed-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9ceed-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9ceed-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9ceed-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ceed-129">CommonParameters</span></span>
<span data-ttu-id="9ceed-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ceed-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ceed-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ceed-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ceed-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="9ceed-132">INPUTS</span></span>

### <span data-ttu-id="9ceed-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9ceed-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9ceed-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="9ceed-134">OUTPUTS</span></span>

### <span data-ttu-id="9ceed-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="9ceed-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="9ceed-136">Notas</span><span class="sxs-lookup"><span data-stu-id="9ceed-136">NOTES</span></span>

<span data-ttu-id="9ceed-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="9ceed-137">ALIASES</span></span>

<span data-ttu-id="9ceed-138">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="9ceed-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9ceed-139">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="9ceed-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9ceed-140">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9ceed-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9ceed-141">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="9ceed-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9ceed-142">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="9ceed-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9ceed-143">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="9ceed-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9ceed-144">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="9ceed-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9ceed-145">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="9ceed-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9ceed-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="9ceed-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9ceed-147">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ceed-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9ceed-148">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9ceed-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9ceed-149">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="9ceed-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9ceed-150">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9ceed-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9ceed-151">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9ceed-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9ceed-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ceed-152">RELATED LINKS</span></span>

