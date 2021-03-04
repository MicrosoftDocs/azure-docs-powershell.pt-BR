---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: f1c96909421dcc21d2b1f318a923ef7f9b804bf8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901467"
---
# <span data-ttu-id="0b2a7-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="0b2a7-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="0b2a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b2a7-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2a7-103">Verifica se o nome da atribuição principal é válido e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="0b2a7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0b2a7-104">SYNTAX</span></span>

### <span data-ttu-id="0b2a7-105">CheckExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0b2a7-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0b2a7-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0b2a7-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b2a7-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b2a7-107">DESCRIPTION</span></span>
<span data-ttu-id="0b2a7-108">Verifica se o nome da atribuição principal é válido e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="0b2a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b2a7-109">EXAMPLES</span></span>

### <span data-ttu-id="0b2a7-110">Exemplo 1: Verifique a disponibilidade de um nome de entidade de cluster que está em uso</span><span class="sxs-lookup"><span data-stu-id="0b2a7-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="0b2a7-111">O comando acima retorna se existe ou não um PrincipalAssignment chamado "myprincipal" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="0b2a7-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="0b2a7-112">Exemplo 2: Verifique a disponibilidade de um nome de entidade de cluster que não está em uso</span><span class="sxs-lookup"><span data-stu-id="0b2a7-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="0b2a7-113">O comando acima retorna se existe ou não um PrincipalAssignment chamado "newprincipal" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="0b2a7-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="0b2a7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0b2a7-114">PARAMETERS</span></span>

### <span data-ttu-id="0b2a7-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0b2a7-115">-ClusterName</span></span>
<span data-ttu-id="0b2a7-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2a7-117">-DefaultProfile</span></span>
<span data-ttu-id="0b2a7-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b2a7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b2a7-119">-InputObject</span></span>
<span data-ttu-id="0b2a7-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0b2a7-121">-Name</span></span>
<span data-ttu-id="0b2a7-122">Nome do recurso Atribuição Principal.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-122">Principal Assignment resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2a7-123">-ResourceGroupName</span></span>
<span data-ttu-id="0b2a7-124">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b2a7-125">-SubscriptionId</span></span>
<span data-ttu-id="0b2a7-126">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0b2a7-127">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a7-128">-Type</span><span class="sxs-lookup"><span data-stu-id="0b2a7-128">-Type</span></span>
<span data-ttu-id="0b2a7-129">O tipo de recurso, Microsoft.Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b2a7-130">-Confirm</span></span>
<span data-ttu-id="0b2a7-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2a7-132">-WhatIf</span></span>
<span data-ttu-id="0b2a7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b2a7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2a7-135">CommonParameters</span></span>
<span data-ttu-id="0b2a7-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2a7-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b2a7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2a7-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b2a7-138">INPUTS</span></span>

### <span data-ttu-id="0b2a7-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0b2a7-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0b2a7-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0b2a7-140">OUTPUTS</span></span>

### <span data-ttu-id="0b2a7-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="0b2a7-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="0b2a7-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="0b2a7-142">NOTES</span></span>

<span data-ttu-id="0b2a7-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0b2a7-143">ALIASES</span></span>

<span data-ttu-id="0b2a7-144">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="0b2a7-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b2a7-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b2a7-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b2a7-147">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="0b2a7-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0b2a7-148">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0b2a7-149">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0b2a7-150">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0b2a7-151">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0b2a7-152">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="0b2a7-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0b2a7-153">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0b2a7-154">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0b2a7-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0b2a7-156">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0b2a7-157">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0b2a7-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0b2a7-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b2a7-158">RELATED LINKS</span></span>

