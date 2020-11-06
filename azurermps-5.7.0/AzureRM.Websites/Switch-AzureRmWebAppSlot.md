---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
ms.openlocfilehash: e1cfb3e70ab8176cfd686dc404b13dbbfb23e4e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427376"
---
# <span data-ttu-id="afec3-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="afec3-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="afec3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afec3-102">SYNOPSIS</span></span>
<span data-ttu-id="afec3-103">Trocar dois slots por um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="afec3-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afec3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afec3-104">SYNTAX</span></span>

### <span data-ttu-id="afec3-105">Eles</span><span class="sxs-lookup"><span data-stu-id="afec3-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afec3-106">S2</span><span class="sxs-lookup"><span data-stu-id="afec3-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afec3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afec3-107">DESCRIPTION</span></span>
<span data-ttu-id="afec3-108">O **switch-AzureRmWebAppSlot** alterna dois slots associados a um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="afec3-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="afec3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afec3-109">EXAMPLES</span></span>

### <span data-ttu-id="afec3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="afec3-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="afec3-111">Esse comando alternará o slot "sourceslot" do slot com "destinationslot" para o aplicativo Web ContosoWebApp associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="afec3-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="afec3-112">OS</span><span class="sxs-lookup"><span data-stu-id="afec3-112">PARAMETERS</span></span>

### <span data-ttu-id="afec3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afec3-113">-DefaultProfile</span></span>
<span data-ttu-id="afec3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afec3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afec3-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="afec3-115">-DestinationSlotName</span></span>
<span data-ttu-id="afec3-116">Nome do slot de destino</span><span class="sxs-lookup"><span data-stu-id="afec3-116">Destination Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afec3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="afec3-117">-Name</span></span>
<span data-ttu-id="afec3-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="afec3-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afec3-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="afec3-119">-PreserveVnet</span></span>
<span data-ttu-id="afec3-120">Preservar booliano de vnet</span><span class="sxs-lookup"><span data-stu-id="afec3-120">Preserve Vnet Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afec3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afec3-121">-ResourceGroupName</span></span>
<span data-ttu-id="afec3-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="afec3-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afec3-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="afec3-123">-SourceSlotName</span></span>
<span data-ttu-id="afec3-124">Nome do slot de origem</span><span class="sxs-lookup"><span data-stu-id="afec3-124">Source Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afec3-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="afec3-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="afec3-126">Alternar com ação de visualização</span><span class="sxs-lookup"><span data-stu-id="afec3-126">Swap With Preview Action</span></span>

```yaml
Type: SwapWithPreviewAction
Parameter Sets: (All)
Aliases: 
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afec3-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="afec3-127">-WebApp</span></span>
<span data-ttu-id="afec3-128">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="afec3-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afec3-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="afec3-129">-Confirm</span></span>
<span data-ttu-id="afec3-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afec3-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afec3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afec3-131">-WhatIf</span></span>
<span data-ttu-id="afec3-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="afec3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afec3-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="afec3-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afec3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afec3-134">CommonParameters</span></span>
<span data-ttu-id="afec3-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afec3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afec3-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afec3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afec3-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afec3-137">INPUTS</span></span>

### <span data-ttu-id="afec3-138">Instalação</span><span class="sxs-lookup"><span data-stu-id="afec3-138">Site</span></span>
<span data-ttu-id="afec3-139">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="afec3-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="afec3-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afec3-140">OUTPUTS</span></span>

## <span data-ttu-id="afec3-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afec3-141">NOTES</span></span>

## <span data-ttu-id="afec3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afec3-142">RELATED LINKS</span></span>

