---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: fafc31700477de968c453002e903b52aa73967d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118942"
---
# <span data-ttu-id="fd3ae-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="fd3ae-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="fd3ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd3ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fd3ae-103">Crie um cluster principal KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="fd3ae-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd3ae-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fd3ae-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd3ae-105">DESCRIPTION</span></span>
<span data-ttu-id="fd3ae-106">Crie um cluster principal KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="fd3ae-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd3ae-107">EXAMPLES</span></span>

### <span data-ttu-id="fd3ae-108">Exemplo 1: Criar um cluster principal KustoAssignment</span><span class="sxs-lookup"><span data-stu-id="fd3ae-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="fd3ae-109">O comando acima cria um cluster principal KustoAssignment</span><span class="sxs-lookup"><span data-stu-id="fd3ae-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="fd3ae-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd3ae-110">PARAMETERS</span></span>

### <span data-ttu-id="fd3ae-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd3ae-111">-AsJob</span></span>
<span data-ttu-id="fd3ae-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="fd3ae-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fd3ae-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fd3ae-113">-ClusterName</span></span>
<span data-ttu-id="fd3ae-114">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="fd3ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd3ae-115">-DefaultProfile</span></span>
<span data-ttu-id="fd3ae-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd3ae-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fd3ae-117">-NoWait</span></span>
<span data-ttu-id="fd3ae-118">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="fd3ae-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fd3ae-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="fd3ae-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="fd3ae-120">O nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="fd3ae-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="fd3ae-121">-PrincipalId</span></span>
<span data-ttu-id="fd3ae-122">A ID principal atribuída à entidade de cluster.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="fd3ae-123">Pode ser um email de usuário, uma ID de aplicativo ou um nome de grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="fd3ae-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="fd3ae-124">-PrincipalType</span></span>
<span data-ttu-id="fd3ae-125">Tipo de entidade.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-125">Principal type.</span></span>

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

### <span data-ttu-id="fd3ae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd3ae-126">-ResourceGroupName</span></span>
<span data-ttu-id="fd3ae-127">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="fd3ae-128">-Função</span><span class="sxs-lookup"><span data-stu-id="fd3ae-128">-Role</span></span>
<span data-ttu-id="fd3ae-129">Função de entidade de cluster.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="fd3ae-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd3ae-130">-SubscriptionId</span></span>
<span data-ttu-id="fd3ae-131">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fd3ae-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fd3ae-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="fd3ae-133">-TenantId</span></span>
<span data-ttu-id="fd3ae-134">A ID do locatário da entidade</span><span class="sxs-lookup"><span data-stu-id="fd3ae-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="fd3ae-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fd3ae-135">-Confirm</span></span>
<span data-ttu-id="fd3ae-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd3ae-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd3ae-137">-WhatIf</span></span>
<span data-ttu-id="fd3ae-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd3ae-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd3ae-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd3ae-140">CommonParameters</span></span>
<span data-ttu-id="fd3ae-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd3ae-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd3ae-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd3ae-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd3ae-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd3ae-143">INPUTS</span></span>

## <span data-ttu-id="fd3ae-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd3ae-144">OUTPUTS</span></span>

### <span data-ttu-id="fd3ae-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="fd3ae-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="fd3ae-146">Notas</span><span class="sxs-lookup"><span data-stu-id="fd3ae-146">NOTES</span></span>

<span data-ttu-id="fd3ae-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="fd3ae-147">ALIASES</span></span>

## <span data-ttu-id="fd3ae-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd3ae-148">RELATED LINKS</span></span>

