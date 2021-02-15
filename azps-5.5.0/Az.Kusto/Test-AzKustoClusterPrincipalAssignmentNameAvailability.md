---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: 0fbffb0effff782c154e4b6c38d6eb296b89ffb9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111824"
---
# <span data-ttu-id="590d1-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="590d1-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="590d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="590d1-102">SYNOPSIS</span></span>
<span data-ttu-id="590d1-103">Verifica se o nome da tarefa principal é válido e se ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="590d1-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="590d1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="590d1-104">SYNTAX</span></span>

### <span data-ttu-id="590d1-105">CheckExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="590d1-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="590d1-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="590d1-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="590d1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="590d1-107">DESCRIPTION</span></span>
<span data-ttu-id="590d1-108">Verifica se o nome da tarefa principal é válido e se ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="590d1-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="590d1-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="590d1-109">EXAMPLES</span></span>

### <span data-ttu-id="590d1-110">Exemplo 1: Verificar a disponibilidade de um nome de aferimento de entidade de cluster que está em uso</span><span class="sxs-lookup"><span data-stu-id="590d1-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="590d1-111">O comando acima retorna se existe ou não um PrincipalAssignment chamado "myprincipal" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="590d1-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="590d1-112">Exemplo 2: Verificar a disponibilidade de um nome de nome de entidade de cluster que não está em uso</span><span class="sxs-lookup"><span data-stu-id="590d1-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="590d1-113">O comando acima retorna se existe ou não um PrincipalAssignment chamado "newprincipal" no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="590d1-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="590d1-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="590d1-114">PARAMETERS</span></span>

### <span data-ttu-id="590d1-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="590d1-115">-ClusterName</span></span>
<span data-ttu-id="590d1-116">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="590d1-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="590d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="590d1-117">-DefaultProfile</span></span>
<span data-ttu-id="590d1-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="590d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="590d1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="590d1-119">-InputObject</span></span>
<span data-ttu-id="590d1-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="590d1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="590d1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="590d1-121">-Name</span></span>
<span data-ttu-id="590d1-122">Nome do recurso de Atribuição Principal.</span><span class="sxs-lookup"><span data-stu-id="590d1-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="590d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="590d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="590d1-124">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="590d1-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="590d1-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="590d1-125">-SubscriptionId</span></span>
<span data-ttu-id="590d1-126">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="590d1-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="590d1-127">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="590d1-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="590d1-128">-Tipo</span><span class="sxs-lookup"><span data-stu-id="590d1-128">-Type</span></span>
<span data-ttu-id="590d1-129">O tipo de recurso, Microsoft.Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="590d1-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="590d1-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="590d1-130">-Confirm</span></span>
<span data-ttu-id="590d1-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="590d1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="590d1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="590d1-132">-WhatIf</span></span>
<span data-ttu-id="590d1-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="590d1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="590d1-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="590d1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="590d1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="590d1-135">CommonParameters</span></span>
<span data-ttu-id="590d1-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="590d1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="590d1-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="590d1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="590d1-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="590d1-138">INPUTS</span></span>

### <span data-ttu-id="590d1-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="590d1-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="590d1-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="590d1-140">OUTPUTS</span></span>

### <span data-ttu-id="590d1-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="590d1-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="590d1-142">Notas</span><span class="sxs-lookup"><span data-stu-id="590d1-142">NOTES</span></span>

<span data-ttu-id="590d1-143">Aliases</span><span class="sxs-lookup"><span data-stu-id="590d1-143">ALIASES</span></span>

<span data-ttu-id="590d1-144">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="590d1-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="590d1-145">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="590d1-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="590d1-146">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="590d1-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="590d1-147">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="590d1-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="590d1-148">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="590d1-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="590d1-149">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="590d1-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="590d1-150">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="590d1-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="590d1-151">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="590d1-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="590d1-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="590d1-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="590d1-153">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="590d1-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="590d1-154">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="590d1-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="590d1-155">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="590d1-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="590d1-156">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="590d1-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="590d1-157">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="590d1-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="590d1-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="590d1-158">RELATED LINKS</span></span>

