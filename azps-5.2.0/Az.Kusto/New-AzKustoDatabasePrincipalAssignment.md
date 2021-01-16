---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 8bfcb3a96ee8db53a6a869a01441739ee9c503bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264374"
---
# <span data-ttu-id="5f8a0-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="5f8a0-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="5f8a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8a0-103">Cria um banco de dados de cluster Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="5f8a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f8a0-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5f8a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f8a0-105">DESCRIPTION</span></span>
<span data-ttu-id="5f8a0-106">Cria um banco de dados de cluster Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="5f8a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f8a0-107">EXAMPLES</span></span>

### <span data-ttu-id="5f8a0-108">Exemplo 1: criar um banco de dados de cluster Kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="5f8a0-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="5f8a0-109">O comando acima cria um banco de dados de cluster Kusto principalAssignment</span><span class="sxs-lookup"><span data-stu-id="5f8a0-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="5f8a0-110">OS</span><span class="sxs-lookup"><span data-stu-id="5f8a0-110">PARAMETERS</span></span>

### <span data-ttu-id="5f8a0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f8a0-111">-AsJob</span></span>
<span data-ttu-id="5f8a0-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="5f8a0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5f8a0-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5f8a0-113">-ClusterName</span></span>
<span data-ttu-id="5f8a0-114">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5f8a0-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5f8a0-115">-DatabaseName</span></span>
<span data-ttu-id="5f8a0-116">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="5f8a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f8a0-117">-DefaultProfile</span></span>
<span data-ttu-id="5f8a0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f8a0-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5f8a0-119">-NoWait</span></span>
<span data-ttu-id="5f8a0-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="5f8a0-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5f8a0-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="5f8a0-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="5f8a0-122">O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="5f8a0-123">-Entidade de segurança</span><span class="sxs-lookup"><span data-stu-id="5f8a0-123">-PrincipalId</span></span>
<span data-ttu-id="5f8a0-124">A ID da entidade de segurança atribuída à entidade do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="5f8a0-125">Pode ser um email do usuário, ID do aplicativo ou nome do grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="5f8a0-126">-Princípiostype</span><span class="sxs-lookup"><span data-stu-id="5f8a0-126">-PrincipalType</span></span>
<span data-ttu-id="5f8a0-127">Tipo de entidade.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-127">Principal type.</span></span>

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

### <span data-ttu-id="5f8a0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f8a0-128">-ResourceGroupName</span></span>
<span data-ttu-id="5f8a0-129">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5f8a0-130">-Função</span><span class="sxs-lookup"><span data-stu-id="5f8a0-130">-Role</span></span>
<span data-ttu-id="5f8a0-131">Função de entidade do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-131">Database principal role.</span></span>

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

### <span data-ttu-id="5f8a0-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f8a0-132">-SubscriptionId</span></span>
<span data-ttu-id="5f8a0-133">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5f8a0-134">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5f8a0-135">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="5f8a0-135">-TenantId</span></span>
<span data-ttu-id="5f8a0-136">A ID do locatário do principal</span><span class="sxs-lookup"><span data-stu-id="5f8a0-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="5f8a0-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5f8a0-137">-Confirm</span></span>
<span data-ttu-id="5f8a0-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f8a0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f8a0-139">-WhatIf</span></span>
<span data-ttu-id="5f8a0-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f8a0-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f8a0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8a0-142">CommonParameters</span></span>
<span data-ttu-id="5f8a0-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f8a0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8a0-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f8a0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8a0-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f8a0-145">INPUTS</span></span>

## <span data-ttu-id="5f8a0-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f8a0-146">OUTPUTS</span></span>

### <span data-ttu-id="5f8a0-147">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="5f8a0-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="5f8a0-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f8a0-148">NOTES</span></span>

<span data-ttu-id="5f8a0-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5f8a0-149">ALIASES</span></span>

## <span data-ttu-id="5f8a0-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f8a0-150">RELATED LINKS</span></span>

