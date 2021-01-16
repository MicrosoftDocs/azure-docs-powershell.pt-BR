---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 8f2a0cd576c3fe7f184d3f016f6666aa8749b5c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258872"
---
# <span data-ttu-id="99046-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="99046-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="99046-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99046-102">SYNOPSIS</span></span>
<span data-ttu-id="99046-103">Crie um Kusto de cluster de principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="99046-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="99046-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99046-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99046-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99046-105">DESCRIPTION</span></span>
<span data-ttu-id="99046-106">Crie um Kusto de cluster de principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="99046-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="99046-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99046-107">EXAMPLES</span></span>

### <span data-ttu-id="99046-108">Exemplo 1: criar um cluster de Kusto de principalAssignment</span><span class="sxs-lookup"><span data-stu-id="99046-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="99046-109">O comando acima cria um cluster de Kusto de principalAssignment</span><span class="sxs-lookup"><span data-stu-id="99046-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="99046-110">OS</span><span class="sxs-lookup"><span data-stu-id="99046-110">PARAMETERS</span></span>

### <span data-ttu-id="99046-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99046-111">-AsJob</span></span>
<span data-ttu-id="99046-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="99046-112">Run the command as a job</span></span>

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

### <span data-ttu-id="99046-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="99046-113">-ClusterName</span></span>
<span data-ttu-id="99046-114">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="99046-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="99046-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99046-115">-DefaultProfile</span></span>
<span data-ttu-id="99046-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99046-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99046-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="99046-117">-NoWait</span></span>
<span data-ttu-id="99046-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="99046-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="99046-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="99046-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="99046-120">O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="99046-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="99046-121">-Entidade de segurança</span><span class="sxs-lookup"><span data-stu-id="99046-121">-PrincipalId</span></span>
<span data-ttu-id="99046-122">A ID da entidade de segurança atribuída à entidade de segurança do grupo.</span><span class="sxs-lookup"><span data-stu-id="99046-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="99046-123">Pode ser um email do usuário, ID do aplicativo ou nome do grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="99046-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="99046-124">-Princípiostype</span><span class="sxs-lookup"><span data-stu-id="99046-124">-PrincipalType</span></span>
<span data-ttu-id="99046-125">Tipo de entidade.</span><span class="sxs-lookup"><span data-stu-id="99046-125">Principal type.</span></span>

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

### <span data-ttu-id="99046-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99046-126">-ResourceGroupName</span></span>
<span data-ttu-id="99046-127">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="99046-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="99046-128">-Função</span><span class="sxs-lookup"><span data-stu-id="99046-128">-Role</span></span>
<span data-ttu-id="99046-129">Função de entidade de segurança de cluster.</span><span class="sxs-lookup"><span data-stu-id="99046-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="99046-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99046-130">-SubscriptionId</span></span>
<span data-ttu-id="99046-131">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="99046-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="99046-132">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="99046-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="99046-133">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="99046-133">-TenantId</span></span>
<span data-ttu-id="99046-134">A ID do locatário do principal</span><span class="sxs-lookup"><span data-stu-id="99046-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="99046-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="99046-135">-Confirm</span></span>
<span data-ttu-id="99046-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99046-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99046-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99046-137">-WhatIf</span></span>
<span data-ttu-id="99046-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99046-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99046-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99046-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99046-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99046-140">CommonParameters</span></span>
<span data-ttu-id="99046-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99046-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99046-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99046-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99046-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99046-143">INPUTS</span></span>

## <span data-ttu-id="99046-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99046-144">OUTPUTS</span></span>

### <span data-ttu-id="99046-145">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="99046-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="99046-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99046-146">NOTES</span></span>

<span data-ttu-id="99046-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="99046-147">ALIASES</span></span>

## <span data-ttu-id="99046-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99046-148">RELATED LINKS</span></span>

