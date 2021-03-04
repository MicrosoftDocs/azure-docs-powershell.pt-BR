---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: b1bdc6b5910f47fdca8e8b66ab99939945547a08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892169"
---
# <span data-ttu-id="fc8a9-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="fc8a9-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="fc8a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8a9-103">Atualize as opções de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="fc8a9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fc8a9-104">SYNTAX</span></span>

### <span data-ttu-id="fc8a9-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fc8a9-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc8a9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc8a9-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc8a9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fc8a9-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc8a9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fc8a9-108">DESCRIPTION</span></span>
<span data-ttu-id="fc8a9-109">Atualize as opções de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="fc8a9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc8a9-110">EXAMPLES</span></span>

### <span data-ttu-id="fc8a9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc8a9-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="fc8a9-112">Atualize as opções de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="fc8a9-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fc8a9-113">PARAMETERS</span></span>

### <span data-ttu-id="fc8a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc8a9-114">-DefaultProfile</span></span>
<span data-ttu-id="fc8a9-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc8a9-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fc8a9-116">-DeviceId</span></span>
<span data-ttu-id="fc8a9-117">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-117">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8a9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc8a9-118">-InputObject</span></span>
<span data-ttu-id="fc8a9-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="fc8a9-119">IotHub object</span></span>

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

### <span data-ttu-id="fc8a9-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fc8a9-120">-IotHubName</span></span>
<span data-ttu-id="fc8a9-121">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="fc8a9-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fc8a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc8a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc8a9-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="fc8a9-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fc8a9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc8a9-124">-ResourceId</span></span>
<span data-ttu-id="fc8a9-125">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="fc8a9-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fc8a9-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="fc8a9-126">-SamplingMode</span></span>
<span data-ttu-id="fc8a9-127">Ativa e desabilita a amostragem para rastreamento distribuído.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8a9-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="fc8a9-128">-SamplingRate</span></span>
<span data-ttu-id="fc8a9-129">Controla a quantidade de mensagens amostradas para adicionar contexto de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="fc8a9-130">Esse valor é uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-130">This value is a percentage.</span></span>
<span data-ttu-id="fc8a9-131">Somente valores de 0 a 100 (inclusive) são permitidos.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8a9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc8a9-132">-Confirm</span></span>
<span data-ttu-id="fc8a9-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc8a9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc8a9-134">-WhatIf</span></span>
<span data-ttu-id="fc8a9-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc8a9-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc8a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8a9-137">CommonParameters</span></span>
<span data-ttu-id="fc8a9-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc8a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8a9-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc8a9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8a9-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc8a9-140">INPUTS</span></span>

### <span data-ttu-id="fc8a9-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fc8a9-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fc8a9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fc8a9-142">System.String</span></span>

## <span data-ttu-id="fc8a9-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fc8a9-143">OUTPUTS</span></span>

### <span data-ttu-id="fc8a9-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="fc8a9-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="fc8a9-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="fc8a9-145">NOTES</span></span>

## <span data-ttu-id="fc8a9-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc8a9-146">RELATED LINKS</span></span>
