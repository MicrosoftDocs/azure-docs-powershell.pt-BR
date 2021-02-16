---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 80ab75e2361cf052e88377e9d7a393fb36627ae7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117590"
---
# <span data-ttu-id="060c5-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="060c5-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="060c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="060c5-102">SYNOPSIS</span></span>
<span data-ttu-id="060c5-103">Cria um banco de dados de cluster Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="060c5-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="060c5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="060c5-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="060c5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="060c5-105">DESCRIPTION</span></span>
<span data-ttu-id="060c5-106">Cria um banco de dados de cluster Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="060c5-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="060c5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="060c5-107">EXAMPLES</span></span>

### <span data-ttu-id="060c5-108">Exemplo 1: Criar um banco de dados de banco de dados cluster Kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="060c5-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="060c5-109">O comando acima cria uma entidade de banco de dados de cluster Kusto</span><span class="sxs-lookup"><span data-stu-id="060c5-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="060c5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="060c5-110">PARAMETERS</span></span>

### <span data-ttu-id="060c5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="060c5-111">-AsJob</span></span>
<span data-ttu-id="060c5-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="060c5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="060c5-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="060c5-113">-ClusterName</span></span>
<span data-ttu-id="060c5-114">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="060c5-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="060c5-115">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="060c5-115">-DatabaseName</span></span>
<span data-ttu-id="060c5-116">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="060c5-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="060c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="060c5-117">-DefaultProfile</span></span>
<span data-ttu-id="060c5-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="060c5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="060c5-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="060c5-119">-NoWait</span></span>
<span data-ttu-id="060c5-120">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="060c5-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="060c5-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="060c5-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="060c5-122">O nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="060c5-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="060c5-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="060c5-123">-PrincipalId</span></span>
<span data-ttu-id="060c5-124">A ID principal atribuída à entidade de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="060c5-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="060c5-125">Pode ser um email de usuário, uma ID de aplicativo ou um nome de grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="060c5-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="060c5-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="060c5-126">-PrincipalType</span></span>
<span data-ttu-id="060c5-127">Tipo de entidade.</span><span class="sxs-lookup"><span data-stu-id="060c5-127">Principal type.</span></span>

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

### <span data-ttu-id="060c5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="060c5-128">-ResourceGroupName</span></span>
<span data-ttu-id="060c5-129">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="060c5-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="060c5-130">-Função</span><span class="sxs-lookup"><span data-stu-id="060c5-130">-Role</span></span>
<span data-ttu-id="060c5-131">Função principal do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="060c5-131">Database principal role.</span></span>

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

### <span data-ttu-id="060c5-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="060c5-132">-SubscriptionId</span></span>
<span data-ttu-id="060c5-133">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="060c5-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="060c5-134">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="060c5-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="060c5-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="060c5-135">-TenantId</span></span>
<span data-ttu-id="060c5-136">A ID do locatário da entidade</span><span class="sxs-lookup"><span data-stu-id="060c5-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="060c5-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="060c5-137">-Confirm</span></span>
<span data-ttu-id="060c5-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="060c5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="060c5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="060c5-139">-WhatIf</span></span>
<span data-ttu-id="060c5-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="060c5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="060c5-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="060c5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="060c5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="060c5-142">CommonParameters</span></span>
<span data-ttu-id="060c5-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="060c5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="060c5-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="060c5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="060c5-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="060c5-145">INPUTS</span></span>

## <span data-ttu-id="060c5-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="060c5-146">OUTPUTS</span></span>

### <span data-ttu-id="060c5-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="060c5-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="060c5-148">Notas</span><span class="sxs-lookup"><span data-stu-id="060c5-148">NOTES</span></span>

<span data-ttu-id="060c5-149">Aliases</span><span class="sxs-lookup"><span data-stu-id="060c5-149">ALIASES</span></span>

## <span data-ttu-id="060c5-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="060c5-150">RELATED LINKS</span></span>

