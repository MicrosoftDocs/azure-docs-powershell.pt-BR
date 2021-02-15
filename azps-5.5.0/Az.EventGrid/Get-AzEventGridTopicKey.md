---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115323"
---
# <span data-ttu-id="f1f64-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="f1f64-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="f1f64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1f64-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f64-103">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um tópico de Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="f1f64-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="f1f64-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1f64-104">SYNTAX</span></span>

### <span data-ttu-id="f1f64-105">TopicNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f1f64-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1f64-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1f64-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1f64-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1f64-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1f64-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1f64-108">DESCRIPTION</span></span>
<span data-ttu-id="f1f64-109">Obtém as chaves de acesso compartilhado usadas para publicar eventos em um tópico de Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="f1f64-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="f1f64-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f1f64-110">EXAMPLES</span></span>

### <span data-ttu-id="f1f64-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1f64-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="f1f64-112">Obtém as chaves de acesso compartilhado do tópico tópico da Grade do Evento1 no grupo \` \` de recursos \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="f1f64-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f1f64-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f1f64-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="f1f64-114">Obtém as chaves de acesso compartilhado do tópico tópico da Grade do Evento1 no grupo \` \` de recursos \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="f1f64-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f1f64-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1f64-115">PARAMETERS</span></span>

### <span data-ttu-id="f1f64-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f64-116">-DefaultProfile</span></span>
<span data-ttu-id="f1f64-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f1f64-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1f64-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1f64-118">-InputObject</span></span>
<span data-ttu-id="f1f64-119">Objeto De Tópico do EventGrid.</span><span class="sxs-lookup"><span data-stu-id="f1f64-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="f1f64-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1f64-120">-Name</span></span>
<span data-ttu-id="f1f64-121">Nome do tópico do EventGrid.</span><span class="sxs-lookup"><span data-stu-id="f1f64-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="f1f64-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f64-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1f64-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1f64-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="f1f64-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1f64-124">-ResourceId</span></span>
<span data-ttu-id="f1f64-125">Identificador de Recurso representando o Tópico da Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="f1f64-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="f1f64-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f64-126">CommonParameters</span></span>
<span data-ttu-id="f1f64-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f64-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f64-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1f64-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f64-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="f1f64-129">INPUTS</span></span>

### <span data-ttu-id="f1f64-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f1f64-130">System.String</span></span>

### <span data-ttu-id="f1f64-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="f1f64-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="f1f64-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="f1f64-132">OUTPUTS</span></span>

### <span data-ttu-id="f1f64-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f1f64-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="f1f64-134">Notas</span><span class="sxs-lookup"><span data-stu-id="f1f64-134">NOTES</span></span>

## <span data-ttu-id="f1f64-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1f64-135">RELATED LINKS</span></span>
