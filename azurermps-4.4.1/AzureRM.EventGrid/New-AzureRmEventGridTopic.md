---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopic.md
ms.openlocfilehash: fdd15de19f921781e89d7e24b57e1d82632e4735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441108"
---
# <span data-ttu-id="60b74-101">New-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="60b74-101">New-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="60b74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60b74-102">SYNOPSIS</span></span>
<span data-ttu-id="60b74-103">Cria um novo tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="60b74-103">Creates a new Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60b74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60b74-104">SYNTAX</span></span>

```
New-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60b74-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60b74-105">DESCRIPTION</span></span>
<span data-ttu-id="60b74-106">Cria um novo tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="60b74-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="60b74-107">Depois que o tópico é criado, um aplicativo pode publicar eventos no ponto de extremidade do tópico.</span><span class="sxs-lookup"><span data-stu-id="60b74-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="60b74-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60b74-108">EXAMPLES</span></span>

### <span data-ttu-id="60b74-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60b74-109">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="60b74-110">Cria um tópico de grade de \` tópico1 \` no local geográfico especificado \` westus2 \` , no grupo de MyResourceGroupName grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="60b74-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="60b74-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="60b74-111">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="60b74-112">Cria um tópico de grade de \` tópico1 \` no local geográfico especificado \` westus2 \` , no grupo de recursos \` MyResourceGroupName, \` com as marcas especificadas "Department" e "Environment".</span><span class="sxs-lookup"><span data-stu-id="60b74-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="60b74-113">OS</span><span class="sxs-lookup"><span data-stu-id="60b74-113">PARAMETERS</span></span>

### <span data-ttu-id="60b74-114">-Local</span><span class="sxs-lookup"><span data-stu-id="60b74-114">-Location</span></span>
<span data-ttu-id="60b74-115">O local do tópico</span><span class="sxs-lookup"><span data-stu-id="60b74-115">The location of the topic</span></span>

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

### <span data-ttu-id="60b74-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="60b74-116">-Name</span></span>
<span data-ttu-id="60b74-117">O nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="60b74-117">The name of the topic.</span></span>

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

### <span data-ttu-id="60b74-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b74-118">-ResourceGroupName</span></span>
<span data-ttu-id="60b74-119">O grupo de recursos no qual o tópico deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="60b74-119">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="60b74-120">-Marca</span><span class="sxs-lookup"><span data-stu-id="60b74-120">-Tag</span></span>
<span data-ttu-id="60b74-121">Hashtables que representam marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="60b74-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="60b74-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60b74-122">-Confirm</span></span>
<span data-ttu-id="60b74-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60b74-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60b74-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60b74-124">-WhatIf</span></span>
<span data-ttu-id="60b74-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60b74-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60b74-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60b74-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60b74-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b74-127">-DefaultProfile</span></span>
<span data-ttu-id="60b74-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60b74-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60b74-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b74-129">CommonParameters</span></span>
<span data-ttu-id="60b74-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b74-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b74-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60b74-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b74-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60b74-132">INPUTS</span></span>

### <span data-ttu-id="60b74-133">System. String</span><span class="sxs-lookup"><span data-stu-id="60b74-133">System.String</span></span>
<span data-ttu-id="60b74-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="60b74-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="60b74-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60b74-135">OUTPUTS</span></span>

### <span data-ttu-id="60b74-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="60b74-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="60b74-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60b74-137">NOTES</span></span>

## <span data-ttu-id="60b74-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60b74-138">RELATED LINKS</span></span>

