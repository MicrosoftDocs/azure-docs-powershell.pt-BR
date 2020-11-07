---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947809"
---
# <span data-ttu-id="de38e-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="de38e-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="de38e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de38e-102">SYNOPSIS</span></span>
<span data-ttu-id="de38e-103">Exclui o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="de38e-103">Deletes the workspace.</span></span>

## <span data-ttu-id="de38e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de38e-104">SYNTAX</span></span>

### <span data-ttu-id="de38e-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="de38e-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="de38e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="de38e-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="de38e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de38e-107">DESCRIPTION</span></span>
<span data-ttu-id="de38e-108">Exclui o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="de38e-108">Deletes the workspace.</span></span>

## <span data-ttu-id="de38e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de38e-109">EXAMPLES</span></span>

### <span data-ttu-id="de38e-110">Exemplo 1: remover um espaço de trabalho databricks</span><span class="sxs-lookup"><span data-stu-id="de38e-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="de38e-111">Esse comando Remove um espaço de trabalho databricks de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de38e-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="de38e-112">Exemplo 2: remover um espaço de trabalho databricks por objeto</span><span class="sxs-lookup"><span data-stu-id="de38e-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="de38e-113">Esse comando Remove um espaço de trabalho databricks de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de38e-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="de38e-114">OS</span><span class="sxs-lookup"><span data-stu-id="de38e-114">PARAMETERS</span></span>

### <span data-ttu-id="de38e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de38e-115">-AsJob</span></span>
<span data-ttu-id="de38e-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="de38e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="de38e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de38e-117">-DefaultProfile</span></span>
<span data-ttu-id="de38e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de38e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de38e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de38e-119">-InputObject</span></span>
<span data-ttu-id="de38e-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="de38e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="de38e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="de38e-121">-Name</span></span>
<span data-ttu-id="de38e-122">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="de38e-122">The name of the workspace.</span></span>

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

### <span data-ttu-id="de38e-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="de38e-123">-NoWait</span></span>
<span data-ttu-id="de38e-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="de38e-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="de38e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de38e-125">-PassThru</span></span>
<span data-ttu-id="de38e-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="de38e-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="de38e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de38e-127">-ResourceGroupName</span></span>
<span data-ttu-id="de38e-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de38e-128">The name of the resource group.</span></span>
<span data-ttu-id="de38e-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="de38e-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="de38e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de38e-130">-SubscriptionId</span></span>
<span data-ttu-id="de38e-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="de38e-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="de38e-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="de38e-132">-Confirm</span></span>
<span data-ttu-id="de38e-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de38e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de38e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de38e-134">-WhatIf</span></span>
<span data-ttu-id="de38e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de38e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de38e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de38e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de38e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de38e-137">CommonParameters</span></span>
<span data-ttu-id="de38e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de38e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de38e-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de38e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de38e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de38e-140">INPUTS</span></span>

### <span data-ttu-id="de38e-141">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="de38e-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="de38e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de38e-142">OUTPUTS</span></span>

### <span data-ttu-id="de38e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de38e-143">System.Boolean</span></span>

## <span data-ttu-id="de38e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de38e-144">NOTES</span></span>

<span data-ttu-id="de38e-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="de38e-145">ALIASES</span></span>

<span data-ttu-id="de38e-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="de38e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="de38e-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="de38e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="de38e-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="de38e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="de38e-149">INPUTobject <IDatabricksIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="de38e-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="de38e-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="de38e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="de38e-151">`[PeeringName <String>]`: O nome do emparelhamento da vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="de38e-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="de38e-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de38e-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="de38e-153">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="de38e-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="de38e-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="de38e-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="de38e-155">`[WorkspaceName <String>]`: O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="de38e-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="de38e-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de38e-156">RELATED LINKS</span></span>

