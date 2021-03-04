---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: 92a70d16f8cd1db2c37c1247c994a3c406df5a54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890424"
---
# <span data-ttu-id="8325a-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="8325a-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="8325a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8325a-102">SYNOPSIS</span></span>
<span data-ttu-id="8325a-103">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um tópico de Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="8325a-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="8325a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8325a-104">SYNTAX</span></span>

### <span data-ttu-id="8325a-105">TopicNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8325a-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8325a-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8325a-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8325a-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8325a-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8325a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8325a-108">DESCRIPTION</span></span>
<span data-ttu-id="8325a-109">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um tópico de Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="8325a-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="8325a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8325a-110">EXAMPLES</span></span>

### <span data-ttu-id="8325a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8325a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="8325a-112">Obtém as chaves de acesso compartilhado do tópico Tópico da Grade de Eventos1 no grupo de recursos \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8325a-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8325a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8325a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="8325a-114">Obtém as chaves de acesso compartilhado do tópico Tópico da Grade de Eventos1 no grupo de recursos \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="8325a-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="8325a-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8325a-115">PARAMETERS</span></span>

### <span data-ttu-id="8325a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8325a-116">-DefaultProfile</span></span>
<span data-ttu-id="8325a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8325a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8325a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8325a-118">-InputObject</span></span>
<span data-ttu-id="8325a-119">Objeto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="8325a-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8325a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8325a-120">-Name</span></span>
<span data-ttu-id="8325a-121">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8325a-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8325a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8325a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8325a-123">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="8325a-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8325a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8325a-124">-ResourceId</span></span>
<span data-ttu-id="8325a-125">Identificador de Recurso que representa o Tópico da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="8325a-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8325a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8325a-126">CommonParameters</span></span>
<span data-ttu-id="8325a-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8325a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8325a-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8325a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8325a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8325a-129">INPUTS</span></span>

### <span data-ttu-id="8325a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8325a-130">System.String</span></span>

### <span data-ttu-id="8325a-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="8325a-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="8325a-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8325a-132">OUTPUTS</span></span>

### <span data-ttu-id="8325a-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="8325a-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="8325a-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="8325a-134">NOTES</span></span>

## <span data-ttu-id="8325a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8325a-135">RELATED LINKS</span></span>
