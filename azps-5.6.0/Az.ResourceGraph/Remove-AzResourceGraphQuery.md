---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 0253a5fa7cf5ff13c678eb0a6d86c31335239fdb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891666"
---
# <span data-ttu-id="ae1ca-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="ae1ca-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="ae1ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1ca-103">Exclua uma consulta gráfica.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-103">Delete a graph query.</span></span>

## <span data-ttu-id="ae1ca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae1ca-104">SYNTAX</span></span>

### <span data-ttu-id="ae1ca-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ae1ca-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ae1ca-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ae1ca-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae1ca-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae1ca-107">DESCRIPTION</span></span>
<span data-ttu-id="ae1ca-108">Exclua uma consulta gráfica.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-108">Delete a graph query.</span></span>

## <span data-ttu-id="ae1ca-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae1ca-109">EXAMPLES</span></span>

### <span data-ttu-id="ae1ca-110">Exemplo 1: Remover uma consulta de gráfico de recursos pelo nome</span><span class="sxs-lookup"><span data-stu-id="ae1ca-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="ae1ca-111">Este comando remove uma consulta de gráfico de recursos pelo nome.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="ae1ca-112">Exemplo 2: Remover uma consulta de gráfico de recursos por objeto</span><span class="sxs-lookup"><span data-stu-id="ae1ca-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="ae1ca-113">Este comando remove uma consulta de gráfico de recursos por objeto.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="ae1ca-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae1ca-114">PARAMETERS</span></span>

### <span data-ttu-id="ae1ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae1ca-115">-DefaultProfile</span></span>
<span data-ttu-id="ae1ca-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae1ca-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae1ca-117">-InputObject</span></span>
<span data-ttu-id="ae1ca-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1ca-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ae1ca-119">-Name</span></span>
<span data-ttu-id="ae1ca-120">O nome do recurso Consulta do Graph.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-120">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="ae1ca-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae1ca-121">-PassThru</span></span>
<span data-ttu-id="ae1ca-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="ae1ca-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ae1ca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae1ca-123">-ResourceGroupName</span></span>
<span data-ttu-id="ae1ca-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ae1ca-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae1ca-125">-SubscriptionId</span></span>
<span data-ttu-id="ae1ca-126">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-126">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="ae1ca-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae1ca-127">-Confirm</span></span>
<span data-ttu-id="ae1ca-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae1ca-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae1ca-129">-WhatIf</span></span>
<span data-ttu-id="ae1ca-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae1ca-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae1ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1ca-132">CommonParameters</span></span>
<span data-ttu-id="ae1ca-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1ca-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae1ca-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1ca-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae1ca-135">INPUTS</span></span>

### <span data-ttu-id="ae1ca-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="ae1ca-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="ae1ca-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae1ca-137">OUTPUTS</span></span>

### <span data-ttu-id="ae1ca-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae1ca-138">System.Boolean</span></span>

## <span data-ttu-id="ae1ca-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae1ca-139">NOTES</span></span>

<span data-ttu-id="ae1ca-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ae1ca-140">ALIASES</span></span>

<span data-ttu-id="ae1ca-141">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="ae1ca-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae1ca-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae1ca-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae1ca-144">INPUTOBJECT <IResourceGraphIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="ae1ca-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ae1ca-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ae1ca-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ae1ca-146">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ae1ca-147">`[ResourceName <String>]`: O nome do recurso Consulta do Graph.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="ae1ca-148">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1ca-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="ae1ca-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae1ca-149">RELATED LINKS</span></span>

