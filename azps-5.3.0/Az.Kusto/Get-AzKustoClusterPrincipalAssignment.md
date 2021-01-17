---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 9ff5021e43b9d23fc79ffca81519809ae0052558
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427173"
---
# <span data-ttu-id="af850-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="af850-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="af850-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af850-102">SYNOPSIS</span></span>
<span data-ttu-id="af850-103">Obtém um Kusto de cluster de principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="af850-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="af850-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af850-104">SYNTAX</span></span>

### <span data-ttu-id="af850-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="af850-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="af850-106">Obter</span><span class="sxs-lookup"><span data-stu-id="af850-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="af850-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="af850-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="af850-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af850-108">DESCRIPTION</span></span>
<span data-ttu-id="af850-109">Obtém um Kusto de cluster de principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="af850-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="af850-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af850-110">EXAMPLES</span></span>

### <span data-ttu-id="af850-111">Exemplo 1: listar todos os principalAssignment de cluster Kusto</span><span class="sxs-lookup"><span data-stu-id="af850-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="af850-112">O comando acima lista todos os principalAssignment no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="af850-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="af850-113">Exemplo 2: Obtém um Kusto de cluster de principalAssignment por nome</span><span class="sxs-lookup"><span data-stu-id="af850-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="af850-114">O comando acima retorna o Kusto de cluster principalAssignment chamado "kustoprincipal1" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="af850-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="af850-115">OS</span><span class="sxs-lookup"><span data-stu-id="af850-115">PARAMETERS</span></span>

### <span data-ttu-id="af850-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="af850-116">-ClusterName</span></span>
<span data-ttu-id="af850-117">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="af850-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="af850-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af850-118">-DefaultProfile</span></span>
<span data-ttu-id="af850-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af850-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af850-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af850-120">-InputObject</span></span>
<span data-ttu-id="af850-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="af850-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="af850-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="af850-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="af850-123">O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="af850-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="af850-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af850-124">-ResourceGroupName</span></span>
<span data-ttu-id="af850-125">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="af850-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="af850-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af850-126">-SubscriptionId</span></span>
<span data-ttu-id="af850-127">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="af850-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="af850-128">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="af850-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="af850-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af850-129">CommonParameters</span></span>
<span data-ttu-id="af850-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af850-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af850-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af850-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af850-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af850-132">INPUTS</span></span>

### <span data-ttu-id="af850-133">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="af850-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="af850-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af850-134">OUTPUTS</span></span>

### <span data-ttu-id="af850-135">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200918. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="af850-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="af850-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af850-136">NOTES</span></span>

<span data-ttu-id="af850-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="af850-137">ALIASES</span></span>

<span data-ttu-id="af850-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="af850-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af850-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="af850-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af850-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="af850-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af850-141">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="af850-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="af850-142">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="af850-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="af850-143">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="af850-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="af850-144">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="af850-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="af850-145">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="af850-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="af850-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="af850-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="af850-147">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="af850-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="af850-148">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="af850-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="af850-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="af850-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="af850-150">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="af850-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="af850-151">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="af850-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="af850-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af850-152">RELATED LINKS</span></span>

