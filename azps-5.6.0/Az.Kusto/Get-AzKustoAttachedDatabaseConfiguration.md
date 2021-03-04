---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fc4d1edfe23e6520af230960b6a9262afba43b6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886956"
---
# <span data-ttu-id="fbd13-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbd13-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="fbd13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbd13-102">SYNOPSIS</span></span>
<span data-ttu-id="fbd13-103">Retorna uma configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="fbd13-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="fbd13-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fbd13-104">SYNTAX</span></span>

### <span data-ttu-id="fbd13-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fbd13-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fbd13-106">Obter</span><span class="sxs-lookup"><span data-stu-id="fbd13-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fbd13-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fbd13-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbd13-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fbd13-108">DESCRIPTION</span></span>
<span data-ttu-id="fbd13-109">Retorna uma configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="fbd13-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="fbd13-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbd13-110">EXAMPLES</span></span>

### <span data-ttu-id="fbd13-111">Exemplo 1: Listar todos os AttachedDatabaseConfigurations em um cluster</span><span class="sxs-lookup"><span data-stu-id="fbd13-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="fbd13-112">O comando acima lista todos os AttachedDatabaseConfigurations no cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="fbd13-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="fbd13-113">Exemplo 2: Obter um AttachedDatabaseConfiguration específico em um cluster</span><span class="sxs-lookup"><span data-stu-id="fbd13-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="fbd13-114">O comando acima retorna o AttachedDatabaseConfigurations chamado "myfollowerconfiguration" no cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="fbd13-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="fbd13-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fbd13-115">PARAMETERS</span></span>

### <span data-ttu-id="fbd13-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fbd13-116">-ClusterName</span></span>
<span data-ttu-id="fbd13-117">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fbd13-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="fbd13-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbd13-118">-DefaultProfile</span></span>
<span data-ttu-id="fbd13-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fbd13-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbd13-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbd13-120">-InputObject</span></span>
<span data-ttu-id="fbd13-121">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fbd13-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fbd13-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fbd13-122">-Name</span></span>
<span data-ttu-id="fbd13-123">O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="fbd13-123">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd13-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbd13-124">-ResourceGroupName</span></span>
<span data-ttu-id="fbd13-125">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fbd13-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="fbd13-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fbd13-126">-SubscriptionId</span></span>
<span data-ttu-id="fbd13-127">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fbd13-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fbd13-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="fbd13-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fbd13-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbd13-129">CommonParameters</span></span>
<span data-ttu-id="fbd13-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbd13-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbd13-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbd13-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbd13-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbd13-132">INPUTS</span></span>

### <span data-ttu-id="fbd13-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="fbd13-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="fbd13-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fbd13-134">OUTPUTS</span></span>

### <span data-ttu-id="fbd13-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbd13-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="fbd13-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="fbd13-136">NOTES</span></span>

<span data-ttu-id="fbd13-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fbd13-137">ALIASES</span></span>

<span data-ttu-id="fbd13-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="fbd13-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fbd13-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="fbd13-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fbd13-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fbd13-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fbd13-141">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="fbd13-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fbd13-142">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="fbd13-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="fbd13-143">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fbd13-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="fbd13-144">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="fbd13-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="fbd13-145">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fbd13-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="fbd13-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="fbd13-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fbd13-147">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="fbd13-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="fbd13-148">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fbd13-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="fbd13-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fbd13-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="fbd13-150">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fbd13-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fbd13-151">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="fbd13-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fbd13-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbd13-152">RELATED LINKS</span></span>

