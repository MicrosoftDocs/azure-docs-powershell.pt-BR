---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257998"
---
# <span data-ttu-id="9e788-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="9e788-101">Remove-AzPeering</span></span>

## <span data-ttu-id="9e788-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e788-102">SYNOPSIS</span></span>
<span data-ttu-id="9e788-103">Excluir ou remover um emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="9e788-103">Delete or remove a peering.</span></span> <span data-ttu-id="9e788-104">Isso excluirá todos os recursos filho ou o alerta sobre o recurso.</span><span class="sxs-lookup"><span data-stu-id="9e788-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="9e788-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e788-105">SYNTAX</span></span>

### <span data-ttu-id="9e788-106">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e788-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e788-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9e788-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e788-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e788-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e788-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e788-109">DESCRIPTION</span></span>
<span data-ttu-id="9e788-110">Perminently excluir um recurso de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="9e788-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="9e788-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e788-111">EXAMPLES</span></span>

### <span data-ttu-id="9e788-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9e788-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="9e788-113">Remover um emparelhamento por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9e788-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="9e788-114">OS</span><span class="sxs-lookup"><span data-stu-id="9e788-114">PARAMETERS</span></span>

### <span data-ttu-id="9e788-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e788-115">-AsJob</span></span>
<span data-ttu-id="9e788-116">Executar em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="9e788-116">Run in the background.</span></span>

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

### <span data-ttu-id="9e788-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e788-117">-DefaultProfile</span></span>
<span data-ttu-id="9e788-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e788-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e788-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9e788-119">-Force</span></span>
<span data-ttu-id="9e788-120">Forçar a conclusão da operação</span><span class="sxs-lookup"><span data-stu-id="9e788-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="9e788-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e788-121">-InputObject</span></span>
<span data-ttu-id="9e788-122">Use Get-AzPeering para recuperar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="9e788-122">Use Get-AzPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="9e788-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e788-123">-Name</span></span>
<span data-ttu-id="9e788-124">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="9e788-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="9e788-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e788-125">-PassThru</span></span>
<span data-ttu-id="9e788-126">Retornar true se concluir</span><span class="sxs-lookup"><span data-stu-id="9e788-126">Return true if complete</span></span>

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

### <span data-ttu-id="9e788-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e788-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e788-128">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="9e788-128">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="9e788-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e788-129">-ResourceId</span></span>
<span data-ttu-id="9e788-130">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9e788-130">The resource id string name.</span></span>

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

### <span data-ttu-id="9e788-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9e788-131">-Confirm</span></span>
<span data-ttu-id="9e788-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e788-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e788-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e788-133">-WhatIf</span></span>
<span data-ttu-id="9e788-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9e788-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e788-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e788-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e788-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e788-136">CommonParameters</span></span>
<span data-ttu-id="9e788-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e788-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e788-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e788-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e788-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e788-139">INPUTS</span></span>

### <span data-ttu-id="9e788-140">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="9e788-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="9e788-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9e788-141">System.String</span></span>

## <span data-ttu-id="9e788-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e788-142">OUTPUTS</span></span>

### <span data-ttu-id="9e788-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e788-143">System.Boolean</span></span>

## <span data-ttu-id="9e788-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e788-144">NOTES</span></span>

## <span data-ttu-id="9e788-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e788-145">RELATED LINKS</span></span>
