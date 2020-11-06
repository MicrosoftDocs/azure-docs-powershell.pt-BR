---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: aad54e42d628239f087e376eabe6b9950c07b6f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440645"
---
# <span data-ttu-id="d48af-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="d48af-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="d48af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d48af-102">SYNOPSIS</span></span>
<span data-ttu-id="d48af-103">Atualiza as propriedades de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="d48af-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d48af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d48af-104">SYNTAX</span></span>

### <span data-ttu-id="d48af-105">UpdateSku (padrão)</span><span class="sxs-lookup"><span data-stu-id="d48af-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d48af-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="d48af-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d48af-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="d48af-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d48af-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="d48af-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d48af-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="d48af-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d48af-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="d48af-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d48af-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="d48af-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d48af-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="d48af-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d48af-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d48af-113">DESCRIPTION</span></span>
<span data-ttu-id="d48af-114">Atualiza as propriedades de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="d48af-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="d48af-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d48af-115">EXAMPLES</span></span>

### <span data-ttu-id="d48af-116">Exemplo 1 atualize a SKU</span><span class="sxs-lookup"><span data-stu-id="d48af-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="d48af-117">Atualize a SKU para S1 e as unidades para 5 para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d48af-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="d48af-118">Exemplo 2 atualizar as propriedades do eventhub</span><span class="sxs-lookup"><span data-stu-id="d48af-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="d48af-119">Atualize o tempo de retenção em dias a 4 para os eventos telemetria e operationsmonitoringevents para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d48af-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d48af-120">OS</span><span class="sxs-lookup"><span data-stu-id="d48af-120">PARAMETERS</span></span>

### <span data-ttu-id="d48af-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="d48af-121">-CloudToDevice</span></span>
<span data-ttu-id="d48af-122">As propriedades da fila do comando nuvem para dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d48af-122">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="d48af-123">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="d48af-123">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="d48af-124">Sinalizador que especifica se as notificações devem ser habilitadas para o carregamento do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d48af-124">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="d48af-125">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="d48af-125">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="d48af-126">Tempo de retenção em dias.</span><span class="sxs-lookup"><span data-stu-id="d48af-126">Retention time in days.</span></span> 

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

### <span data-ttu-id="d48af-127">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="d48af-127">-FallbackRoute</span></span>
<span data-ttu-id="d48af-128">Rota de fallback para roteamento</span><span class="sxs-lookup"><span data-stu-id="d48af-128">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="d48af-129">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="d48af-129">-FileUploadContainerName</span></span>
<span data-ttu-id="d48af-130">O nome do contêiner para o qual carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="d48af-130">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="d48af-131">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="d48af-131">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="d48af-132">A contagem máxima de entrega para notificações de carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d48af-132">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="d48af-133">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="d48af-133">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="d48af-134">Valor de vida útil para as mensagens na fila de notificação de carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d48af-134">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="d48af-135">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="d48af-135">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="d48af-136">Tempo de vida para o URI da SAS gerado para o carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d48af-136">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="d48af-137">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="d48af-137">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="d48af-138">A cadeia de conexão de armazenamento para a qual carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="d48af-138">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="d48af-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="d48af-139">-Name</span></span>
<span data-ttu-id="d48af-140">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="d48af-140">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d48af-141">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="d48af-141">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="d48af-142">As propriedades relacionadas ao monitoramento de operações.</span><span class="sxs-lookup"><span data-stu-id="d48af-142">The properties related to operations monitoring.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d48af-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d48af-143">-ResourceGroupName</span></span>
<span data-ttu-id="d48af-144">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d48af-144">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d48af-145">-Rotas</span><span class="sxs-lookup"><span data-stu-id="d48af-145">-Routes</span></span>
<span data-ttu-id="d48af-146">Rotas a serem adicionadas para roteamento</span><span class="sxs-lookup"><span data-stu-id="d48af-146">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="d48af-147">-Routingproperties</span><span class="sxs-lookup"><span data-stu-id="d48af-147">-RoutingProperties</span></span>
<span data-ttu-id="d48af-148">As propriedades de roteamento para direcionar mensagens para pontos de extremidade externos</span><span class="sxs-lookup"><span data-stu-id="d48af-148">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="d48af-149">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d48af-149">-SkuName</span></span>
<span data-ttu-id="d48af-150">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="d48af-150">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d48af-151">-Unidades</span><span class="sxs-lookup"><span data-stu-id="d48af-151">-Units</span></span>
<span data-ttu-id="d48af-152">Número de unidades</span><span class="sxs-lookup"><span data-stu-id="d48af-152">Number of Units</span></span>

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

### <span data-ttu-id="d48af-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d48af-153">-Confirm</span></span>
<span data-ttu-id="d48af-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d48af-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d48af-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d48af-155">-WhatIf</span></span>
<span data-ttu-id="d48af-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d48af-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d48af-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d48af-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d48af-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d48af-158">-DefaultProfile</span></span>
<span data-ttu-id="d48af-159">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d48af-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d48af-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d48af-160">CommonParameters</span></span>
<span data-ttu-id="d48af-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d48af-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d48af-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d48af-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d48af-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d48af-163">INPUTS</span></span>

### <span data-ttu-id="d48af-164">System. String</span><span class="sxs-lookup"><span data-stu-id="d48af-164">System.String</span></span>
<span data-ttu-id="d48af-165">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties Microsoft. Azure. Commands. Management. IotHub. Models. PSOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="d48af-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="d48af-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d48af-166">OUTPUTS</span></span>

### <span data-ttu-id="d48af-167">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d48af-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="d48af-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d48af-168">NOTES</span></span>

## <span data-ttu-id="d48af-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d48af-169">RELATED LINKS</span></span>

