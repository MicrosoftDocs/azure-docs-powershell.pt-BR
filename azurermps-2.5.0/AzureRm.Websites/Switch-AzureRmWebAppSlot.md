---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 9671c2041f767df5066353988eb633318289de47
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785402"
---
# <span data-ttu-id="b60df-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b60df-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="b60df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b60df-102">SYNOPSIS</span></span>
<span data-ttu-id="b60df-103">Trocar dois slots por um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="b60df-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b60df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b60df-104">SYNTAX</span></span>

### <span data-ttu-id="b60df-105">Eles</span><span class="sxs-lookup"><span data-stu-id="b60df-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b60df-106">S2</span><span class="sxs-lookup"><span data-stu-id="b60df-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b60df-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b60df-107">DESCRIPTION</span></span>
<span data-ttu-id="b60df-108">O **switch-AzureRmWebAppSlot** alterna dois slots associados a um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="b60df-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="b60df-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b60df-109">EXAMPLES</span></span>

### <span data-ttu-id="b60df-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b60df-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="b60df-111">Esse comando alternará o slot "sourceslot" do slot com "destinationslot" para o aplicativo Web ContosoWebApp associado ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="b60df-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="b60df-112">OS</span><span class="sxs-lookup"><span data-stu-id="b60df-112">PARAMETERS</span></span>

### <span data-ttu-id="b60df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60df-113">-DefaultProfile</span></span>
<span data-ttu-id="b60df-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b60df-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b60df-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="b60df-115">-DestinationSlotName</span></span>
<span data-ttu-id="b60df-116">Nome do slot de destino</span><span class="sxs-lookup"><span data-stu-id="b60df-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="b60df-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b60df-117">-Name</span></span>
<span data-ttu-id="b60df-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="b60df-118">WebApp Name</span></span>

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

### <span data-ttu-id="b60df-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="b60df-119">-PreserveVnet</span></span>
<span data-ttu-id="b60df-120">Preservar booliano de vnet</span><span class="sxs-lookup"><span data-stu-id="b60df-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="b60df-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60df-121">-ResourceGroupName</span></span>
<span data-ttu-id="b60df-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b60df-122">Resource Group Name</span></span>

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

### <span data-ttu-id="b60df-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="b60df-123">-SourceSlotName</span></span>
<span data-ttu-id="b60df-124">Nome do slot de origem</span><span class="sxs-lookup"><span data-stu-id="b60df-124">Source Slot Name</span></span>

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

### <span data-ttu-id="b60df-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="b60df-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="b60df-126">Alternar com ação de visualização</span><span class="sxs-lookup"><span data-stu-id="b60df-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="b60df-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b60df-127">-WebApp</span></span>
<span data-ttu-id="b60df-128">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="b60df-128">WebApp Object</span></span>

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

### <span data-ttu-id="b60df-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b60df-129">-Confirm</span></span>
<span data-ttu-id="b60df-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b60df-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b60df-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60df-131">-WhatIf</span></span>
<span data-ttu-id="b60df-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b60df-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b60df-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b60df-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b60df-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60df-134">CommonParameters</span></span>
<span data-ttu-id="b60df-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b60df-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60df-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b60df-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60df-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b60df-137">INPUTS</span></span>

### <span data-ttu-id="b60df-138">Instalação</span><span class="sxs-lookup"><span data-stu-id="b60df-138">Site</span></span>
<span data-ttu-id="b60df-139">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="b60df-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b60df-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b60df-140">OUTPUTS</span></span>

## <span data-ttu-id="b60df-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b60df-141">NOTES</span></span>

## <span data-ttu-id="b60df-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b60df-142">RELATED LINKS</span></span>

