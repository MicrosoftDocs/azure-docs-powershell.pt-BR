---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111920"
---
# <span data-ttu-id="a6fb4-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6fb4-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="a6fb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="a6fb4-103">Exclui o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-103">Deletes the workspace.</span></span>

## <span data-ttu-id="a6fb4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6fb4-104">SYNTAX</span></span>

### <span data-ttu-id="a6fb4-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a6fb4-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6fb4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a6fb4-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6fb4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6fb4-107">DESCRIPTION</span></span>
<span data-ttu-id="a6fb4-108">Exclui o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-108">Deletes the workspace.</span></span>

## <span data-ttu-id="a6fb4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a6fb4-109">EXAMPLES</span></span>

### <span data-ttu-id="a6fb4-110">Exemplo 1: Remover um espaço de trabalho Datab sérvios</span><span class="sxs-lookup"><span data-stu-id="a6fb4-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="a6fb4-111">Esse comando remove um espaço de trabalho Databções de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="a6fb4-112">Exemplo 2: Remover um espaço de trabalho Databéticos por objeto</span><span class="sxs-lookup"><span data-stu-id="a6fb4-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="a6fb4-113">Esse comando remove um espaço de trabalho Databções de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="a6fb4-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6fb4-114">PARAMETERS</span></span>

### <span data-ttu-id="a6fb4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6fb4-115">-AsJob</span></span>
<span data-ttu-id="a6fb4-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a6fb4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a6fb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6fb4-117">-DefaultProfile</span></span>
<span data-ttu-id="a6fb4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6fb4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6fb4-119">-InputObject</span></span>
<span data-ttu-id="a6fb4-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a6fb4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6fb4-121">-Name</span></span>
<span data-ttu-id="a6fb4-122">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-122">The name of the workspace.</span></span>

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

### <span data-ttu-id="a6fb4-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a6fb4-123">-NoWait</span></span>
<span data-ttu-id="a6fb4-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="a6fb4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a6fb4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6fb4-125">-PassThru</span></span>
<span data-ttu-id="a6fb4-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a6fb4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a6fb4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6fb4-127">-ResourceGroupName</span></span>
<span data-ttu-id="a6fb4-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-128">The name of the resource group.</span></span>
<span data-ttu-id="a6fb4-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a6fb4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6fb4-130">-SubscriptionId</span></span>
<span data-ttu-id="a6fb4-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a6fb4-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a6fb4-132">-Confirm</span></span>
<span data-ttu-id="a6fb4-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6fb4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6fb4-134">-WhatIf</span></span>
<span data-ttu-id="a6fb4-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6fb4-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6fb4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6fb4-137">CommonParameters</span></span>
<span data-ttu-id="a6fb4-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6fb4-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6fb4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6fb4-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="a6fb4-140">INPUTS</span></span>

### <span data-ttu-id="a6fb4-141">Microsoft.Azure.PowerShell.Cmdlets.Databndezs.Models.IDatabtabçõesIdentity</span><span class="sxs-lookup"><span data-stu-id="a6fb4-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="a6fb4-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="a6fb4-142">OUTPUTS</span></span>

### <span data-ttu-id="a6fb4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6fb4-143">System.Boolean</span></span>

## <span data-ttu-id="a6fb4-144">Notas</span><span class="sxs-lookup"><span data-stu-id="a6fb4-144">NOTES</span></span>

<span data-ttu-id="a6fb4-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="a6fb4-145">ALIASES</span></span>

<span data-ttu-id="a6fb4-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="a6fb4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6fb4-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6fb4-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6fb4-149">INPUTOBJECT: <IDatabricksIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="a6fb4-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6fb4-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="a6fb4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6fb4-151">`[PeeringName <String>]`: o nome do pario vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="a6fb4-152">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a6fb4-153">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="a6fb4-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a6fb4-155">`[WorkspaceName <String>]`: o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6fb4-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="a6fb4-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6fb4-156">RELATED LINKS</span></span>

