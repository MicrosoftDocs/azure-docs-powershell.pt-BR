---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 6340db7446671660df08449529b6678cf79a2af9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115319"
---
# <span data-ttu-id="446af-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="446af-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="446af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="446af-102">SYNOPSIS</span></span>
<span data-ttu-id="446af-103">Cria um novo domínio de grade de evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="446af-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="446af-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="446af-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="446af-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="446af-105">DESCRIPTION</span></span>
<span data-ttu-id="446af-106">Cria um novo domínio de grade de evento do Azure.</span><span class="sxs-lookup"><span data-stu-id="446af-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="446af-107">Depois que o domínio é criado, um aplicativo pode publicar eventos no ponto de extremidade do tópico.</span><span class="sxs-lookup"><span data-stu-id="446af-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="446af-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="446af-108">EXAMPLES</span></span>

### <span data-ttu-id="446af-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="446af-109">Example 1</span></span>

<span data-ttu-id="446af-110">Cria um domínio de Grade de Evento1 no westus2 da localização geográfica especificada, no grupo de recursos \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="446af-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="446af-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="446af-111">Example 2</span></span>

<span data-ttu-id="446af-112">Cria um domínio de Grade de Eventos1 na localização geográfica especificada westus2, no grupo de recursos \` \` \` \` \` MyResourceGroupName com as marcas especificadas \` "Departamento" e "Ambiente".</span><span class="sxs-lookup"><span data-stu-id="446af-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="446af-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="446af-113">PARAMETERS</span></span>

### <span data-ttu-id="446af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="446af-114">-DefaultProfile</span></span>
<span data-ttu-id="446af-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="446af-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="446af-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="446af-116">-InboundIpRule</span></span>
<span data-ttu-id="446af-117">Hashtable, que representa a lista de regras de IP de entrada.</span><span class="sxs-lookup"><span data-stu-id="446af-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="446af-118">Cada regra especifica o Endereço IP na notação CIDR, por exemplo, 10.0.0.0/8 juntamente com a Ação correspondente a ser executada com base na combinação ou nenhuma correspondente da IpMask.</span><span class="sxs-lookup"><span data-stu-id="446af-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="446af-119">Os valores possíveis de Ação incluem Permitir somente</span><span class="sxs-lookup"><span data-stu-id="446af-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="446af-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="446af-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="446af-121">Tabela hash que representa os campos de mapeamento de entrada com valor padrão no formato de espaço separado = formato de valor.</span><span class="sxs-lookup"><span data-stu-id="446af-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="446af-122">Os nomes de chave permitidos são: assunto, tipo de evento e dataversion.</span><span class="sxs-lookup"><span data-stu-id="446af-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="446af-123">Isso é usado quando InputSchemaHelp é somente customeventschema.</span><span class="sxs-lookup"><span data-stu-id="446af-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="446af-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="446af-124">-InputMappingField</span></span>
<span data-ttu-id="446af-125">Hashtable, que representa os campos de mapeamento de entrada na tecla de espaço separada = formato de valor.</span><span class="sxs-lookup"><span data-stu-id="446af-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="446af-126">Os nomes de chave permitidos são: id, tópico, eventtime, assunto, tipo de evento e dataversion.</span><span class="sxs-lookup"><span data-stu-id="446af-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="446af-127">Isso é usado quando InputSchemaHelp é somente customeventschema.</span><span class="sxs-lookup"><span data-stu-id="446af-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="446af-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="446af-128">-InputSchema</span></span>
<span data-ttu-id="446af-129">O esquema dos eventos de entrada para o tópico.</span><span class="sxs-lookup"><span data-stu-id="446af-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="446af-130">Os valores permitidos são: eventgridschema, customeventschema ou cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="446af-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="446af-131">O valor padrão é eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="446af-131">Default value is eventgridschema.</span></span> <span data-ttu-id="446af-132">Observe que, se customeventschema for especificado, os parâmetros InputMappingField ou/e InputMappingDefaultValue também precisarão ser especificados.</span><span class="sxs-lookup"><span data-stu-id="446af-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="446af-133">-Local</span><span class="sxs-lookup"><span data-stu-id="446af-133">-Location</span></span>
<span data-ttu-id="446af-134">O local do domínio.</span><span class="sxs-lookup"><span data-stu-id="446af-134">The location of the domain.</span></span>

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

### <span data-ttu-id="446af-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="446af-135">-Name</span></span>
<span data-ttu-id="446af-136">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="446af-136">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="446af-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="446af-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="446af-138">Isso determina se o tráfego é permitido pela rede pública.</span><span class="sxs-lookup"><span data-stu-id="446af-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="446af-139">Por padrão, ela está habilitada.</span><span class="sxs-lookup"><span data-stu-id="446af-139">By default it is enabled.</span></span> <span data-ttu-id="446af-140">Você pode restringir ainda mais a IPs específicos configurando parâmetros InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="446af-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="446af-141">Os valores permitidos são desabilitados e habilitados.</span><span class="sxs-lookup"><span data-stu-id="446af-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="446af-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="446af-142">-ResourceGroupName</span></span>
<span data-ttu-id="446af-143">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="446af-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="446af-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="446af-144">-Tag</span></span>
<span data-ttu-id="446af-145">Hashtable, que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="446af-145">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="446af-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="446af-146">-Confirm</span></span>
<span data-ttu-id="446af-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="446af-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="446af-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="446af-148">-WhatIf</span></span>
<span data-ttu-id="446af-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="446af-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="446af-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="446af-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="446af-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="446af-151">CommonParameters</span></span>
<span data-ttu-id="446af-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="446af-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="446af-153">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="446af-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="446af-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="446af-154">INPUTS</span></span>

### <span data-ttu-id="446af-155">System.String</span><span class="sxs-lookup"><span data-stu-id="446af-155">System.String</span></span>

### <span data-ttu-id="446af-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="446af-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="446af-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="446af-157">OUTPUTS</span></span>

### <span data-ttu-id="446af-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="446af-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="446af-159">Notas</span><span class="sxs-lookup"><span data-stu-id="446af-159">NOTES</span></span>

## <span data-ttu-id="446af-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="446af-160">RELATED LINKS</span></span>
