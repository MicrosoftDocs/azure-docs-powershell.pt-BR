---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 738f0d4b4033dd7cccdc0fbabe94d2dfde9779c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886329"
---
# <span data-ttu-id="57b10-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="57b10-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="57b10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57b10-102">SYNOPSIS</span></span>
<span data-ttu-id="57b10-103">Crie uma entidade de cluster KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="57b10-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="57b10-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="57b10-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57b10-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="57b10-105">DESCRIPTION</span></span>
<span data-ttu-id="57b10-106">Crie uma entidade de cluster KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="57b10-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="57b10-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57b10-107">EXAMPLES</span></span>

### <span data-ttu-id="57b10-108">Exemplo 1: Criar uma entidade de cluster KustoAssignment</span><span class="sxs-lookup"><span data-stu-id="57b10-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="57b10-109">O comando acima cria uma entidade de cluster KustoAssignment</span><span class="sxs-lookup"><span data-stu-id="57b10-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="57b10-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="57b10-110">PARAMETERS</span></span>

### <span data-ttu-id="57b10-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57b10-111">-AsJob</span></span>
<span data-ttu-id="57b10-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="57b10-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b10-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="57b10-113">-ClusterName</span></span>
<span data-ttu-id="57b10-114">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="57b10-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="57b10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b10-115">-DefaultProfile</span></span>
<span data-ttu-id="57b10-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57b10-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57b10-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="57b10-117">-NoWait</span></span>
<span data-ttu-id="57b10-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="57b10-118">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b10-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="57b10-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="57b10-120">O nome da entidade KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="57b10-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="57b10-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="57b10-121">-PrincipalId</span></span>
<span data-ttu-id="57b10-122">A ID principal atribuída à entidade de cluster.</span><span class="sxs-lookup"><span data-stu-id="57b10-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="57b10-123">Pode ser um email de usuário, ID do aplicativo ou nome do grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="57b10-123">It can be a user email, application ID, or security group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b10-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="57b10-124">-PrincipalType</span></span>
<span data-ttu-id="57b10-125">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="57b10-125">Principal type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.PrincipalType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b10-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57b10-126">-ResourceGroupName</span></span>
<span data-ttu-id="57b10-127">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="57b10-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="57b10-128">-Role</span><span class="sxs-lookup"><span data-stu-id="57b10-128">-Role</span></span>
<span data-ttu-id="57b10-129">Função principal do cluster.</span><span class="sxs-lookup"><span data-stu-id="57b10-129">Cluster principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.ClusterPrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b10-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57b10-130">-SubscriptionId</span></span>
<span data-ttu-id="57b10-131">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57b10-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57b10-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="57b10-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b10-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="57b10-133">-TenantId</span></span>
<span data-ttu-id="57b10-134">A id de locatário da entidade principal</span><span class="sxs-lookup"><span data-stu-id="57b10-134">The tenant id of the principal</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b10-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57b10-135">-Confirm</span></span>
<span data-ttu-id="57b10-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57b10-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57b10-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57b10-137">-WhatIf</span></span>
<span data-ttu-id="57b10-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57b10-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57b10-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57b10-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57b10-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b10-140">CommonParameters</span></span>
<span data-ttu-id="57b10-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57b10-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b10-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57b10-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b10-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57b10-143">INPUTS</span></span>

## <span data-ttu-id="57b10-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="57b10-144">OUTPUTS</span></span>

### <span data-ttu-id="57b10-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="57b10-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="57b10-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="57b10-146">NOTES</span></span>

<span data-ttu-id="57b10-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="57b10-147">ALIASES</span></span>

## <span data-ttu-id="57b10-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57b10-148">RELATED LINKS</span></span>

