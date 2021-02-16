---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117670"
---
# <span data-ttu-id="484d7-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="484d7-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="484d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="484d7-102">SYNOPSIS</span></span>
<span data-ttu-id="484d7-103">Define as propriedades de um tópico de Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="484d7-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="484d7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="484d7-104">SYNTAX</span></span>

### <span data-ttu-id="484d7-105">TopicNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="484d7-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="484d7-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="484d7-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="484d7-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="484d7-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="484d7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="484d7-108">DESCRIPTION</span></span>
<span data-ttu-id="484d7-109">Define as propriedades de um tópico de Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="484d7-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="484d7-110">Isso pode ser usado para substituir as marcas de um tópico de Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="484d7-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="484d7-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="484d7-111">EXAMPLES</span></span>

### <span data-ttu-id="484d7-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="484d7-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="484d7-113">Define as propriedades do tópico da Grade do Evento1 no grupo de recursos MyResourceGroupName para substituir as marcas com as marcas \` \` \` \` especificadas "Departamento" e "Ambiente".</span><span class="sxs-lookup"><span data-stu-id="484d7-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="484d7-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="484d7-114">PARAMETERS</span></span>

### <span data-ttu-id="484d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="484d7-115">-DefaultProfile</span></span>
<span data-ttu-id="484d7-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="484d7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="484d7-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="484d7-117">-InboundIpRule</span></span>
<span data-ttu-id="484d7-118">Hashtable, que representa a lista de regras de IP de entrada.</span><span class="sxs-lookup"><span data-stu-id="484d7-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="484d7-119">Cada regra especifica o Endereço IP na notação CIDR, por exemplo, 10.0.0.0/8 juntamente com a Ação correspondente a ser executada com base na combinação ou nenhuma correspondente da IpMask.</span><span class="sxs-lookup"><span data-stu-id="484d7-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="484d7-120">Os valores possíveis de Ação incluem Permitir somente</span><span class="sxs-lookup"><span data-stu-id="484d7-120">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="484d7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="484d7-121">-InputObject</span></span>
<span data-ttu-id="484d7-122">Objeto De Tópico do EventGrid.</span><span class="sxs-lookup"><span data-stu-id="484d7-122">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="484d7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="484d7-123">-Name</span></span>
<span data-ttu-id="484d7-124">Nome do tópico do EventGrid.</span><span class="sxs-lookup"><span data-stu-id="484d7-124">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="484d7-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="484d7-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="484d7-126">Isso determina se o tráfego é permitido pela rede pública.</span><span class="sxs-lookup"><span data-stu-id="484d7-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="484d7-127">Por padrão, ela está habilitada.</span><span class="sxs-lookup"><span data-stu-id="484d7-127">By default it is enabled.</span></span> <span data-ttu-id="484d7-128">Você pode restringir ainda mais a IPs específicos configurando parâmetros InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="484d7-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="484d7-129">Os valores permitidos são desabilitados e habilitados.</span><span class="sxs-lookup"><span data-stu-id="484d7-129">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="484d7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="484d7-130">-ResourceGroupName</span></span>
<span data-ttu-id="484d7-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="484d7-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="484d7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="484d7-132">-ResourceId</span></span>
<span data-ttu-id="484d7-133">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="484d7-133">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="484d7-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="484d7-134">-Tag</span></span>
<span data-ttu-id="484d7-135">Hashtables que representa a marca de recurso.</span><span class="sxs-lookup"><span data-stu-id="484d7-135">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="484d7-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="484d7-136">-Confirm</span></span>
<span data-ttu-id="484d7-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="484d7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="484d7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="484d7-138">-WhatIf</span></span>
<span data-ttu-id="484d7-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="484d7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="484d7-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="484d7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="484d7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="484d7-141">CommonParameters</span></span>
<span data-ttu-id="484d7-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="484d7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="484d7-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="484d7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="484d7-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="484d7-144">INPUTS</span></span>

### <span data-ttu-id="484d7-145">System.String</span><span class="sxs-lookup"><span data-stu-id="484d7-145">System.String</span></span>

### <span data-ttu-id="484d7-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="484d7-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="484d7-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="484d7-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="484d7-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="484d7-148">OUTPUTS</span></span>

### <span data-ttu-id="484d7-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="484d7-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="484d7-150">Notas</span><span class="sxs-lookup"><span data-stu-id="484d7-150">NOTES</span></span>

## <span data-ttu-id="484d7-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="484d7-151">RELATED LINKS</span></span>
