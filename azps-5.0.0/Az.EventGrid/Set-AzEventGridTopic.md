---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117454"
---
# <span data-ttu-id="c2063-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="c2063-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="c2063-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2063-102">SYNOPSIS</span></span>
<span data-ttu-id="c2063-103">Define as propriedades de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="c2063-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="c2063-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2063-104">SYNTAX</span></span>

### <span data-ttu-id="c2063-105">TopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c2063-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2063-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2063-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2063-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2063-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2063-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2063-108">DESCRIPTION</span></span>
<span data-ttu-id="c2063-109">Define as propriedades de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="c2063-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="c2063-110">Isso pode ser usado para substituir as marcas de um tópico de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="c2063-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="c2063-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2063-111">EXAMPLES</span></span>

### <span data-ttu-id="c2063-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2063-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="c2063-113">Define as propriedades do tópico da grade de eventos \` tópico1 \` no grupo de MyResourceGroupName de recursos \` \` para substituir as marcas por "departamento" e "ambiente" especificado.</span><span class="sxs-lookup"><span data-stu-id="c2063-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="c2063-114">OS</span><span class="sxs-lookup"><span data-stu-id="c2063-114">PARAMETERS</span></span>

### <span data-ttu-id="c2063-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2063-115">-DefaultProfile</span></span>
<span data-ttu-id="c2063-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c2063-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2063-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="c2063-117">-InboundIpRule</span></span>
<span data-ttu-id="c2063-118">Hashtable que representa a lista de regras de IP de entrada.</span><span class="sxs-lookup"><span data-stu-id="c2063-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="c2063-119">Cada regra especifica o endereço IP na notação CIDR, por exemplo, 10.0.0.0/8 juntamente com a ação correspondente a ser executada com base na correspondência ou nenhuma correspondência do IpMask.</span><span class="sxs-lookup"><span data-stu-id="c2063-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="c2063-120">Os valores de ação possíveis incluem somente permitir</span><span class="sxs-lookup"><span data-stu-id="c2063-120">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2063-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2063-121">-InputObject</span></span>
<span data-ttu-id="c2063-122">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c2063-122">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="c2063-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2063-123">-Name</span></span>
<span data-ttu-id="c2063-124">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c2063-124">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="c2063-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c2063-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="c2063-126">Isso determina se o tráfego é permitido em redes públicas.</span><span class="sxs-lookup"><span data-stu-id="c2063-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="c2063-127">Por padrão, ele está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c2063-127">By default it is enabled.</span></span> <span data-ttu-id="c2063-128">Você pode restringir ainda mais a IPs específicos configurando parâmetros InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="c2063-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="c2063-129">Os valores permitidos são desabilitados e habilitados.</span><span class="sxs-lookup"><span data-stu-id="c2063-129">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:
Accepted values: enabled, disabled

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:
Accepted values: enabled, disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2063-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2063-130">-ResourceGroupName</span></span>
<span data-ttu-id="c2063-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2063-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="c2063-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2063-132">-ResourceId</span></span>
<span data-ttu-id="c2063-133">Resourceation topic EventGrid</span><span class="sxs-lookup"><span data-stu-id="c2063-133">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="c2063-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="c2063-134">-Tag</span></span>
<span data-ttu-id="c2063-135">Hashtables que representam a marca de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2063-135">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2063-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c2063-136">-Confirm</span></span>
<span data-ttu-id="c2063-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2063-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2063-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2063-138">-WhatIf</span></span>
<span data-ttu-id="c2063-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c2063-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2063-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c2063-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2063-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2063-141">CommonParameters</span></span>
<span data-ttu-id="c2063-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2063-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2063-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2063-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2063-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2063-144">INPUTS</span></span>

### <span data-ttu-id="c2063-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c2063-145">System.String</span></span>

### <span data-ttu-id="c2063-146">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c2063-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="c2063-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c2063-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c2063-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2063-148">OUTPUTS</span></span>

### <span data-ttu-id="c2063-149">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c2063-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="c2063-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2063-150">NOTES</span></span>

## <span data-ttu-id="c2063-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2063-151">RELATED LINKS</span></span>
