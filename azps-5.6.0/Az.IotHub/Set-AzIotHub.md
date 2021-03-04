---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 5be94896aeb4217e3c2f9da700e0f59032473296
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890402"
---
# <span data-ttu-id="e753f-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="e753f-101">Set-AzIotHub</span></span>

## <span data-ttu-id="e753f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e753f-102">SYNOPSIS</span></span>
<span data-ttu-id="e753f-103">Atualiza as propriedades de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="e753f-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="e753f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e753f-104">SYNTAX</span></span>

### <span data-ttu-id="e753f-105">UpdateSku (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e753f-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e753f-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="e753f-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e753f-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="e753f-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e753f-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="e753f-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e753f-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="e753f-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e753f-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="e753f-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e753f-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="e753f-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e753f-112">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e753f-112">DESCRIPTION</span></span>
<span data-ttu-id="e753f-113">Atualiza as propriedades de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="e753f-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="e753f-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e753f-114">EXAMPLES</span></span>

### <span data-ttu-id="e753f-115">Exemplo 1 Atualizar o sku</span><span class="sxs-lookup"><span data-stu-id="e753f-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="e753f-116">Atualize o sku para S1 e unidades para 5 para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e753f-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="e753f-117">Exemplo 2 Atualizar as propriedades eventhub</span><span class="sxs-lookup"><span data-stu-id="e753f-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="e753f-118">Atualize o tempo de retenção da telemetria em dias para 4 para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e753f-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e753f-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e753f-119">PARAMETERS</span></span>

### <span data-ttu-id="e753f-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="e753f-120">-CloudToDevice</span></span>
<span data-ttu-id="e753f-121">As propriedades da fila de comando nuvem para dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e753f-121">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e753f-122">-DefaultProfile</span></span>
<span data-ttu-id="e753f-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e753f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e753f-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="e753f-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="e753f-125">Sinalizador que especifica se as notificações devem ser habilitadas para carregamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e753f-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="e753f-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="e753f-127">Tempo de retenção em dias.</span><span class="sxs-lookup"><span data-stu-id="e753f-127">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="e753f-128">-FallbackRoute</span></span>
<span data-ttu-id="e753f-129">Rota de fallback para roteamento</span><span class="sxs-lookup"><span data-stu-id="e753f-129">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="e753f-130">-FileUploadContainerName</span></span>
<span data-ttu-id="e753f-131">O nome do contêiner para o que carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="e753f-131">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="e753f-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="e753f-133">A contagem máxima de entrega para notificações de carregamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e753f-133">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="e753f-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="e753f-135">Tempo de vida para as mensagens na fila de notificação de carregamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e753f-135">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="e753f-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="e753f-137">Tempo de vida para o Uri do SAS gerado para carregamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e753f-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="e753f-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="e753f-139">A cadeia de conexão de armazenamento para carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="e753f-139">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-140">-Name</span><span class="sxs-lookup"><span data-stu-id="e753f-140">-Name</span></span>
<span data-ttu-id="e753f-141">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="e753f-141">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e753f-142">-ResourceGroupName</span></span>
<span data-ttu-id="e753f-143">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e753f-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-144">-Routes</span><span class="sxs-lookup"><span data-stu-id="e753f-144">-Routes</span></span>
<span data-ttu-id="e753f-145">Rotas a serem adicionadas para Roteamento</span><span class="sxs-lookup"><span data-stu-id="e753f-145">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="e753f-146">-RoutingProperties</span></span>
<span data-ttu-id="e753f-147">As propriedades de roteamento de mensagens para pontos de extremidade externos</span><span class="sxs-lookup"><span data-stu-id="e753f-147">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e753f-148">-SkuName</span></span>
<span data-ttu-id="e753f-149">Nome do Sku.</span><span class="sxs-lookup"><span data-stu-id="e753f-149">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-150">-Units</span><span class="sxs-lookup"><span data-stu-id="e753f-150">-Units</span></span>
<span data-ttu-id="e753f-151">Número de unidades</span><span class="sxs-lookup"><span data-stu-id="e753f-151">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e753f-152">-Confirm</span></span>
<span data-ttu-id="e753f-153">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e753f-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e753f-154">-WhatIf</span></span>
<span data-ttu-id="e753f-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e753f-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e753f-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e753f-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e753f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e753f-157">CommonParameters</span></span>
<span data-ttu-id="e753f-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e753f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e753f-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e753f-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e753f-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e753f-160">INPUTS</span></span>

### <span data-ttu-id="e753f-161">System.String</span><span class="sxs-lookup"><span data-stu-id="e753f-161">System.String</span></span>

## <span data-ttu-id="e753f-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e753f-162">OUTPUTS</span></span>

### <span data-ttu-id="e753f-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e753f-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="e753f-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="e753f-164">NOTES</span></span>

## <span data-ttu-id="e753f-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e753f-165">RELATED LINKS</span></span>
