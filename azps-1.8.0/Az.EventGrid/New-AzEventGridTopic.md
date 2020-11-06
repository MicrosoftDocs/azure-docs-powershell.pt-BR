---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 1922d399cf4b7c4fe1295f9a19409094ab5676c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600869"
---
# <span data-ttu-id="fbe0a-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="fbe0a-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="fbe0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbe0a-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe0a-103">Cria um novo tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe0a-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="fbe0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbe0a-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe0a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fbe0a-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe0a-106">Cria um novo tópico da grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe0a-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="fbe0a-107">Depois que o tópico é criado, um aplicativo pode publicar eventos no ponto de extremidade do tópico.</span><span class="sxs-lookup"><span data-stu-id="fbe0a-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="fbe0a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbe0a-108">EXAMPLES</span></span>

### <span data-ttu-id="fbe0a-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fbe0a-109">Example 1</span></span>
```
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="fbe0a-110">Cria um tópico de grade de \` tópico1 \` no local geográfico especificado \` westus2 \` , no grupo de MyResourceGroupName grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="fbe0a-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="fbe0a-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fbe0a-111">Example 2</span></span>
```
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="fbe0a-112">Cria um tópico de grade de \` tópico1 \` no local geográfico especificado \` westus2 \` , no grupo de recursos \` MyResourceGroupName, \` com as marcas especificadas "Department" e "Environment".</span><span class="sxs-lookup"><span data-stu-id="fbe0a-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="fbe0a-113">OS</span><span class="sxs-lookup"><span data-stu-id="fbe0a-113">PARAMETERS</span></span>

### <span data-ttu-id="fbe0a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe0a-114">-DefaultProfile</span></span>
<span data-ttu-id="fbe0a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fbe0a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbe0a-116">-Local</span><span class="sxs-lookup"><span data-stu-id="fbe0a-116">-Location</span></span>
<span data-ttu-id="fbe0a-117">O local do tópico</span><span class="sxs-lookup"><span data-stu-id="fbe0a-117">The location of the topic</span></span>

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

### <span data-ttu-id="fbe0a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbe0a-118">-Name</span></span>
<span data-ttu-id="fbe0a-119">O nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="fbe0a-119">The name of the topic.</span></span>

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

### <span data-ttu-id="fbe0a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe0a-120">-ResourceGroupName</span></span>
<span data-ttu-id="fbe0a-121">O grupo de recursos no qual o tópico deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="fbe0a-121">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="fbe0a-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="fbe0a-122">-Tag</span></span>
<span data-ttu-id="fbe0a-123">Hashtables que representam marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="fbe0a-123">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="fbe0a-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fbe0a-124">-Confirm</span></span>
<span data-ttu-id="fbe0a-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbe0a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe0a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe0a-126">-WhatIf</span></span>
<span data-ttu-id="fbe0a-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fbe0a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe0a-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fbe0a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe0a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe0a-129">CommonParameters</span></span>
<span data-ttu-id="fbe0a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe0a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe0a-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe0a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe0a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fbe0a-132">INPUTS</span></span>

### <span data-ttu-id="fbe0a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fbe0a-133">System.String</span></span>

### <span data-ttu-id="fbe0a-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbe0a-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fbe0a-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fbe0a-135">OUTPUTS</span></span>

### <span data-ttu-id="fbe0a-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="fbe0a-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="fbe0a-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fbe0a-137">NOTES</span></span>

## <span data-ttu-id="fbe0a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbe0a-138">RELATED LINKS</span></span>
