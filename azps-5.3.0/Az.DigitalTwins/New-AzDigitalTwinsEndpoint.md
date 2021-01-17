---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6b2c51d21b40745d3dd4dd2db71604fa01a5a6cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426997"
---
# <span data-ttu-id="39287-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="39287-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="39287-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39287-102">SYNOPSIS</span></span>
<span data-ttu-id="39287-103">Crie ou atualize o ponto de extremidade DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="39287-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="39287-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39287-104">SYNTAX</span></span>

### <span data-ttu-id="39287-105">EventHub (padrão)</span><span class="sxs-lookup"><span data-stu-id="39287-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39287-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="39287-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39287-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39287-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39287-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39287-108">DESCRIPTION</span></span>
<span data-ttu-id="39287-109">Crie ou atualize o ponto de extremidade DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="39287-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="39287-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39287-110">EXAMPLES</span></span>

### <span data-ttu-id="39287-111">Exemplo 1: criar um AzDigitalTwinsEndpoint para o Eventhub</span><span class="sxs-lookup"><span data-stu-id="39287-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="39287-112">Criar um AzDigitalTwinsEndpoint para o Eventhub pela connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="39287-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="39287-113">Exemplo 2: criar um AzDigitalTwinsEndpoint para EventGrid</span><span class="sxs-lookup"><span data-stu-id="39287-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="39287-114">Criar um AzDigitalTwinsEndpoint para o Eventhub pelo TopicEndpoint e pelo accessKey1</span><span class="sxs-lookup"><span data-stu-id="39287-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="39287-115">Exemplo 3: criar um AzDigitalTwinsEndpoint para o ServiceBus</span><span class="sxs-lookup"><span data-stu-id="39287-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="39287-116">Criar um AzDigitalTwinsEndpoint para ServicBus por PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="39287-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="39287-117">OS</span><span class="sxs-lookup"><span data-stu-id="39287-117">PARAMETERS</span></span>

### <span data-ttu-id="39287-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="39287-118">-AccessKey1</span></span>
<span data-ttu-id="39287-119">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="39287-119">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39287-120">-AsJob</span></span>
<span data-ttu-id="39287-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="39287-121">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="39287-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="39287-123">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="39287-123">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="39287-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="39287-125">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="39287-125">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="39287-126">-DeadLetterSecret</span></span>
<span data-ttu-id="39287-127">Segredo do armazenamento de carta de inatividade.</span><span class="sxs-lookup"><span data-stu-id="39287-127">Dead letter storage secret.</span></span>
<span data-ttu-id="39287-128">Serão ofuscados durante a leitura.</span><span class="sxs-lookup"><span data-stu-id="39287-128">Will be obfuscated during read.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39287-129">-DefaultProfile</span></span>
<span data-ttu-id="39287-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39287-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="39287-131">-EndpointDescription</span></span>
<span data-ttu-id="39287-132">Recurso de ponto de extremidade DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="39287-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="39287-133">Para construir, consulte a seção notas para propriedades ENDPOINTDESCRIPTION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="39287-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39287-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="39287-134">-EndpointName</span></span>
<span data-ttu-id="39287-135">Nome do recurso de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="39287-135">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="39287-136">-EndpointType</span></span>
<span data-ttu-id="39287-137">O tipo de ponto de extremidade Twins digital</span><span class="sxs-lookup"><span data-stu-id="39287-137">The type of Digital Twins endpoint</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Support.EndpointType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="39287-138">-NoWait</span></span>
<span data-ttu-id="39287-139">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="39287-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="39287-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="39287-141">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="39287-141">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceBus
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39287-142">-ResourceGroupName</span></span>
<span data-ttu-id="39287-143">O nome do grupo de recursos que contém o DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="39287-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="39287-144">-ResourceName</span></span>
<span data-ttu-id="39287-145">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="39287-145">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39287-146">-SubscriptionId</span></span>
<span data-ttu-id="39287-147">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="39287-147">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="39287-148">-TopicEndpoint</span></span>
<span data-ttu-id="39287-149">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="39287-149">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39287-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="39287-150">-Confirm</span></span>
<span data-ttu-id="39287-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39287-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39287-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39287-152">-WhatIf</span></span>
<span data-ttu-id="39287-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="39287-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39287-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39287-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39287-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39287-155">CommonParameters</span></span>
<span data-ttu-id="39287-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39287-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39287-157">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39287-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39287-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39287-158">INPUTS</span></span>

### <span data-ttu-id="39287-159">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="39287-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="39287-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39287-160">OUTPUTS</span></span>

### <span data-ttu-id="39287-161">Microsoft. Azure. PowerShell. cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="39287-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="39287-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39287-162">NOTES</span></span>

<span data-ttu-id="39287-163">ALIASES</span><span class="sxs-lookup"><span data-stu-id="39287-163">ALIASES</span></span>

<span data-ttu-id="39287-164">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="39287-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39287-165">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="39287-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39287-166">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39287-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39287-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource> : DigitalTwinsInstance recurso de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="39287-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="39287-168">`EndpointType <EndpointType>`: O tipo de ponto de extremidade Twins digital</span><span class="sxs-lookup"><span data-stu-id="39287-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="39287-169">`[DeadLetterSecret <String>]`: Segredo de armazenamento de letra de inatividade.</span><span class="sxs-lookup"><span data-stu-id="39287-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="39287-170">Serão ofuscados durante a leitura.</span><span class="sxs-lookup"><span data-stu-id="39287-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="39287-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39287-171">RELATED LINKS</span></span>

