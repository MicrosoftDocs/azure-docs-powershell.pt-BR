---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 3fc5c493f94b6da371a4249479e397ea6e2362f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271566"
---
# <span data-ttu-id="bbd7b-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="bbd7b-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="bbd7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbd7b-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd7b-103">Excluir uma consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-103">Delete a graph query.</span></span>

## <span data-ttu-id="bbd7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbd7b-104">SYNTAX</span></span>

### <span data-ttu-id="bbd7b-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="bbd7b-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bbd7b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bbd7b-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bbd7b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bbd7b-107">DESCRIPTION</span></span>
<span data-ttu-id="bbd7b-108">Excluir uma consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-108">Delete a graph query.</span></span>

## <span data-ttu-id="bbd7b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbd7b-109">EXAMPLES</span></span>

### <span data-ttu-id="bbd7b-110">Exemplo 1: remover uma consulta de gráfico de recursos por nome</span><span class="sxs-lookup"><span data-stu-id="bbd7b-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="bbd7b-111">Esse comando Remove uma consulta de gráfico de recursos por nome.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="bbd7b-112">Exemplo 2: remover uma consulta de gráfico de recursos por objeto</span><span class="sxs-lookup"><span data-stu-id="bbd7b-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="bbd7b-113">Esse comando Remove uma consulta de gráfico de recursos por objeto.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="bbd7b-114">OS</span><span class="sxs-lookup"><span data-stu-id="bbd7b-114">PARAMETERS</span></span>

### <span data-ttu-id="bbd7b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd7b-115">-DefaultProfile</span></span>
<span data-ttu-id="bbd7b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbd7b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbd7b-117">-InputObject</span></span>
<span data-ttu-id="bbd7b-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bbd7b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbd7b-119">-Name</span></span>
<span data-ttu-id="bbd7b-120">O nome do recurso de consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-120">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="bbd7b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbd7b-121">-PassThru</span></span>
<span data-ttu-id="bbd7b-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="bbd7b-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bbd7b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd7b-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbd7b-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="bbd7b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbd7b-125">-SubscriptionId</span></span>
<span data-ttu-id="bbd7b-126">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-126">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="bbd7b-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bbd7b-127">-Confirm</span></span>
<span data-ttu-id="bbd7b-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbd7b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd7b-129">-WhatIf</span></span>
<span data-ttu-id="bbd7b-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd7b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbd7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd7b-132">CommonParameters</span></span>
<span data-ttu-id="bbd7b-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd7b-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbd7b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd7b-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bbd7b-135">INPUTS</span></span>

### <span data-ttu-id="bbd7b-136">Microsoft. Azure. PowerShell. cmdlets. ResourceGraph. Models. IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="bbd7b-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="bbd7b-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bbd7b-137">OUTPUTS</span></span>

### <span data-ttu-id="bbd7b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bbd7b-138">System.Boolean</span></span>

## <span data-ttu-id="bbd7b-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bbd7b-139">NOTES</span></span>

<span data-ttu-id="bbd7b-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bbd7b-140">ALIASES</span></span>

<span data-ttu-id="bbd7b-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="bbd7b-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bbd7b-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bbd7b-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bbd7b-144">INPUTobject <IResourceGraphIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="bbd7b-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bbd7b-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="bbd7b-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bbd7b-146">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="bbd7b-147">`[ResourceName <String>]`: O nome do recurso de consulta de gráfico.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="bbd7b-148">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd7b-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="bbd7b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbd7b-149">RELATED LINKS</span></span>

