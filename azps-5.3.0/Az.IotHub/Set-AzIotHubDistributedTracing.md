---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272797"
---
# <span data-ttu-id="6ef14-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="6ef14-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="6ef14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ef14-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef14-103">Atualizar as opções de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ef14-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="6ef14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ef14-104">SYNTAX</span></span>

### <span data-ttu-id="6ef14-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6ef14-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ef14-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6ef14-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ef14-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="6ef14-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ef14-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ef14-108">DESCRIPTION</span></span>
<span data-ttu-id="6ef14-109">Atualizar as opções de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ef14-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="6ef14-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ef14-110">EXAMPLES</span></span>

### <span data-ttu-id="6ef14-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6ef14-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="6ef14-112">Atualizar as opções de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ef14-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="6ef14-113">OS</span><span class="sxs-lookup"><span data-stu-id="6ef14-113">PARAMETERS</span></span>

### <span data-ttu-id="6ef14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef14-114">-DefaultProfile</span></span>
<span data-ttu-id="6ef14-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ef14-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ef14-116">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="6ef14-116">-DeviceId</span></span>
<span data-ttu-id="6ef14-117">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="6ef14-117">Target Device Id.</span></span>

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

### <span data-ttu-id="6ef14-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ef14-118">-InputObject</span></span>
<span data-ttu-id="6ef14-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="6ef14-119">IotHub object</span></span>

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

### <span data-ttu-id="6ef14-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6ef14-120">-IotHubName</span></span>
<span data-ttu-id="6ef14-121">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="6ef14-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6ef14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ef14-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ef14-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6ef14-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6ef14-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ef14-124">-ResourceId</span></span>
<span data-ttu-id="6ef14-125">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="6ef14-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6ef14-126">-Amostragemmode</span><span class="sxs-lookup"><span data-stu-id="6ef14-126">-SamplingMode</span></span>
<span data-ttu-id="6ef14-127">Torna a amostragem para habilitar e desabilitar o rastreamento distribuído.</span><span class="sxs-lookup"><span data-stu-id="6ef14-127">Turns sampling for distributed tracing enable and disable.</span></span>

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

### <span data-ttu-id="6ef14-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="6ef14-128">-SamplingRate</span></span>
<span data-ttu-id="6ef14-129">Controla a quantidade de mensagens amostradas para adicionar contexto de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="6ef14-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="6ef14-130">Esse valor é uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="6ef14-130">This value is a percentage.</span></span>
<span data-ttu-id="6ef14-131">Somente os valores de 0 a 100 (inclusivos) são permitidos.</span><span class="sxs-lookup"><span data-stu-id="6ef14-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

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

### <span data-ttu-id="6ef14-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6ef14-132">-Confirm</span></span>
<span data-ttu-id="6ef14-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ef14-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ef14-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ef14-134">-WhatIf</span></span>
<span data-ttu-id="6ef14-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ef14-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ef14-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ef14-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ef14-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef14-137">CommonParameters</span></span>
<span data-ttu-id="6ef14-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ef14-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef14-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ef14-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef14-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ef14-140">INPUTS</span></span>

### <span data-ttu-id="6ef14-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6ef14-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6ef14-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6ef14-142">System.String</span></span>

## <span data-ttu-id="6ef14-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ef14-143">OUTPUTS</span></span>

### <span data-ttu-id="6ef14-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="6ef14-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="6ef14-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ef14-145">NOTES</span></span>

## <span data-ttu-id="6ef14-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ef14-146">RELATED LINKS</span></span>
