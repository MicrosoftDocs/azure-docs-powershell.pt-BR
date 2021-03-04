---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: c8e63bd0a6496b1c0ce0899f0e183fb10db32a7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886665"
---
# <span data-ttu-id="23d24-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="23d24-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="23d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23d24-102">SYNOPSIS</span></span>
<span data-ttu-id="23d24-103">Exclui o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="23d24-103">Deletes the workspace.</span></span>

## <span data-ttu-id="23d24-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="23d24-104">SYNTAX</span></span>

### <span data-ttu-id="23d24-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="23d24-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="23d24-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="23d24-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="23d24-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="23d24-107">DESCRIPTION</span></span>
<span data-ttu-id="23d24-108">Exclui o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="23d24-108">Deletes the workspace.</span></span>

## <span data-ttu-id="23d24-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23d24-109">EXAMPLES</span></span>

### <span data-ttu-id="23d24-110">Exemplo 1: Remover um espaço de trabalho Databricks</span><span class="sxs-lookup"><span data-stu-id="23d24-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="23d24-111">Este comando remove um espaço de trabalho Databricks de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23d24-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="23d24-112">Exemplo 2: Remover um espaço de trabalho Databricks por objeto</span><span class="sxs-lookup"><span data-stu-id="23d24-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="23d24-113">Este comando remove um espaço de trabalho Databricks de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23d24-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="23d24-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="23d24-114">PARAMETERS</span></span>

### <span data-ttu-id="23d24-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23d24-115">-AsJob</span></span>
<span data-ttu-id="23d24-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="23d24-116">Run the command as a job</span></span>

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

### <span data-ttu-id="23d24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d24-117">-DefaultProfile</span></span>
<span data-ttu-id="23d24-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23d24-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23d24-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23d24-119">-InputObject</span></span>
<span data-ttu-id="23d24-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="23d24-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23d24-121">-Name</span><span class="sxs-lookup"><span data-stu-id="23d24-121">-Name</span></span>
<span data-ttu-id="23d24-122">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="23d24-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d24-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="23d24-123">-NoWait</span></span>
<span data-ttu-id="23d24-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="23d24-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="23d24-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23d24-125">-PassThru</span></span>
<span data-ttu-id="23d24-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="23d24-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="23d24-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d24-127">-ResourceGroupName</span></span>
<span data-ttu-id="23d24-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23d24-128">The name of the resource group.</span></span>
<span data-ttu-id="23d24-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="23d24-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d24-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23d24-130">-SubscriptionId</span></span>
<span data-ttu-id="23d24-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="23d24-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d24-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23d24-132">-Confirm</span></span>
<span data-ttu-id="23d24-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23d24-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23d24-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d24-134">-WhatIf</span></span>
<span data-ttu-id="23d24-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23d24-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23d24-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23d24-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23d24-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d24-137">CommonParameters</span></span>
<span data-ttu-id="23d24-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d24-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d24-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23d24-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d24-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23d24-140">INPUTS</span></span>

### <span data-ttu-id="23d24-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="23d24-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="23d24-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="23d24-142">OUTPUTS</span></span>

### <span data-ttu-id="23d24-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="23d24-143">System.Boolean</span></span>

## <span data-ttu-id="23d24-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="23d24-144">NOTES</span></span>

<span data-ttu-id="23d24-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="23d24-145">ALIASES</span></span>

<span data-ttu-id="23d24-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="23d24-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="23d24-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="23d24-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23d24-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23d24-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="23d24-149">INPUTOBJECT <IDatabricksIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="23d24-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23d24-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="23d24-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23d24-151">`[PeeringName <String>]`: O nome do paring vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="23d24-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="23d24-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23d24-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="23d24-153">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="23d24-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="23d24-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="23d24-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="23d24-155">`[WorkspaceName <String>]`: O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="23d24-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="23d24-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23d24-156">RELATED LINKS</span></span>

