---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
ms.openlocfilehash: a20262e1414b8f747e638f22283aed26b5483896
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430940"
---
# <span data-ttu-id="a772b-101">New-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="a772b-101">New-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="a772b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a772b-102">SYNOPSIS</span></span>
<span data-ttu-id="a772b-103">Cria um novo tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a772b-103">Creates a new Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a772b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a772b-104">SYNTAX</span></span>

```
New-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a772b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a772b-105">DESCRIPTION</span></span>
<span data-ttu-id="a772b-106">Cria um novo tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a772b-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="a772b-107">Depois que o tópico é criado, um aplicativo pode publicar eventos no ponto de extremidade do tópico.</span><span class="sxs-lookup"><span data-stu-id="a772b-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="a772b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a772b-108">EXAMPLES</span></span>

### <span data-ttu-id="a772b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a772b-109">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="a772b-110">Cria um tópico de grade de \` tópico1 \` no local geográfico especificado \` westus2 \` , no grupo de MyResourceGroupName grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="a772b-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a772b-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a772b-111">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="a772b-112">Cria um tópico de grade de \` tópico1 \` no local geográfico especificado \` westus2 \` , no grupo de recursos \` MyResourceGroupName, \` com as marcas especificadas "Department" e "Environment".</span><span class="sxs-lookup"><span data-stu-id="a772b-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="a772b-113">OS</span><span class="sxs-lookup"><span data-stu-id="a772b-113">PARAMETERS</span></span>

### <span data-ttu-id="a772b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a772b-114">-DefaultProfile</span></span>
<span data-ttu-id="a772b-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a772b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a772b-116">-Local</span><span class="sxs-lookup"><span data-stu-id="a772b-116">-Location</span></span>
<span data-ttu-id="a772b-117">O local do tópico</span><span class="sxs-lookup"><span data-stu-id="a772b-117">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a772b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a772b-118">-Name</span></span>
<span data-ttu-id="a772b-119">O nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="a772b-119">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a772b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a772b-120">-ResourceGroupName</span></span>
<span data-ttu-id="a772b-121">O grupo de recursos no qual o tópico deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="a772b-121">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a772b-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="a772b-122">-Tag</span></span>
<span data-ttu-id="a772b-123">Hashtables que representam marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="a772b-123">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a772b-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a772b-124">-Confirm</span></span>
<span data-ttu-id="a772b-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a772b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a772b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a772b-126">-WhatIf</span></span>
<span data-ttu-id="a772b-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a772b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a772b-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a772b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a772b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a772b-129">CommonParameters</span></span>
<span data-ttu-id="a772b-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a772b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a772b-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a772b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a772b-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a772b-132">INPUTS</span></span>

### <span data-ttu-id="a772b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a772b-133">System.String</span></span>

### <span data-ttu-id="a772b-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a772b-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a772b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a772b-135">OUTPUTS</span></span>

### <span data-ttu-id="a772b-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a772b-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a772b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a772b-137">NOTES</span></span>

## <span data-ttu-id="a772b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a772b-138">RELATED LINKS</span></span>
