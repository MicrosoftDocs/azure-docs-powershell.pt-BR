---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261193"
---
# <span data-ttu-id="3b74a-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="3b74a-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="3b74a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b74a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b74a-103">Verifica se o nome da atribuição principal é válido e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="3b74a-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="3b74a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b74a-104">SYNTAX</span></span>

### <span data-ttu-id="3b74a-105">CheckExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="3b74a-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3b74a-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3b74a-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3b74a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b74a-107">DESCRIPTION</span></span>
<span data-ttu-id="3b74a-108">Verifica se o nome da atribuição principal é válido e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="3b74a-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="3b74a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b74a-109">EXAMPLES</span></span>

### <span data-ttu-id="3b74a-110">Exemplo 1: verificar a disponibilidade de um nome de principalassignment de cluster que está em uso</span><span class="sxs-lookup"><span data-stu-id="3b74a-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="3b74a-111">O comando acima retorna se um PrincipalAssignment chamado "myupn" existe no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="3b74a-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="3b74a-112">Exemplo 2: verificar a disponibilidade de um nome de principalassignment de cluster que não está em uso</span><span class="sxs-lookup"><span data-stu-id="3b74a-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="3b74a-113">O comando acima retorna se um PrincipalAssignment chamado "newprincipal" existe no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="3b74a-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="3b74a-114">OS</span><span class="sxs-lookup"><span data-stu-id="3b74a-114">PARAMETERS</span></span>

### <span data-ttu-id="3b74a-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3b74a-115">-ClusterName</span></span>
<span data-ttu-id="3b74a-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3b74a-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3b74a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b74a-117">-DefaultProfile</span></span>
<span data-ttu-id="3b74a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b74a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b74a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b74a-119">-InputObject</span></span>
<span data-ttu-id="3b74a-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3b74a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3b74a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b74a-121">-Name</span></span>
<span data-ttu-id="3b74a-122">Nome do recurso da atribuição principal.</span><span class="sxs-lookup"><span data-stu-id="3b74a-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="3b74a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b74a-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b74a-124">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3b74a-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3b74a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b74a-125">-SubscriptionId</span></span>
<span data-ttu-id="3b74a-126">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3b74a-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3b74a-127">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3b74a-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3b74a-128">-Digite</span><span class="sxs-lookup"><span data-stu-id="3b74a-128">-Type</span></span>
<span data-ttu-id="3b74a-129">O tipo de recurso, Microsoft. Kusto/clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="3b74a-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="3b74a-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3b74a-130">-Confirm</span></span>
<span data-ttu-id="3b74a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b74a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b74a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b74a-132">-WhatIf</span></span>
<span data-ttu-id="3b74a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b74a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b74a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b74a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b74a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b74a-135">CommonParameters</span></span>
<span data-ttu-id="3b74a-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b74a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b74a-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b74a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b74a-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b74a-138">INPUTS</span></span>

### <span data-ttu-id="3b74a-139">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="3b74a-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3b74a-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b74a-140">OUTPUTS</span></span>

### <span data-ttu-id="3b74a-141">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="3b74a-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="3b74a-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b74a-142">NOTES</span></span>

<span data-ttu-id="3b74a-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3b74a-143">ALIASES</span></span>

<span data-ttu-id="3b74a-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="3b74a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b74a-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3b74a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b74a-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b74a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b74a-147">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="3b74a-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b74a-148">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="3b74a-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3b74a-149">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3b74a-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3b74a-150">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="3b74a-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3b74a-151">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3b74a-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3b74a-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3b74a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b74a-153">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b74a-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3b74a-154">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="3b74a-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3b74a-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3b74a-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3b74a-156">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3b74a-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3b74a-157">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3b74a-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3b74a-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b74a-158">RELATED LINKS</span></span>

