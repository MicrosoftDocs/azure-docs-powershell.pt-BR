---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 7cb74e6eec27df299206ee62264588a37dee3a2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893026"
---
# <span data-ttu-id="c0c41-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c0c41-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="c0c41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0c41-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c41-103">Trocar dois slots por um Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="c0c41-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="c0c41-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c0c41-104">SYNTAX</span></span>

### <span data-ttu-id="c0c41-105">S1</span><span class="sxs-lookup"><span data-stu-id="c0c41-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c41-106">S2</span><span class="sxs-lookup"><span data-stu-id="c0c41-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c41-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c0c41-107">DESCRIPTION</span></span>
<span data-ttu-id="c0c41-108">O **Switch-AzWebAppSlot** alterna dois slots associados a um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0c41-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="c0c41-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0c41-109">EXAMPLES</span></span>

### <span data-ttu-id="c0c41-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0c41-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="c0c41-111">Este comando alterna o slot "sourceslot" com "destinationslot" do Web App ContosoWebApp associado ao grupo de recursos Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="c0c41-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c0c41-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c0c41-112">PARAMETERS</span></span>

### <span data-ttu-id="c0c41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c41-113">-DefaultProfile</span></span>
<span data-ttu-id="c0c41-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c0c41-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0c41-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="c0c41-115">-DestinationSlotName</span></span>
<span data-ttu-id="c0c41-116">Nome do Slot de Destino</span><span class="sxs-lookup"><span data-stu-id="c0c41-116">Destination Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c41-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c0c41-117">-Name</span></span>
<span data-ttu-id="c0c41-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="c0c41-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c41-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="c0c41-119">-PreserveVnet</span></span>
<span data-ttu-id="c0c41-120">Preserve Vnet Boolean</span><span class="sxs-lookup"><span data-stu-id="c0c41-120">Preserve Vnet Boolean</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c41-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0c41-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0c41-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c0c41-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c41-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="c0c41-123">-SourceSlotName</span></span>
<span data-ttu-id="c0c41-124">Nome do slot de origem</span><span class="sxs-lookup"><span data-stu-id="c0c41-124">Source Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c41-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="c0c41-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="c0c41-126">Troca com ação de visualização</span><span class="sxs-lookup"><span data-stu-id="c0c41-126">Swap With Preview Action</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.WebApps.Utilities.SwapWithPreviewAction]
Parameter Sets: (All)
Aliases:
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0c41-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c0c41-127">-WebApp</span></span>
<span data-ttu-id="c0c41-128">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="c0c41-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c41-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0c41-129">-Confirm</span></span>
<span data-ttu-id="c0c41-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0c41-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c41-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c41-131">-WhatIf</span></span>
<span data-ttu-id="c0c41-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0c41-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c41-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0c41-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c41-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c41-134">CommonParameters</span></span>
<span data-ttu-id="c0c41-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c41-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c41-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c41-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c41-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0c41-137">INPUTS</span></span>

### <span data-ttu-id="c0c41-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c0c41-138">System.String</span></span>

### <span data-ttu-id="c0c41-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c0c41-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c0c41-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c0c41-140">OUTPUTS</span></span>

### <span data-ttu-id="c0c41-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="c0c41-141">System.Void</span></span>

## <span data-ttu-id="c0c41-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="c0c41-142">NOTES</span></span>

## <span data-ttu-id="c0c41-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0c41-143">RELATED LINKS</span></span>
