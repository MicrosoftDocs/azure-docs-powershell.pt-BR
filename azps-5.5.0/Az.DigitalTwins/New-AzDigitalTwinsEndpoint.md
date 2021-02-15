---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6b2c51d21b40745d3dd4dd2db71604fa01a5a6cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115329"
---
# <span data-ttu-id="c14b3-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="c14b3-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="c14b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c14b3-102">SYNOPSIS</span></span>
<span data-ttu-id="c14b3-103">Criar ou atualizar o ponto de extremidade DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c14b3-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="c14b3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c14b3-104">SYNTAX</span></span>

### <span data-ttu-id="c14b3-105">EventHub (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c14b3-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c14b3-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="c14b3-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c14b3-107">Servicebus</span><span class="sxs-lookup"><span data-stu-id="c14b3-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c14b3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c14b3-108">DESCRIPTION</span></span>
<span data-ttu-id="c14b3-109">Criar ou atualizar o ponto de extremidade DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c14b3-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="c14b3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c14b3-110">EXAMPLES</span></span>

### <span data-ttu-id="c14b3-111">Exemplo 1: Criar um AzDigitalTwinsEndpoint para Eventhub</span><span class="sxs-lookup"><span data-stu-id="c14b3-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="c14b3-112">Criar um AzDigitalTwinsEndpoint para Eventhub por conexãoStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c14b3-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="c14b3-113">Exemplo 2: Criar um AzDigitalTwinsEndpoint para EventGrid</span><span class="sxs-lookup"><span data-stu-id="c14b3-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="c14b3-114">Criar um AzDigitalTwinsEndpoint para Eventhub por TopicEndpoint e accessKey1</span><span class="sxs-lookup"><span data-stu-id="c14b3-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="c14b3-115">Exemplo 3: Criar um AzDigitalTwinsEndpoint para ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c14b3-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="c14b3-116">Criar um AzDigitalTwinsEndpoint para ServicBus pela PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="c14b3-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="c14b3-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c14b3-117">PARAMETERS</span></span>

### <span data-ttu-id="c14b3-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="c14b3-118">-AccessKey1</span></span>
<span data-ttu-id="c14b3-119">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c14b3-119">The subscription identifier.</span></span>

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

### <span data-ttu-id="c14b3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c14b3-120">-AsJob</span></span>
<span data-ttu-id="c14b3-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c14b3-121">Run the command as a job</span></span>

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

### <span data-ttu-id="c14b3-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c14b3-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="c14b3-123">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c14b3-123">The subscription identifier.</span></span>

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

### <span data-ttu-id="c14b3-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="c14b3-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="c14b3-125">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c14b3-125">The subscription identifier.</span></span>

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

### <span data-ttu-id="c14b3-126">-DeadLetterSecsec</span><span class="sxs-lookup"><span data-stu-id="c14b3-126">-DeadLetterSecret</span></span>
<span data-ttu-id="c14b3-127">Segredo de armazenamento de cartas mortos.</span><span class="sxs-lookup"><span data-stu-id="c14b3-127">Dead letter storage secret.</span></span>
<span data-ttu-id="c14b3-128">Serão ofuscados durante a leitura.</span><span class="sxs-lookup"><span data-stu-id="c14b3-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="c14b3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14b3-129">-DefaultProfile</span></span>
<span data-ttu-id="c14b3-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c14b3-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c14b3-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="c14b3-131">-EndpointDescription</span></span>
<span data-ttu-id="c14b3-132">Recurso de ponto de extremidade DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c14b3-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="c14b3-133">Para construir, consulte a seção ANOTAÇÕES para propriedades ENDPOINTDESCRIPTION e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="c14b3-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="c14b3-134">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="c14b3-134">-EndpointName</span></span>
<span data-ttu-id="c14b3-135">Nome do Recurso do Ponto de Extremidade.</span><span class="sxs-lookup"><span data-stu-id="c14b3-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="c14b3-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="c14b3-136">-EndpointType</span></span>
<span data-ttu-id="c14b3-137">O tipo de ponto de extremidade Digital Descarrém</span><span class="sxs-lookup"><span data-stu-id="c14b3-137">The type of Digital Twins endpoint</span></span>

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

### <span data-ttu-id="c14b3-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c14b3-138">-NoWait</span></span>
<span data-ttu-id="c14b3-139">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="c14b3-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c14b3-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="c14b3-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="c14b3-141">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c14b3-141">The subscription identifier.</span></span>

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

### <span data-ttu-id="c14b3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c14b3-142">-ResourceGroupName</span></span>
<span data-ttu-id="c14b3-143">O nome do grupo de recursos que contém a DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c14b3-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="c14b3-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c14b3-144">-ResourceName</span></span>
<span data-ttu-id="c14b3-145">O nome da DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c14b3-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="c14b3-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c14b3-146">-SubscriptionId</span></span>
<span data-ttu-id="c14b3-147">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c14b3-147">The subscription identifier.</span></span>

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

### <span data-ttu-id="c14b3-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="c14b3-148">-TopicEndpoint</span></span>
<span data-ttu-id="c14b3-149">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c14b3-149">The subscription identifier.</span></span>

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

### <span data-ttu-id="c14b3-150">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c14b3-150">-Confirm</span></span>
<span data-ttu-id="c14b3-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c14b3-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c14b3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c14b3-152">-WhatIf</span></span>
<span data-ttu-id="c14b3-153">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c14b3-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c14b3-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c14b3-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c14b3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14b3-155">CommonParameters</span></span>
<span data-ttu-id="c14b3-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c14b3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14b3-157">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c14b3-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14b3-158">Entradas</span><span class="sxs-lookup"><span data-stu-id="c14b3-158">INPUTS</span></span>

### <span data-ttu-id="c14b3-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="c14b3-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="c14b3-160">Saídas</span><span class="sxs-lookup"><span data-stu-id="c14b3-160">OUTPUTS</span></span>

### <span data-ttu-id="c14b3-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="c14b3-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="c14b3-162">Notas</span><span class="sxs-lookup"><span data-stu-id="c14b3-162">NOTES</span></span>

<span data-ttu-id="c14b3-163">Aliases</span><span class="sxs-lookup"><span data-stu-id="c14b3-163">ALIASES</span></span>

<span data-ttu-id="c14b3-164">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="c14b3-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c14b3-165">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c14b3-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c14b3-166">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c14b3-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c14b3-167">ENDPOINTDESCRIPTION : Recurso de ponto de extremidade <IDigitalTwinsEndpointResource> DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c14b3-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="c14b3-168">`EndpointType <EndpointType>`: o tipo de ponto de extremidade Digital Descarrém</span><span class="sxs-lookup"><span data-stu-id="c14b3-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="c14b3-169">`[DeadLetterSecret <String>]`: segredo de armazenamento de cartas mortos.</span><span class="sxs-lookup"><span data-stu-id="c14b3-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="c14b3-170">Serão ofuscados durante a leitura.</span><span class="sxs-lookup"><span data-stu-id="c14b3-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="c14b3-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c14b3-171">RELATED LINKS</span></span>

