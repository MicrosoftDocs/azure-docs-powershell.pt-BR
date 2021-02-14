---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 3fc5c493f94b6da371a4249479e397ea6e2362f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110825"
---
# <span data-ttu-id="e05aa-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="e05aa-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="e05aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e05aa-102">SYNOPSIS</span></span>
<span data-ttu-id="e05aa-103">Excluir uma consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="e05aa-103">Delete a graph query.</span></span>

## <span data-ttu-id="e05aa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e05aa-104">SYNTAX</span></span>

### <span data-ttu-id="e05aa-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e05aa-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e05aa-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e05aa-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e05aa-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e05aa-107">DESCRIPTION</span></span>
<span data-ttu-id="e05aa-108">Excluir uma consulta gráfica.</span><span class="sxs-lookup"><span data-stu-id="e05aa-108">Delete a graph query.</span></span>

## <span data-ttu-id="e05aa-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e05aa-109">EXAMPLES</span></span>

### <span data-ttu-id="e05aa-110">Exemplo 1: Remover uma consulta de gráfico de recursos por nome</span><span class="sxs-lookup"><span data-stu-id="e05aa-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="e05aa-111">Esse comando remove uma consulta de gráfico de recursos por nome.</span><span class="sxs-lookup"><span data-stu-id="e05aa-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="e05aa-112">Exemplo 2: Remover uma consulta de gráfico de recursos por objeto</span><span class="sxs-lookup"><span data-stu-id="e05aa-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="e05aa-113">Esse comando remove uma consulta de gráfico de recursos por objeto.</span><span class="sxs-lookup"><span data-stu-id="e05aa-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="e05aa-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e05aa-114">PARAMETERS</span></span>

### <span data-ttu-id="e05aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05aa-115">-DefaultProfile</span></span>
<span data-ttu-id="e05aa-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e05aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e05aa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e05aa-117">-InputObject</span></span>
<span data-ttu-id="e05aa-118">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="e05aa-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e05aa-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e05aa-119">-Name</span></span>
<span data-ttu-id="e05aa-120">O nome do recurso Consulta gráfica.</span><span class="sxs-lookup"><span data-stu-id="e05aa-120">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="e05aa-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e05aa-121">-PassThru</span></span>
<span data-ttu-id="e05aa-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e05aa-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e05aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e05aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="e05aa-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e05aa-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="e05aa-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e05aa-125">-SubscriptionId</span></span>
<span data-ttu-id="e05aa-126">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e05aa-126">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="e05aa-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e05aa-127">-Confirm</span></span>
<span data-ttu-id="e05aa-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e05aa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e05aa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e05aa-129">-WhatIf</span></span>
<span data-ttu-id="e05aa-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e05aa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e05aa-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e05aa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e05aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05aa-132">CommonParameters</span></span>
<span data-ttu-id="e05aa-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05aa-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e05aa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05aa-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="e05aa-135">INPUTS</span></span>

### <span data-ttu-id="e05aa-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="e05aa-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="e05aa-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="e05aa-137">OUTPUTS</span></span>

### <span data-ttu-id="e05aa-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e05aa-138">System.Boolean</span></span>

## <span data-ttu-id="e05aa-139">Notas</span><span class="sxs-lookup"><span data-stu-id="e05aa-139">NOTES</span></span>

<span data-ttu-id="e05aa-140">Aliases</span><span class="sxs-lookup"><span data-stu-id="e05aa-140">ALIASES</span></span>

<span data-ttu-id="e05aa-141">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="e05aa-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e05aa-142">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e05aa-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e05aa-143">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e05aa-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e05aa-144">INPUTOBJECT: <IResourceGraphIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="e05aa-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e05aa-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="e05aa-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e05aa-146">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e05aa-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e05aa-147">`[ResourceName <String>]`: o nome do recurso Consulta do Gráfico.</span><span class="sxs-lookup"><span data-stu-id="e05aa-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="e05aa-148">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e05aa-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="e05aa-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e05aa-149">RELATED LINKS</span></span>

