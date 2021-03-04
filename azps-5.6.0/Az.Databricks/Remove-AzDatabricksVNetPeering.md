---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 986bea9de45ea8a628cea8eda4d8a63ec74d46fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888981"
---
# <span data-ttu-id="85115-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="85115-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="85115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85115-102">SYNOPSIS</span></span>
<span data-ttu-id="85115-103">Exclui o vNetPeering do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="85115-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="85115-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="85115-104">SYNTAX</span></span>

### <span data-ttu-id="85115-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="85115-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="85115-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="85115-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="85115-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="85115-107">DESCRIPTION</span></span>
<span data-ttu-id="85115-108">Exclui o vNetPeering do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="85115-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="85115-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85115-109">EXAMPLES</span></span>

### <span data-ttu-id="85115-110">Exemplo 1: Remover um par de vnet de databricks pelo nome</span><span class="sxs-lookup"><span data-stu-id="85115-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="85115-111">Este comando remove um par de vnet de databricks pelo nome</span><span class="sxs-lookup"><span data-stu-id="85115-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="85115-112">Exemplo 2: Remover um par de vnet de databricks por objeto</span><span class="sxs-lookup"><span data-stu-id="85115-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="85115-113">Este comando remove um par de vnet de databricks por objeto</span><span class="sxs-lookup"><span data-stu-id="85115-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="85115-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="85115-114">PARAMETERS</span></span>

### <span data-ttu-id="85115-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85115-115">-AsJob</span></span>
<span data-ttu-id="85115-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="85115-116">Run the command as a job</span></span>

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

### <span data-ttu-id="85115-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85115-117">-DefaultProfile</span></span>
<span data-ttu-id="85115-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85115-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85115-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85115-119">-InputObject</span></span>
<span data-ttu-id="85115-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="85115-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="85115-121">-Name</span><span class="sxs-lookup"><span data-stu-id="85115-121">-Name</span></span>
<span data-ttu-id="85115-122">O nome do paring vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="85115-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="85115-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="85115-123">-NoWait</span></span>
<span data-ttu-id="85115-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="85115-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="85115-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85115-125">-PassThru</span></span>
<span data-ttu-id="85115-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="85115-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="85115-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85115-127">-ResourceGroupName</span></span>
<span data-ttu-id="85115-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85115-128">The name of the resource group.</span></span>
<span data-ttu-id="85115-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85115-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="85115-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85115-130">-SubscriptionId</span></span>
<span data-ttu-id="85115-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="85115-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="85115-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="85115-132">-WorkspaceName</span></span>
<span data-ttu-id="85115-133">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="85115-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="85115-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85115-134">-Confirm</span></span>
<span data-ttu-id="85115-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85115-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85115-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85115-136">-WhatIf</span></span>
<span data-ttu-id="85115-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85115-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85115-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85115-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85115-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85115-139">CommonParameters</span></span>
<span data-ttu-id="85115-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85115-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85115-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85115-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85115-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85115-142">INPUTS</span></span>

### <span data-ttu-id="85115-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="85115-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="85115-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="85115-144">OUTPUTS</span></span>

### <span data-ttu-id="85115-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85115-145">System.Boolean</span></span>

## <span data-ttu-id="85115-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="85115-146">NOTES</span></span>

<span data-ttu-id="85115-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="85115-147">ALIASES</span></span>

<span data-ttu-id="85115-148">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="85115-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="85115-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="85115-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85115-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="85115-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="85115-151">INPUTOBJECT <IDatabricksIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="85115-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="85115-152">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="85115-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="85115-153">`[PeeringName <String>]`: O nome do paring vNet do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="85115-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="85115-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85115-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="85115-155">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85115-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="85115-156">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="85115-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="85115-157">`[WorkspaceName <String>]`: O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="85115-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="85115-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85115-158">RELATED LINKS</span></span>

