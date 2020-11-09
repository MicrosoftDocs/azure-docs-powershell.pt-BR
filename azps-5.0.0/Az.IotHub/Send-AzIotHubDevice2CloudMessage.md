---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280530"
---
# <span data-ttu-id="7b561-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="7b561-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="7b561-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b561-102">SYNOPSIS</span></span>
<span data-ttu-id="7b561-103">Envie uma mensagem de dispositivo para a nuvem.</span><span class="sxs-lookup"><span data-stu-id="7b561-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="7b561-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b561-104">SYNTAX</span></span>

### <span data-ttu-id="7b561-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7b561-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b561-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7b561-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b561-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="7b561-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b561-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b561-108">DESCRIPTION</span></span>
<span data-ttu-id="7b561-109">O comando aceita o envio de mensagens com o aplicativo e as propriedades do sistema.</span><span class="sxs-lookup"><span data-stu-id="7b561-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="7b561-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b561-110">EXAMPLES</span></span>

### <span data-ttu-id="7b561-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b561-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="7b561-112">Enviando o dispositivo para a mensagem na nuvem usando o tipo de transporte padrão.</span><span class="sxs-lookup"><span data-stu-id="7b561-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="7b561-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7b561-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="7b561-114">Enviar um dispositivo MQTT para a mensagem na nuvem.</span><span class="sxs-lookup"><span data-stu-id="7b561-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="7b561-115">OS</span><span class="sxs-lookup"><span data-stu-id="7b561-115">PARAMETERS</span></span>

### <span data-ttu-id="7b561-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b561-116">-DefaultProfile</span></span>
<span data-ttu-id="7b561-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b561-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b561-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="7b561-118">-DeviceId</span></span>
<span data-ttu-id="7b561-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="7b561-119">Target Device Id.</span></span>

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

### <span data-ttu-id="7b561-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b561-120">-InputObject</span></span>
<span data-ttu-id="7b561-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="7b561-121">IotHub object</span></span>

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

### <span data-ttu-id="7b561-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7b561-122">-IotHubName</span></span>
<span data-ttu-id="7b561-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="7b561-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7b561-124">-Mensagem</span><span class="sxs-lookup"><span data-stu-id="7b561-124">-Message</span></span>
<span data-ttu-id="7b561-125">Corpo da mensagem para enviar ao Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="7b561-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="7b561-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b561-126">-PassThru</span></span>
<span data-ttu-id="7b561-127">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="7b561-127">Allows to return the boolean object.</span></span> <span data-ttu-id="7b561-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7b561-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7b561-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b561-129">-ResourceGroupName</span></span>
<span data-ttu-id="7b561-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7b561-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7b561-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b561-131">-ResourceId</span></span>
<span data-ttu-id="7b561-132">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="7b561-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7b561-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="7b561-133">-TransportType</span></span>
<span data-ttu-id="7b561-134">Tipo de transporte a ser usado.</span><span class="sxs-lookup"><span data-stu-id="7b561-134">Transport type to use.</span></span>
<span data-ttu-id="7b561-135">O padrão é AMQP.</span><span class="sxs-lookup"><span data-stu-id="7b561-135">Default is Amqp.</span></span>

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

### <span data-ttu-id="7b561-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7b561-136">-Confirm</span></span>
<span data-ttu-id="7b561-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b561-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b561-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b561-138">-WhatIf</span></span>
<span data-ttu-id="7b561-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b561-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b561-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b561-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b561-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b561-141">CommonParameters</span></span>
<span data-ttu-id="7b561-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b561-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b561-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b561-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b561-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b561-144">INPUTS</span></span>

### <span data-ttu-id="7b561-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7b561-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7b561-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7b561-146">System.String</span></span>

## <span data-ttu-id="7b561-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b561-147">OUTPUTS</span></span>

### <span data-ttu-id="7b561-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b561-148">System.Boolean</span></span>

## <span data-ttu-id="7b561-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b561-149">NOTES</span></span>

## <span data-ttu-id="7b561-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b561-150">RELATED LINKS</span></span>
