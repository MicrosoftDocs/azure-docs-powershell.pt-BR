---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 9fd729a85babf1440516c52f0e7737f4c0d0d281
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887722"
---
# <span data-ttu-id="f9b6d-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f9b6d-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="f9b6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b6d-103">Cria um banco de dados de cluster Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="f9b6d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f9b6d-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f9b6d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f9b6d-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b6d-106">Cria um banco de dados de cluster Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="f9b6d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9b6d-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b6d-108">Exemplo 1: Criar um banco de dados de cluster Kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="f9b6d-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="f9b6d-109">O comando acima cria um banco de dados de cluster Kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="f9b6d-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="f9b6d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f9b6d-110">PARAMETERS</span></span>

### <span data-ttu-id="f9b6d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9b6d-111">-AsJob</span></span>
<span data-ttu-id="f9b6d-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f9b6d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f9b6d-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f9b6d-113">-ClusterName</span></span>
<span data-ttu-id="f9b6d-114">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f9b6d-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f9b6d-115">-DatabaseName</span></span>
<span data-ttu-id="f9b6d-116">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f9b6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b6d-117">-DefaultProfile</span></span>
<span data-ttu-id="f9b6d-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b6d-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f9b6d-119">-NoWait</span></span>
<span data-ttu-id="f9b6d-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="f9b6d-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f9b6d-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f9b6d-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="f9b6d-122">O nome da entidade KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="f9b6d-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="f9b6d-123">-PrincipalId</span></span>
<span data-ttu-id="f9b6d-124">A ID principal atribuída à entidade de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="f9b6d-125">Pode ser um email de usuário, ID do aplicativo ou nome do grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="f9b6d-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="f9b6d-126">-PrincipalType</span></span>
<span data-ttu-id="f9b6d-127">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-127">Principal type.</span></span>

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

### <span data-ttu-id="f9b6d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b6d-128">-ResourceGroupName</span></span>
<span data-ttu-id="f9b6d-129">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f9b6d-130">-Role</span><span class="sxs-lookup"><span data-stu-id="f9b6d-130">-Role</span></span>
<span data-ttu-id="f9b6d-131">Função principal do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-131">Database principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DatabasePrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b6d-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9b6d-132">-SubscriptionId</span></span>
<span data-ttu-id="f9b6d-133">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f9b6d-134">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f9b6d-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="f9b6d-135">-TenantId</span></span>
<span data-ttu-id="f9b6d-136">A id de locatário da entidade principal</span><span class="sxs-lookup"><span data-stu-id="f9b6d-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="f9b6d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9b6d-137">-Confirm</span></span>
<span data-ttu-id="f9b6d-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b6d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b6d-139">-WhatIf</span></span>
<span data-ttu-id="f9b6d-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9b6d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b6d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b6d-142">CommonParameters</span></span>
<span data-ttu-id="f9b6d-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b6d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b6d-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9b6d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b6d-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9b6d-145">INPUTS</span></span>

## <span data-ttu-id="f9b6d-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f9b6d-146">OUTPUTS</span></span>

### <span data-ttu-id="f9b6d-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="f9b6d-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="f9b6d-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="f9b6d-148">NOTES</span></span>

<span data-ttu-id="f9b6d-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f9b6d-149">ALIASES</span></span>

## <span data-ttu-id="f9b6d-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9b6d-150">RELATED LINKS</span></span>

