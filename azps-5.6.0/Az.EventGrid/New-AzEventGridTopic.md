---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: df81f976f571a59f68d51ef734f1bc3ea5536015
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890415"
---
# <span data-ttu-id="81b7e-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="81b7e-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="81b7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="81b7e-103">Cria um novo tópico de grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="81b7e-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="81b7e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="81b7e-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81b7e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="81b7e-105">DESCRIPTION</span></span>
<span data-ttu-id="81b7e-106">Cria um novo tópico de grade de eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="81b7e-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="81b7e-107">Depois que o tópico for criado, um aplicativo poderá publicar eventos no ponto de extremidade do tópico.</span><span class="sxs-lookup"><span data-stu-id="81b7e-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="81b7e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81b7e-108">EXAMPLES</span></span>

### <span data-ttu-id="81b7e-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81b7e-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="81b7e-110">Cria um tópico de Grade de Eventos Tópico1 no local geográfico especificado westus2 , no grupo de recursos \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="81b7e-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="81b7e-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="81b7e-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="81b7e-112">Cria um tópico de Grade de Eventos Tópico1 na localização geográfica especificada westus2 , no grupo de recursos MyResourceGroupName com as marcas \` \` \` \` \` \` especificadas "Department" e "Environment".</span><span class="sxs-lookup"><span data-stu-id="81b7e-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="81b7e-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="81b7e-113">PARAMETERS</span></span>

### <span data-ttu-id="81b7e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b7e-114">-DefaultProfile</span></span>
<span data-ttu-id="81b7e-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="81b7e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81b7e-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="81b7e-116">-InboundIpRule</span></span>
<span data-ttu-id="81b7e-117">Hashtable que representa a lista de regras ip de entrada.</span><span class="sxs-lookup"><span data-stu-id="81b7e-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="81b7e-118">Cada regra especifica o Endereço IP na notação CIDR, por exemplo, 10.0.0.0/8 juntamente com a Ação correspondente a ser executada com base na combinação ou não da combinação do IpMask.</span><span class="sxs-lookup"><span data-stu-id="81b7e-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="81b7e-119">Os valores de ação possíveis incluem Permitir somente</span><span class="sxs-lookup"><span data-stu-id="81b7e-119">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81b7e-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="81b7e-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="81b7e-121">Hashtable que representa os campos de mapeamento de entrada com valor padrão no espaço separado chave = formato de valor.</span><span class="sxs-lookup"><span data-stu-id="81b7e-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="81b7e-122">Os nomes de chave permitidos são: subject, eventtype e dataversion.</span><span class="sxs-lookup"><span data-stu-id="81b7e-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="81b7e-123">Isso é usado quando InputSchemaHelp é customeventschema somente.</span><span class="sxs-lookup"><span data-stu-id="81b7e-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81b7e-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="81b7e-124">-InputMappingField</span></span>
<span data-ttu-id="81b7e-125">Hashtable que representa os campos de mapeamento de entrada em chave separada de espaço = formato de valor.</span><span class="sxs-lookup"><span data-stu-id="81b7e-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="81b7e-126">Os nomes de chave permitidos são: id, tópico, eventtime, subject, eventtype e dataversion.</span><span class="sxs-lookup"><span data-stu-id="81b7e-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="81b7e-127">Isso é usado quando InputSchemaHelp é customeventschema somente.</span><span class="sxs-lookup"><span data-stu-id="81b7e-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81b7e-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="81b7e-128">-InputSchema</span></span>
<span data-ttu-id="81b7e-129">O esquema dos eventos de entrada do tópico.</span><span class="sxs-lookup"><span data-stu-id="81b7e-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="81b7e-130">Os valores permitidos são: eventgridschema, customeventschema ou cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="81b7e-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="81b7e-131">O valor padrão é eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="81b7e-131">Default value is eventgridschema.</span></span> <span data-ttu-id="81b7e-132">Observe que, se customeventschema for especificado, os parâmetros InputMappingField ou/e InputMappingDefaultValue também precisarão ser especificados.</span><span class="sxs-lookup"><span data-stu-id="81b7e-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81b7e-133">-Location</span><span class="sxs-lookup"><span data-stu-id="81b7e-133">-Location</span></span>
<span data-ttu-id="81b7e-134">O local do tópico</span><span class="sxs-lookup"><span data-stu-id="81b7e-134">The location of the topic</span></span>

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

### <span data-ttu-id="81b7e-135">-Name</span><span class="sxs-lookup"><span data-stu-id="81b7e-135">-Name</span></span>
<span data-ttu-id="81b7e-136">O nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="81b7e-136">The name of the topic.</span></span>

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

### <span data-ttu-id="81b7e-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="81b7e-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="81b7e-138">Isso determina se o tráfego é permitido em rede pública.</span><span class="sxs-lookup"><span data-stu-id="81b7e-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="81b7e-139">Por padrão, ele está habilitado.</span><span class="sxs-lookup"><span data-stu-id="81b7e-139">By default it is enabled.</span></span> <span data-ttu-id="81b7e-140">Você pode restringir ainda mais IPs específicos configurando parâmetros InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="81b7e-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="81b7e-141">Os valores permitidos estão desabilitados e habilitados.</span><span class="sxs-lookup"><span data-stu-id="81b7e-141">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81b7e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81b7e-142">-ResourceGroupName</span></span>
<span data-ttu-id="81b7e-143">O grupo de recursos no qual o tópico deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="81b7e-143">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="81b7e-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="81b7e-144">-Tag</span></span>
<span data-ttu-id="81b7e-145">Hashtables que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="81b7e-145">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81b7e-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81b7e-146">-Confirm</span></span>
<span data-ttu-id="81b7e-147">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b7e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81b7e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b7e-148">-WhatIf</span></span>
<span data-ttu-id="81b7e-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81b7e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81b7e-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81b7e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b7e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b7e-151">CommonParameters</span></span>
<span data-ttu-id="81b7e-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b7e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b7e-153">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81b7e-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b7e-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81b7e-154">INPUTS</span></span>

### <span data-ttu-id="81b7e-155">System.String</span><span class="sxs-lookup"><span data-stu-id="81b7e-155">System.String</span></span>

### <span data-ttu-id="81b7e-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="81b7e-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="81b7e-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="81b7e-157">OUTPUTS</span></span>

### <span data-ttu-id="81b7e-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="81b7e-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="81b7e-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="81b7e-159">NOTES</span></span>

## <span data-ttu-id="81b7e-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81b7e-160">RELATED LINKS</span></span>
