---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258982"
---
# <span data-ttu-id="f39da-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="f39da-101">Set-AzIotHub</span></span>

## <span data-ttu-id="f39da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f39da-102">SYNOPSIS</span></span>
<span data-ttu-id="f39da-103">Atualiza as propriedades de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="f39da-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="f39da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f39da-104">SYNTAX</span></span>

### <span data-ttu-id="f39da-105">UpdateSku (padrão)</span><span class="sxs-lookup"><span data-stu-id="f39da-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39da-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="f39da-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39da-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="f39da-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39da-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="f39da-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39da-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="f39da-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39da-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="f39da-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39da-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="f39da-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f39da-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f39da-112">DESCRIPTION</span></span>
<span data-ttu-id="f39da-113">Atualiza as propriedades de um IotHub.</span><span class="sxs-lookup"><span data-stu-id="f39da-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="f39da-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f39da-114">EXAMPLES</span></span>

### <span data-ttu-id="f39da-115">Exemplo 1 atualize a SKU</span><span class="sxs-lookup"><span data-stu-id="f39da-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="f39da-116">Atualize a SKU para S1 e as unidades para 5 para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f39da-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="f39da-117">Exemplo 2 atualizar as propriedades do eventhub</span><span class="sxs-lookup"><span data-stu-id="f39da-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="f39da-118">Atualize o tempo de retenção de telemetria em dias como 4 para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f39da-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f39da-119">OS</span><span class="sxs-lookup"><span data-stu-id="f39da-119">PARAMETERS</span></span>

### <span data-ttu-id="f39da-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="f39da-120">-CloudToDevice</span></span>
<span data-ttu-id="f39da-121">As propriedades da fila do comando nuvem para dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f39da-121">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="f39da-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39da-122">-DefaultProfile</span></span>
<span data-ttu-id="f39da-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f39da-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f39da-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="f39da-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="f39da-125">Sinalizador que especifica se as notificações devem ser habilitadas para o carregamento do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f39da-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="f39da-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="f39da-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="f39da-127">Tempo de retenção em dias.</span><span class="sxs-lookup"><span data-stu-id="f39da-127">Retention time in days.</span></span> 

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

### <span data-ttu-id="f39da-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="f39da-128">-FallbackRoute</span></span>
<span data-ttu-id="f39da-129">Rota de fallback para roteamento</span><span class="sxs-lookup"><span data-stu-id="f39da-129">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="f39da-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="f39da-130">-FileUploadContainerName</span></span>
<span data-ttu-id="f39da-131">O nome do contêiner para o qual carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="f39da-131">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="f39da-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="f39da-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="f39da-133">A contagem máxima de entrega para notificações de carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f39da-133">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="f39da-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="f39da-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="f39da-135">Valor de vida útil para as mensagens na fila de notificação de carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f39da-135">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="f39da-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="f39da-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="f39da-137">Tempo de vida para o URI da SAS gerado para o carregamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f39da-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="f39da-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="f39da-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="f39da-139">A cadeia de conexão de armazenamento para a qual carregar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="f39da-139">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="f39da-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="f39da-140">-Name</span></span>
<span data-ttu-id="f39da-141">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="f39da-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="f39da-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39da-142">-ResourceGroupName</span></span>
<span data-ttu-id="f39da-143">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f39da-143">Resource Group Name</span></span>

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

### <span data-ttu-id="f39da-144">-Rotas</span><span class="sxs-lookup"><span data-stu-id="f39da-144">-Routes</span></span>
<span data-ttu-id="f39da-145">Rotas a serem adicionadas para roteamento</span><span class="sxs-lookup"><span data-stu-id="f39da-145">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="f39da-146">-Routingproperties</span><span class="sxs-lookup"><span data-stu-id="f39da-146">-RoutingProperties</span></span>
<span data-ttu-id="f39da-147">As propriedades de roteamento para direcionar mensagens para pontos de extremidade externos</span><span class="sxs-lookup"><span data-stu-id="f39da-147">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="f39da-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f39da-148">-SkuName</span></span>
<span data-ttu-id="f39da-149">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="f39da-149">Name of the Sku.</span></span>

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

### <span data-ttu-id="f39da-150">-Unidades</span><span class="sxs-lookup"><span data-stu-id="f39da-150">-Units</span></span>
<span data-ttu-id="f39da-151">Número de unidades</span><span class="sxs-lookup"><span data-stu-id="f39da-151">Number of Units</span></span>

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

### <span data-ttu-id="f39da-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f39da-152">-Confirm</span></span>
<span data-ttu-id="f39da-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f39da-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f39da-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f39da-154">-WhatIf</span></span>
<span data-ttu-id="f39da-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f39da-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f39da-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f39da-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f39da-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39da-157">CommonParameters</span></span>
<span data-ttu-id="f39da-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f39da-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39da-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39da-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39da-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f39da-160">INPUTS</span></span>

### <span data-ttu-id="f39da-161">System. String</span><span class="sxs-lookup"><span data-stu-id="f39da-161">System.String</span></span>

## <span data-ttu-id="f39da-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f39da-162">OUTPUTS</span></span>

### <span data-ttu-id="f39da-163">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f39da-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="f39da-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f39da-164">NOTES</span></span>

## <span data-ttu-id="f39da-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f39da-165">RELATED LINKS</span></span>
