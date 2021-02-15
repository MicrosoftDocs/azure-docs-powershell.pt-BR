---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111922"
---
# <span data-ttu-id="f5114-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="f5114-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="f5114-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5114-102">SYNOPSIS</span></span>
<span data-ttu-id="f5114-103">Exclui o vNetPeering do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f5114-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="f5114-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5114-104">SYNTAX</span></span>

### <span data-ttu-id="f5114-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f5114-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f5114-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f5114-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f5114-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5114-107">DESCRIPTION</span></span>
<span data-ttu-id="f5114-108">Exclui o vNetPeering do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f5114-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="f5114-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5114-109">EXAMPLES</span></span>

### <span data-ttu-id="f5114-110">Exemplo 1: Remover um par de vnet de databções por nome</span><span class="sxs-lookup"><span data-stu-id="f5114-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="f5114-111">Este comando remove um par de vnet de databções por nome</span><span class="sxs-lookup"><span data-stu-id="f5114-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="f5114-112">Exemplo 2: Remover um par de vnet de databções por objeto</span><span class="sxs-lookup"><span data-stu-id="f5114-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="f5114-113">Este comando remove um par de vnet de databções por objeto</span><span class="sxs-lookup"><span data-stu-id="f5114-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="f5114-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5114-114">PARAMETERS</span></span>

### <span data-ttu-id="f5114-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5114-115">-AsJob</span></span>
<span data-ttu-id="f5114-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f5114-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f5114-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5114-117">-DefaultProfile</span></span>
<span data-ttu-id="f5114-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5114-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5114-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5114-119">-InputObject</span></span>
<span data-ttu-id="f5114-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="f5114-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f5114-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5114-121">-Name</span></span>
<span data-ttu-id="f5114-122">O nome do paring vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f5114-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="f5114-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f5114-123">-NoWait</span></span>
<span data-ttu-id="f5114-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="f5114-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f5114-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5114-125">-PassThru</span></span>
<span data-ttu-id="f5114-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f5114-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f5114-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5114-127">-ResourceGroupName</span></span>
<span data-ttu-id="f5114-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5114-128">The name of the resource group.</span></span>
<span data-ttu-id="f5114-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f5114-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f5114-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5114-130">-SubscriptionId</span></span>
<span data-ttu-id="f5114-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f5114-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f5114-132">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="f5114-132">-WorkspaceName</span></span>
<span data-ttu-id="f5114-133">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f5114-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="f5114-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f5114-134">-Confirm</span></span>
<span data-ttu-id="f5114-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5114-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5114-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5114-136">-WhatIf</span></span>
<span data-ttu-id="f5114-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f5114-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5114-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5114-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5114-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5114-139">CommonParameters</span></span>
<span data-ttu-id="f5114-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5114-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5114-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5114-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5114-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="f5114-142">INPUTS</span></span>

### <span data-ttu-id="f5114-143">Microsoft.Azure.PowerShell.Cmdlets.Databndezs.Models.IDatabtabçõesIdentity</span><span class="sxs-lookup"><span data-stu-id="f5114-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="f5114-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="f5114-144">OUTPUTS</span></span>

### <span data-ttu-id="f5114-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f5114-145">System.Boolean</span></span>

## <span data-ttu-id="f5114-146">Notas</span><span class="sxs-lookup"><span data-stu-id="f5114-146">NOTES</span></span>

<span data-ttu-id="f5114-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="f5114-147">ALIASES</span></span>

<span data-ttu-id="f5114-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="f5114-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f5114-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f5114-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5114-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f5114-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f5114-151">INPUTOBJECT: <IDatabricksIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="f5114-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5114-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="f5114-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5114-153">`[PeeringName <String>]`: o nome do pario vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f5114-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="f5114-154">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5114-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f5114-155">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f5114-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="f5114-156">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="f5114-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f5114-157">`[WorkspaceName <String>]`: o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f5114-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="f5114-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5114-158">RELATED LINKS</span></span>

