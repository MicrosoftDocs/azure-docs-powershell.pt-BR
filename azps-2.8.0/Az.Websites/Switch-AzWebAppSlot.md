---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 932ac78e3ea17bf6d0dbfe79ab45910fb2527e41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774413"
---
# <span data-ttu-id="be893-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="be893-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="be893-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be893-102">SYNOPSIS</span></span>
<span data-ttu-id="be893-103">Trocar dois slots por um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="be893-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="be893-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be893-104">SYNTAX</span></span>

### <span data-ttu-id="be893-105">Eles</span><span class="sxs-lookup"><span data-stu-id="be893-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be893-106">S2</span><span class="sxs-lookup"><span data-stu-id="be893-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be893-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be893-107">DESCRIPTION</span></span>
<span data-ttu-id="be893-108">O **switch-AzWebAppSlot** alterna dois slots associados a um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="be893-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="be893-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be893-109">EXAMPLES</span></span>

### <span data-ttu-id="be893-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="be893-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="be893-111">Esse comando alternará o slot "sourceslot" do slot com "destinationslot", o aplicativo Web ContosoWebApp associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="be893-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="be893-112">OS</span><span class="sxs-lookup"><span data-stu-id="be893-112">PARAMETERS</span></span>

### <span data-ttu-id="be893-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be893-113">-DefaultProfile</span></span>
<span data-ttu-id="be893-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be893-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be893-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="be893-115">-DestinationSlotName</span></span>
<span data-ttu-id="be893-116">Nome do slot de destino</span><span class="sxs-lookup"><span data-stu-id="be893-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="be893-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="be893-117">-Name</span></span>
<span data-ttu-id="be893-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="be893-118">WebApp Name</span></span>

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

### <span data-ttu-id="be893-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="be893-119">-PreserveVnet</span></span>
<span data-ttu-id="be893-120">Preservar booliano de vnet</span><span class="sxs-lookup"><span data-stu-id="be893-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="be893-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be893-121">-ResourceGroupName</span></span>
<span data-ttu-id="be893-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="be893-122">Resource Group Name</span></span>

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

### <span data-ttu-id="be893-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="be893-123">-SourceSlotName</span></span>
<span data-ttu-id="be893-124">Nome do slot de origem</span><span class="sxs-lookup"><span data-stu-id="be893-124">Source Slot Name</span></span>

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

### <span data-ttu-id="be893-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="be893-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="be893-126">Alternar com ação de visualização</span><span class="sxs-lookup"><span data-stu-id="be893-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="be893-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="be893-127">-WebApp</span></span>
<span data-ttu-id="be893-128">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="be893-128">WebApp Object</span></span>

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

### <span data-ttu-id="be893-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="be893-129">-Confirm</span></span>
<span data-ttu-id="be893-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be893-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be893-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be893-131">-WhatIf</span></span>
<span data-ttu-id="be893-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be893-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be893-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be893-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be893-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be893-134">CommonParameters</span></span>
<span data-ttu-id="be893-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be893-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be893-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be893-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be893-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be893-137">INPUTS</span></span>

### <span data-ttu-id="be893-138">System. String</span><span class="sxs-lookup"><span data-stu-id="be893-138">System.String</span></span>

### <span data-ttu-id="be893-139">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="be893-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="be893-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be893-140">OUTPUTS</span></span>

### <span data-ttu-id="be893-141">System. void</span><span class="sxs-lookup"><span data-stu-id="be893-141">System.Void</span></span>

## <span data-ttu-id="be893-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be893-142">NOTES</span></span>

## <span data-ttu-id="be893-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be893-143">RELATED LINKS</span></span>