---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 41c4f5f4852f499f45b5c765263bdf356dbf90ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890619"
---
# <span data-ttu-id="58052-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="58052-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="58052-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58052-102">SYNOPSIS</span></span>
<span data-ttu-id="58052-103">Enviar mensagem de dispositivo para nuvem.</span><span class="sxs-lookup"><span data-stu-id="58052-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="58052-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="58052-104">SYNTAX</span></span>

### <span data-ttu-id="58052-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="58052-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58052-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="58052-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58052-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="58052-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58052-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="58052-108">DESCRIPTION</span></span>
<span data-ttu-id="58052-109">O comando dá suporte ao envio de mensagens com propriedades do aplicativo e do sistema.</span><span class="sxs-lookup"><span data-stu-id="58052-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="58052-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58052-110">EXAMPLES</span></span>

### <span data-ttu-id="58052-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58052-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="58052-112">Enviar mensagem de dispositivo para a nuvem usando o tipo de transporte padrão.</span><span class="sxs-lookup"><span data-stu-id="58052-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="58052-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="58052-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="58052-114">Enviando um dispositivo mqtt para a mensagem na nuvem.</span><span class="sxs-lookup"><span data-stu-id="58052-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="58052-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="58052-115">PARAMETERS</span></span>

### <span data-ttu-id="58052-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58052-116">-DefaultProfile</span></span>
<span data-ttu-id="58052-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58052-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58052-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="58052-118">-DeviceId</span></span>
<span data-ttu-id="58052-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="58052-119">Target Device Id.</span></span>

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

### <span data-ttu-id="58052-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58052-120">-InputObject</span></span>
<span data-ttu-id="58052-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="58052-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58052-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="58052-122">-IotHubName</span></span>
<span data-ttu-id="58052-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="58052-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58052-124">-Message</span><span class="sxs-lookup"><span data-stu-id="58052-124">-Message</span></span>
<span data-ttu-id="58052-125">Corpo da mensagem a ser enviado para o Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="58052-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="58052-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58052-126">-PassThru</span></span>
<span data-ttu-id="58052-127">Permite retornar o objeto booleano.</span><span class="sxs-lookup"><span data-stu-id="58052-127">Allows to return the boolean object.</span></span> <span data-ttu-id="58052-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="58052-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58052-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58052-129">-ResourceGroupName</span></span>
<span data-ttu-id="58052-130">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="58052-130">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58052-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58052-131">-ResourceId</span></span>
<span data-ttu-id="58052-132">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="58052-132">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58052-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="58052-133">-TransportType</span></span>
<span data-ttu-id="58052-134">Tipo de transporte a ser usado.</span><span class="sxs-lookup"><span data-stu-id="58052-134">Transport type to use.</span></span>
<span data-ttu-id="58052-135">O padrão é Amqp.</span><span class="sxs-lookup"><span data-stu-id="58052-135">Default is Amqp.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSTransportType
Parameter Sets: (All)
Aliases:
Accepted values: Amqp, Http1, Amqp_WebSocket_Only, Amqp_Tcp_Only, Mqtt, Mqtt_WebSocket_Only, Mqtt_Tcp_Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58052-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58052-136">-Confirm</span></span>
<span data-ttu-id="58052-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58052-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58052-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58052-138">-WhatIf</span></span>
<span data-ttu-id="58052-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58052-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58052-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58052-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58052-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58052-141">CommonParameters</span></span>
<span data-ttu-id="58052-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58052-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58052-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58052-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58052-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58052-144">INPUTS</span></span>

### <span data-ttu-id="58052-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="58052-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="58052-146">System.String</span><span class="sxs-lookup"><span data-stu-id="58052-146">System.String</span></span>

## <span data-ttu-id="58052-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="58052-147">OUTPUTS</span></span>

### <span data-ttu-id="58052-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58052-148">System.Boolean</span></span>

## <span data-ttu-id="58052-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="58052-149">NOTES</span></span>

## <span data-ttu-id="58052-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58052-150">RELATED LINKS</span></span>
