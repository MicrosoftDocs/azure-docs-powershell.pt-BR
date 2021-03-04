---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: ba6817928751c67e87f6641a6362a1fbf84eece8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890139"
---
# <span data-ttu-id="df357-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="df357-101">Remove-AzPeering</span></span>

## <span data-ttu-id="df357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df357-102">SYNOPSIS</span></span>
<span data-ttu-id="df357-103">Excluir ou remover um par.</span><span class="sxs-lookup"><span data-stu-id="df357-103">Delete or remove a peering.</span></span> <span data-ttu-id="df357-104">Isso excluirá todos os recursos filho ou alertará o recurso.</span><span class="sxs-lookup"><span data-stu-id="df357-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="df357-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="df357-105">SYNTAX</span></span>

### <span data-ttu-id="df357-106">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="df357-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df357-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="df357-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df357-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df357-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df357-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="df357-109">DESCRIPTION</span></span>
<span data-ttu-id="df357-110">Exclua permanentemente um recurso de peering.</span><span class="sxs-lookup"><span data-stu-id="df357-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="df357-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df357-111">EXAMPLES</span></span>

### <span data-ttu-id="df357-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df357-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="df357-113">Remova um paring por id de recurso.</span><span class="sxs-lookup"><span data-stu-id="df357-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="df357-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="df357-114">PARAMETERS</span></span>

### <span data-ttu-id="df357-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df357-115">-AsJob</span></span>
<span data-ttu-id="df357-116">Execute em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="df357-116">Run in the background.</span></span>

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

### <span data-ttu-id="df357-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df357-117">-DefaultProfile</span></span>
<span data-ttu-id="df357-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df357-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df357-119">-Force</span><span class="sxs-lookup"><span data-stu-id="df357-119">-Force</span></span>
<span data-ttu-id="df357-120">Forçar a conclusão da operação</span><span class="sxs-lookup"><span data-stu-id="df357-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="df357-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df357-121">-InputObject</span></span>
<span data-ttu-id="df357-122">Use Get-AzPeering para recuperar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="df357-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df357-123">-Name</span><span class="sxs-lookup"><span data-stu-id="df357-123">-Name</span></span>
<span data-ttu-id="df357-124">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="df357-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df357-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df357-125">-PassThru</span></span>
<span data-ttu-id="df357-126">Retornar true se concluído</span><span class="sxs-lookup"><span data-stu-id="df357-126">Return true if complete</span></span>

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

### <span data-ttu-id="df357-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df357-127">-ResourceGroupName</span></span>
<span data-ttu-id="df357-128">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="df357-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df357-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df357-129">-ResourceId</span></span>
<span data-ttu-id="df357-130">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="df357-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df357-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df357-131">-Confirm</span></span>
<span data-ttu-id="df357-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df357-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df357-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df357-133">-WhatIf</span></span>
<span data-ttu-id="df357-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df357-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df357-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df357-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df357-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df357-136">CommonParameters</span></span>
<span data-ttu-id="df357-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df357-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df357-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df357-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df357-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df357-139">INPUTS</span></span>

### <span data-ttu-id="df357-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="df357-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="df357-141">System.String</span><span class="sxs-lookup"><span data-stu-id="df357-141">System.String</span></span>

## <span data-ttu-id="df357-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="df357-142">OUTPUTS</span></span>

### <span data-ttu-id="df357-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df357-143">System.Boolean</span></span>

## <span data-ttu-id="df357-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="df357-144">NOTES</span></span>

## <span data-ttu-id="df357-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df357-145">RELATED LINKS</span></span>
