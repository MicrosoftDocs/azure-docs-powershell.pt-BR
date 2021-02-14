---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117281"
---
# <span data-ttu-id="6d0d6-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="6d0d6-101">Remove-AzPeering</span></span>

## <span data-ttu-id="6d0d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="6d0d6-103">Excluir ou remover um peering.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-103">Delete or remove a peering.</span></span> <span data-ttu-id="6d0d6-104">Isso excluirá todos os recursos filho ou os alertas sobre o recurso.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="6d0d6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d0d6-105">SYNTAX</span></span>

### <span data-ttu-id="6d0d6-106">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="6d0d6-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d0d6-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="6d0d6-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d0d6-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6d0d6-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d0d6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d0d6-109">DESCRIPTION</span></span>
<span data-ttu-id="6d0d6-110">Exclua permanentemente um recurso de peering.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="6d0d6-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d0d6-111">EXAMPLES</span></span>

### <span data-ttu-id="6d0d6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d0d6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="6d0d6-113">Remover um peering por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="6d0d6-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d0d6-114">PARAMETERS</span></span>

### <span data-ttu-id="6d0d6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d0d6-115">-AsJob</span></span>
<span data-ttu-id="6d0d6-116">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-116">Run in the background.</span></span>

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

### <span data-ttu-id="6d0d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d0d6-117">-DefaultProfile</span></span>
<span data-ttu-id="6d0d6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d0d6-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="6d0d6-119">-Force</span></span>
<span data-ttu-id="6d0d6-120">Forçar a conclusão da operação</span><span class="sxs-lookup"><span data-stu-id="6d0d6-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="6d0d6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d0d6-121">-InputObject</span></span>
<span data-ttu-id="6d0d6-122">Use Get-AzPeering para recuperar este objeto.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-122">Use Get-AzPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="6d0d6-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d0d6-123">-Name</span></span>
<span data-ttu-id="6d0d6-124">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="6d0d6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d0d6-125">-PassThru</span></span>
<span data-ttu-id="6d0d6-126">Retornar verdadeiro se concluído</span><span class="sxs-lookup"><span data-stu-id="6d0d6-126">Return true if complete</span></span>

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

### <span data-ttu-id="6d0d6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d0d6-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d0d6-128">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-128">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="6d0d6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d0d6-129">-ResourceId</span></span>
<span data-ttu-id="6d0d6-130">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-130">The resource id string name.</span></span>

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

### <span data-ttu-id="6d0d6-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6d0d6-131">-Confirm</span></span>
<span data-ttu-id="6d0d6-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d0d6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d0d6-133">-WhatIf</span></span>
<span data-ttu-id="6d0d6-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d0d6-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d0d6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d0d6-136">CommonParameters</span></span>
<span data-ttu-id="6d0d6-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d0d6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d0d6-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d0d6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d0d6-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="6d0d6-139">INPUTS</span></span>

### <span data-ttu-id="6d0d6-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="6d0d6-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="6d0d6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6d0d6-141">System.String</span></span>

## <span data-ttu-id="6d0d6-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="6d0d6-142">OUTPUTS</span></span>

### <span data-ttu-id="6d0d6-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d0d6-143">System.Boolean</span></span>

## <span data-ttu-id="6d0d6-144">Notas</span><span class="sxs-lookup"><span data-stu-id="6d0d6-144">NOTES</span></span>

## <span data-ttu-id="6d0d6-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d0d6-145">RELATED LINKS</span></span>
