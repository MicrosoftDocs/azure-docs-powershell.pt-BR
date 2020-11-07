---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: ca7fe171e95d87dd054f0dac27e1a5ccd07396a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770693"
---
# <span data-ttu-id="fbe5f-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="fbe5f-101">Set-AzIotHub</span></span>

## <span data-ttu-id="fbe5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbe5f-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe5f-103">Atualiza as propriedades de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="fbe5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbe5f-104">SYNTAX</span></span>

### <span data-ttu-id="fbe5f-105">UpdateSku (padrão)</span><span class="sxs-lookup"><span data-stu-id="fbe5f-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe5f-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="fbe5f-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe5f-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="fbe5f-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe5f-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="fbe5f-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe5f-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="fbe5f-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe5f-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="fbe5f-110">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe5f-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="fbe5f-111">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe5f-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="fbe5f-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe5f-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fbe5f-113">DESCRIPTION</span></span>
<span data-ttu-id="fbe5f-114">Atualiza as propriedades de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="fbe5f-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbe5f-115">EXAMPLES</span></span>

### <span data-ttu-id="fbe5f-116">Exemplo 1 atualize a SKU</span><span class="sxs-lookup"><span data-stu-id="fbe5f-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="fbe5f-117">Atualize a SKU para S1 e as unidades para 5 para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="fbe5f-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="fbe5f-118">Exemplo 2 atualizar as propriedades do eventhub</span><span class="sxs-lookup"><span data-stu-id="fbe5f-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="fbe5f-119">Atualize o tempo de retenção em dias a 4 para os eventos telemetria e operationsmonitoringevents para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="fbe5f-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="fbe5f-120">OS</span><span class="sxs-lookup"><span data-stu-id="fbe5f-120">PARAMETERS</span></span>

### <span data-ttu-id="fbe5f-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="fbe5f-121">-CloudToDevice</span></span>
<span data-ttu-id="fbe5f-122">As propriedades da fila do comando nuvem para dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-122">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="fbe5f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe5f-123">-DefaultProfile</span></span>
<span data-ttu-id="fbe5f-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fbe5f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbe5f-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="fbe5f-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="fbe5f-126">Sinalizador que especifica se as notificações devem ser habilitadas para o carregamento do arquivo.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="fbe5f-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="fbe5f-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="fbe5f-128">Tempo de retenção em dias.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-128">Retention time in days.</span></span> 

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

### <span data-ttu-id="fbe5f-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="fbe5f-129">-FallbackRoute</span></span>
<span data-ttu-id="fbe5f-130">Rota de fallback para roteamento</span><span class="sxs-lookup"><span data-stu-id="fbe5f-130">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="fbe5f-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="fbe5f-131">-FileUploadContainerName</span></span>
<span data-ttu-id="fbe5f-132">O nome do contêiner para o qual carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-132">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="fbe5f-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="fbe5f-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="fbe5f-134">A contagem máxima de entrega para notificações de carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-134">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="fbe5f-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="fbe5f-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="fbe5f-136">Valor de vida útil para as mensagens na fila de notificação de carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-136">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="fbe5f-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="fbe5f-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="fbe5f-138">Tempo de vida para o URI da SAS gerado para o carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="fbe5f-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="fbe5f-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="fbe5f-140">A cadeia de conexão de armazenamento para a qual carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-140">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="fbe5f-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbe5f-141">-Name</span></span>
<span data-ttu-id="fbe5f-142">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="fbe5f-142">Name of the IotHub</span></span>

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

### <span data-ttu-id="fbe5f-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="fbe5f-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="fbe5f-144">As propriedades relacionadas ao monitoramento de operações.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-144">The properties related to operations monitoring.</span></span> 

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

### <span data-ttu-id="fbe5f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe5f-145">-ResourceGroupName</span></span>
<span data-ttu-id="fbe5f-146">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fbe5f-146">Resource Group Name</span></span>

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

### <span data-ttu-id="fbe5f-147">-Rotas</span><span class="sxs-lookup"><span data-stu-id="fbe5f-147">-Routes</span></span>
<span data-ttu-id="fbe5f-148">Rotas a serem adicionadas para roteamento</span><span class="sxs-lookup"><span data-stu-id="fbe5f-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="fbe5f-149">-Routingproperties</span><span class="sxs-lookup"><span data-stu-id="fbe5f-149">-RoutingProperties</span></span>
<span data-ttu-id="fbe5f-150">As propriedades de roteamento para direcionar mensagens para pontos de extremidade externos</span><span class="sxs-lookup"><span data-stu-id="fbe5f-150">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="fbe5f-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fbe5f-151">-SkuName</span></span>
<span data-ttu-id="fbe5f-152">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-152">Name of the Sku.</span></span>

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

### <span data-ttu-id="fbe5f-153">-Unidades</span><span class="sxs-lookup"><span data-stu-id="fbe5f-153">-Units</span></span>
<span data-ttu-id="fbe5f-154">Número de unidades</span><span class="sxs-lookup"><span data-stu-id="fbe5f-154">Number of Units</span></span>

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

### <span data-ttu-id="fbe5f-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fbe5f-155">-Confirm</span></span>
<span data-ttu-id="fbe5f-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe5f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe5f-157">-WhatIf</span></span>
<span data-ttu-id="fbe5f-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe5f-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe5f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe5f-160">CommonParameters</span></span>
<span data-ttu-id="fbe5f-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe5f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe5f-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe5f-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe5f-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fbe5f-163">INPUTS</span></span>

### <span data-ttu-id="fbe5f-164">System. String</span><span class="sxs-lookup"><span data-stu-id="fbe5f-164">System.String</span></span>

## <span data-ttu-id="fbe5f-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fbe5f-165">OUTPUTS</span></span>

### <span data-ttu-id="fbe5f-166">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fbe5f-166">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="fbe5f-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fbe5f-167">NOTES</span></span>

## <span data-ttu-id="fbe5f-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbe5f-168">RELATED LINKS</span></span>
