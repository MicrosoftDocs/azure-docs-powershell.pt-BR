---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 8f2a0cd576c3fe7f184d3f016f6666aa8749b5c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113548"
---
# <span data-ttu-id="cb0a3-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="cb0a3-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="cb0a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb0a3-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0a3-103">Crie um Kusto de cluster de principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="cb0a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb0a3-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb0a3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb0a3-105">DESCRIPTION</span></span>
<span data-ttu-id="cb0a3-106">Crie um Kusto de cluster de principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="cb0a3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb0a3-107">EXAMPLES</span></span>

### <span data-ttu-id="cb0a3-108">Exemplo 1: criar um cluster de Kusto de principalAssignment</span><span class="sxs-lookup"><span data-stu-id="cb0a3-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="cb0a3-109">O comando acima cria um cluster de Kusto de principalAssignment</span><span class="sxs-lookup"><span data-stu-id="cb0a3-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="cb0a3-110">OS</span><span class="sxs-lookup"><span data-stu-id="cb0a3-110">PARAMETERS</span></span>

### <span data-ttu-id="cb0a3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb0a3-111">-AsJob</span></span>
<span data-ttu-id="cb0a3-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="cb0a3-112">Run the command as a job</span></span>

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

### <span data-ttu-id="cb0a3-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cb0a3-113">-ClusterName</span></span>
<span data-ttu-id="cb0a3-114">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cb0a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0a3-115">-DefaultProfile</span></span>
<span data-ttu-id="cb0a3-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb0a3-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cb0a3-117">-NoWait</span></span>
<span data-ttu-id="cb0a3-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="cb0a3-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cb0a3-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="cb0a3-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="cb0a3-120">O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="cb0a3-121">-Entidade de segurança</span><span class="sxs-lookup"><span data-stu-id="cb0a3-121">-PrincipalId</span></span>
<span data-ttu-id="cb0a3-122">A ID da entidade de segurança atribuída à entidade de segurança do grupo.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="cb0a3-123">Pode ser um email do usuário, ID do aplicativo ou nome do grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="cb0a3-124">-Princípiostype</span><span class="sxs-lookup"><span data-stu-id="cb0a3-124">-PrincipalType</span></span>
<span data-ttu-id="cb0a3-125">Tipo de entidade.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-125">Principal type.</span></span>

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

### <span data-ttu-id="cb0a3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb0a3-126">-ResourceGroupName</span></span>
<span data-ttu-id="cb0a3-127">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cb0a3-128">-Função</span><span class="sxs-lookup"><span data-stu-id="cb0a3-128">-Role</span></span>
<span data-ttu-id="cb0a3-129">Função de entidade de segurança de cluster.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="cb0a3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb0a3-130">-SubscriptionId</span></span>
<span data-ttu-id="cb0a3-131">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cb0a3-132">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cb0a3-133">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="cb0a3-133">-TenantId</span></span>
<span data-ttu-id="cb0a3-134">A ID do locatário do principal</span><span class="sxs-lookup"><span data-stu-id="cb0a3-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="cb0a3-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cb0a3-135">-Confirm</span></span>
<span data-ttu-id="cb0a3-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb0a3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb0a3-137">-WhatIf</span></span>
<span data-ttu-id="cb0a3-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb0a3-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb0a3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0a3-140">CommonParameters</span></span>
<span data-ttu-id="cb0a3-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb0a3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0a3-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb0a3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0a3-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb0a3-143">INPUTS</span></span>

## <span data-ttu-id="cb0a3-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb0a3-144">OUTPUTS</span></span>

### <span data-ttu-id="cb0a3-145">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="cb0a3-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="cb0a3-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb0a3-146">NOTES</span></span>

<span data-ttu-id="cb0a3-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cb0a3-147">ALIASES</span></span>

## <span data-ttu-id="cb0a3-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb0a3-148">RELATED LINKS</span></span>

