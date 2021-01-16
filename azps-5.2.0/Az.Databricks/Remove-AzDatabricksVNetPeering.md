---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259158"
---
# <span data-ttu-id="088e7-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="088e7-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="088e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="088e7-102">SYNOPSIS</span></span>
<span data-ttu-id="088e7-103">Exclui a vNetPeering do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="088e7-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="088e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="088e7-104">SYNTAX</span></span>

### <span data-ttu-id="088e7-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="088e7-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="088e7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="088e7-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="088e7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="088e7-107">DESCRIPTION</span></span>
<span data-ttu-id="088e7-108">Exclui a vNetPeering do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="088e7-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="088e7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="088e7-109">EXAMPLES</span></span>

### <span data-ttu-id="088e7-110">Exemplo 1: remover um emparelhamento via rede virtual de Bricks por nome</span><span class="sxs-lookup"><span data-stu-id="088e7-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="088e7-111">Esse comando Remove um emparelhamento de rede virtual de Bricks por nome</span><span class="sxs-lookup"><span data-stu-id="088e7-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="088e7-112">Exemplo 2: remover um emparelhamento via rede virtual de Bricks por objeto</span><span class="sxs-lookup"><span data-stu-id="088e7-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="088e7-113">Esse comando Remove um emparelhamento de rede virtual de Bricks por objeto</span><span class="sxs-lookup"><span data-stu-id="088e7-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="088e7-114">OS</span><span class="sxs-lookup"><span data-stu-id="088e7-114">PARAMETERS</span></span>

### <span data-ttu-id="088e7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="088e7-115">-AsJob</span></span>
<span data-ttu-id="088e7-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="088e7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="088e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="088e7-117">-DefaultProfile</span></span>
<span data-ttu-id="088e7-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="088e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="088e7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="088e7-119">-InputObject</span></span>
<span data-ttu-id="088e7-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="088e7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="088e7-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="088e7-121">-Name</span></span>
<span data-ttu-id="088e7-122">O nome do emparelhamento da vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="088e7-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="088e7-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="088e7-123">-NoWait</span></span>
<span data-ttu-id="088e7-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="088e7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="088e7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="088e7-125">-PassThru</span></span>
<span data-ttu-id="088e7-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="088e7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="088e7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="088e7-127">-ResourceGroupName</span></span>
<span data-ttu-id="088e7-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="088e7-128">The name of the resource group.</span></span>
<span data-ttu-id="088e7-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="088e7-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="088e7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="088e7-130">-SubscriptionId</span></span>
<span data-ttu-id="088e7-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="088e7-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="088e7-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="088e7-132">-WorkspaceName</span></span>
<span data-ttu-id="088e7-133">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="088e7-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="088e7-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="088e7-134">-Confirm</span></span>
<span data-ttu-id="088e7-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="088e7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="088e7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="088e7-136">-WhatIf</span></span>
<span data-ttu-id="088e7-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="088e7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="088e7-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="088e7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="088e7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="088e7-139">CommonParameters</span></span>
<span data-ttu-id="088e7-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="088e7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="088e7-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="088e7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="088e7-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="088e7-142">INPUTS</span></span>

### <span data-ttu-id="088e7-143">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="088e7-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="088e7-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="088e7-144">OUTPUTS</span></span>

### <span data-ttu-id="088e7-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="088e7-145">System.Boolean</span></span>

## <span data-ttu-id="088e7-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="088e7-146">NOTES</span></span>

<span data-ttu-id="088e7-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="088e7-147">ALIASES</span></span>

<span data-ttu-id="088e7-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="088e7-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="088e7-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="088e7-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="088e7-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="088e7-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="088e7-151">INPUTobject <IDatabricksIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="088e7-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="088e7-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="088e7-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="088e7-153">`[PeeringName <String>]`: O nome do emparelhamento da vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="088e7-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="088e7-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="088e7-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="088e7-155">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="088e7-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="088e7-156">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="088e7-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="088e7-157">`[WorkspaceName <String>]`: O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="088e7-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="088e7-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="088e7-158">RELATED LINKS</span></span>

