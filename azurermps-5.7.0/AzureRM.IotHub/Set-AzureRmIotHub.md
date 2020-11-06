---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: a9005819bb78e5393f3a617dd18886309d3defc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610947"
---
# <span data-ttu-id="bfb87-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="bfb87-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="bfb87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfb87-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb87-103">Atualiza as propriedades de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="bfb87-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfb87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfb87-104">SYNTAX</span></span>

### <span data-ttu-id="bfb87-105">UpdateSku (padrão)</span><span class="sxs-lookup"><span data-stu-id="bfb87-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb87-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="bfb87-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb87-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="bfb87-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb87-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="bfb87-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb87-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="bfb87-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb87-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="bfb87-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb87-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="bfb87-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb87-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="bfb87-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfb87-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfb87-113">DESCRIPTION</span></span>
<span data-ttu-id="bfb87-114">Atualiza as propriedades de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="bfb87-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="bfb87-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfb87-115">EXAMPLES</span></span>

### <span data-ttu-id="bfb87-116">Exemplo 1 atualize a SKU</span><span class="sxs-lookup"><span data-stu-id="bfb87-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="bfb87-117">Atualize a SKU para S1 e as unidades para 5 para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="bfb87-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="bfb87-118">Exemplo 2 atualizar as propriedades do eventhub</span><span class="sxs-lookup"><span data-stu-id="bfb87-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="bfb87-119">Atualize o tempo de retenção em dias a 4 para os eventos telemetria e operationsmonitoringevents para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="bfb87-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="bfb87-120">OS</span><span class="sxs-lookup"><span data-stu-id="bfb87-120">PARAMETERS</span></span>

### <span data-ttu-id="bfb87-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="bfb87-121">-CloudToDevice</span></span>
<span data-ttu-id="bfb87-122">As propriedades da fila do comando nuvem para dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfb87-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb87-123">-DefaultProfile</span></span>
<span data-ttu-id="bfb87-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bfb87-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="bfb87-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="bfb87-126">Sinalizador que especifica se as notificações devem ser habilitadas para o carregamento do arquivo.</span><span class="sxs-lookup"><span data-stu-id="bfb87-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="bfb87-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="bfb87-128">Tempo de retenção em dias.</span><span class="sxs-lookup"><span data-stu-id="bfb87-128">Retention time in days.</span></span> 

```yaml
Type: Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="bfb87-129">-FallbackRoute</span></span>
<span data-ttu-id="bfb87-130">Rota de fallback para roteamento</span><span class="sxs-lookup"><span data-stu-id="bfb87-130">Fallback Route for Routing</span></span>

```yaml
Type: PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="bfb87-131">-FileUploadContainerName</span></span>
<span data-ttu-id="bfb87-132">O nome do contêiner para o qual carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="bfb87-132">The name of the container to upload the files to.</span></span>

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="bfb87-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="bfb87-134">A contagem máxima de entrega para notificações de carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="bfb87-134">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: Int32
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="bfb87-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="bfb87-136">Valor de vida útil para as mensagens na fila de notificação de carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="bfb87-136">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="bfb87-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="bfb87-138">Tempo de vida para o URI da SAS gerado para o carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="bfb87-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="bfb87-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="bfb87-140">A cadeia de conexão de armazenamento para a qual carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="bfb87-140">The storage connection string to upload the files to.</span></span> 

```yaml
Type: String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfb87-141">-Name</span></span>
<span data-ttu-id="bfb87-142">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="bfb87-142">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="bfb87-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="bfb87-144">As propriedades relacionadas ao monitoramento de operações.</span><span class="sxs-lookup"><span data-stu-id="bfb87-144">The properties related to operations monitoring.</span></span> 

```yaml
Type: PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb87-145">-ResourceGroupName</span></span>
<span data-ttu-id="bfb87-146">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bfb87-146">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-147">-Rotas</span><span class="sxs-lookup"><span data-stu-id="bfb87-147">-Routes</span></span>
<span data-ttu-id="bfb87-148">Rotas a serem adicionadas para roteamento</span><span class="sxs-lookup"><span data-stu-id="bfb87-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="bfb87-149">-Routingproperties</span><span class="sxs-lookup"><span data-stu-id="bfb87-149">-RoutingProperties</span></span>
<span data-ttu-id="bfb87-150">As propriedades de roteamento para direcionar mensagens para pontos de extremidade externos</span><span class="sxs-lookup"><span data-stu-id="bfb87-150">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bfb87-151">-SkuName</span></span>
<span data-ttu-id="bfb87-152">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="bfb87-152">Name of the Sku.</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-153">-Unidades</span><span class="sxs-lookup"><span data-stu-id="bfb87-153">-Units</span></span>
<span data-ttu-id="bfb87-154">Número de unidades</span><span class="sxs-lookup"><span data-stu-id="bfb87-154">Number of Units</span></span>

```yaml
Type: Int64
Parameter Sets: UpdateSku
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bfb87-155">-Confirm</span></span>
<span data-ttu-id="bfb87-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb87-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb87-157">-WhatIf</span></span>
<span data-ttu-id="bfb87-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bfb87-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfb87-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfb87-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb87-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb87-160">CommonParameters</span></span>
<span data-ttu-id="bfb87-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb87-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb87-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb87-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb87-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfb87-163">INPUTS</span></span>

### <span data-ttu-id="bfb87-164">System. String</span><span class="sxs-lookup"><span data-stu-id="bfb87-164">System.String</span></span>
<span data-ttu-id="bfb87-165">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties Microsoft. Azure. Commands. Management. IotHub. Models. PSOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="bfb87-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="bfb87-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfb87-166">OUTPUTS</span></span>

### <span data-ttu-id="bfb87-167">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bfb87-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="bfb87-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfb87-168">NOTES</span></span>

## <span data-ttu-id="bfb87-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfb87-169">RELATED LINKS</span></span>

