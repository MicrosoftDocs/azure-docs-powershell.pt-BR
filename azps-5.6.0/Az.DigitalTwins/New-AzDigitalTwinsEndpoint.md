---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 3c59099a2e4440e2c92836ab02b8396b5fc3b207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889514"
---
# <span data-ttu-id="cf659-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf659-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="cf659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf659-102">SYNOPSIS</span></span>
<span data-ttu-id="cf659-103">Criar ou atualizar o ponto de extremidade DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="cf659-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="cf659-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cf659-104">SYNTAX</span></span>

### <span data-ttu-id="cf659-105">EventHub (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cf659-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf659-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="cf659-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf659-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cf659-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf659-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cf659-108">DESCRIPTION</span></span>
<span data-ttu-id="cf659-109">Criar ou atualizar o ponto de extremidade DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="cf659-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="cf659-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf659-110">EXAMPLES</span></span>

### <span data-ttu-id="cf659-111">Exemplo 1: Criar um AzDigitalTwinsEndpoint para Eventhub</span><span class="sxs-lookup"><span data-stu-id="cf659-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="cf659-112">Criar um AzDigitalTwinsEndpoint para Eventhub por connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="cf659-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="cf659-113">Exemplo 2: Criar um AzDigitalTwinsEndpoint para EventGrid</span><span class="sxs-lookup"><span data-stu-id="cf659-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="cf659-114">Criar um AzDigitalTwinsEndpoint para Eventhub por TopicEndpoint e accessKey1</span><span class="sxs-lookup"><span data-stu-id="cf659-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="cf659-115">Exemplo 3: Criar um AzDigitalTwinsEndpoint para ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cf659-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="cf659-116">Criar um AzDigitalTwinsEndpoint para ServicBus por PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="cf659-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="cf659-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cf659-117">PARAMETERS</span></span>

### <span data-ttu-id="cf659-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="cf659-118">-AccessKey1</span></span>
<span data-ttu-id="cf659-119">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cf659-119">The subscription identifier.</span></span>

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

### <span data-ttu-id="cf659-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf659-120">-AsJob</span></span>
<span data-ttu-id="cf659-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="cf659-121">Run the command as a job</span></span>

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

### <span data-ttu-id="cf659-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="cf659-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="cf659-123">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cf659-123">The subscription identifier.</span></span>

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

### <span data-ttu-id="cf659-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="cf659-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="cf659-125">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cf659-125">The subscription identifier.</span></span>

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

### <span data-ttu-id="cf659-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="cf659-126">-DeadLetterSecret</span></span>
<span data-ttu-id="cf659-127">Segredo de armazenamento de carta morta.</span><span class="sxs-lookup"><span data-stu-id="cf659-127">Dead letter storage secret.</span></span>
<span data-ttu-id="cf659-128">Será ofuscado durante a leitura.</span><span class="sxs-lookup"><span data-stu-id="cf659-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="cf659-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf659-129">-DefaultProfile</span></span>
<span data-ttu-id="cf659-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf659-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf659-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="cf659-131">-EndpointDescription</span></span>
<span data-ttu-id="cf659-132">Recurso de ponto de extremidade DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="cf659-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="cf659-133">Para construir, consulte a seção NOTES para propriedades ENDPOINTDESCRIPTION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cf659-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf659-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cf659-134">-EndpointName</span></span>
<span data-ttu-id="cf659-135">Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="cf659-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="cf659-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="cf659-136">-EndpointType</span></span>
<span data-ttu-id="cf659-137">O tipo de ponto de extremidade de Digital Twins</span><span class="sxs-lookup"><span data-stu-id="cf659-137">The type of Digital Twins endpoint</span></span>

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

### <span data-ttu-id="cf659-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cf659-138">-NoWait</span></span>
<span data-ttu-id="cf659-139">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="cf659-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cf659-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="cf659-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="cf659-141">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cf659-141">The subscription identifier.</span></span>

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

### <span data-ttu-id="cf659-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf659-142">-ResourceGroupName</span></span>
<span data-ttu-id="cf659-143">O nome do grupo de recursos que contém DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="cf659-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="cf659-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cf659-144">-ResourceName</span></span>
<span data-ttu-id="cf659-145">O nome do DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="cf659-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="cf659-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf659-146">-SubscriptionId</span></span>
<span data-ttu-id="cf659-147">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cf659-147">The subscription identifier.</span></span>

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

### <span data-ttu-id="cf659-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf659-148">-TopicEndpoint</span></span>
<span data-ttu-id="cf659-149">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="cf659-149">The subscription identifier.</span></span>

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

### <span data-ttu-id="cf659-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf659-150">-Confirm</span></span>
<span data-ttu-id="cf659-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf659-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf659-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf659-152">-WhatIf</span></span>
<span data-ttu-id="cf659-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf659-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf659-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf659-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf659-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf659-155">CommonParameters</span></span>
<span data-ttu-id="cf659-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf659-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf659-157">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf659-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf659-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf659-158">INPUTS</span></span>

### <span data-ttu-id="cf659-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="cf659-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="cf659-160">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cf659-160">OUTPUTS</span></span>

### <span data-ttu-id="cf659-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="cf659-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="cf659-162">NOTES</span><span class="sxs-lookup"><span data-stu-id="cf659-162">NOTES</span></span>

<span data-ttu-id="cf659-163">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cf659-163">ALIASES</span></span>

<span data-ttu-id="cf659-164">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="cf659-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf659-165">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="cf659-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf659-166">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf659-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf659-167">ENDPOINTDESCRIPTION : Recurso de ponto de extremidade <IDigitalTwinsEndpointResource> DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="cf659-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="cf659-168">`EndpointType <EndpointType>`: O tipo de ponto de extremidade do Digital Twins</span><span class="sxs-lookup"><span data-stu-id="cf659-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="cf659-169">`[DeadLetterSecret <String>]`: Segredo de armazenamento de carta morta.</span><span class="sxs-lookup"><span data-stu-id="cf659-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="cf659-170">Será ofuscado durante a leitura.</span><span class="sxs-lookup"><span data-stu-id="cf659-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="cf659-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf659-171">RELATED LINKS</span></span>

