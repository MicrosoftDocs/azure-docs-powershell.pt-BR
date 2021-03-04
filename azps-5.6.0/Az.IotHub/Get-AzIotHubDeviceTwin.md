---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 45966042a2c2c6a660f052280039204a1d5eb908
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889955"
---
# <span data-ttu-id="f5764-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="f5764-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="f5764-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5764-102">SYNOPSIS</span></span>
<span data-ttu-id="f5764-103">Obtém um dispositivo duplo.</span><span class="sxs-lookup"><span data-stu-id="f5764-103">Gets a device twin.</span></span>

## <span data-ttu-id="f5764-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f5764-104">SYNTAX</span></span>

### <span data-ttu-id="f5764-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f5764-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5764-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f5764-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5764-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f5764-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5764-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f5764-108">DESCRIPTION</span></span>
<span data-ttu-id="f5764-109">Obtém um dispositivo duplo.</span><span class="sxs-lookup"><span data-stu-id="f5764-109">Gets a device twin.</span></span> <span data-ttu-id="f5764-110">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins mais informações.</span><span class="sxs-lookup"><span data-stu-id="f5764-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="f5764-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5764-111">EXAMPLES</span></span>

### <span data-ttu-id="f5764-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5764-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="f5764-113">Retorna o objeto duplo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5764-113">Returns the device twin object.</span></span>

## <span data-ttu-id="f5764-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f5764-114">PARAMETERS</span></span>

### <span data-ttu-id="f5764-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5764-115">-DefaultProfile</span></span>
<span data-ttu-id="f5764-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5764-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5764-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f5764-117">-DeviceId</span></span>
<span data-ttu-id="f5764-118">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="f5764-118">Target Device Id.</span></span>

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

### <span data-ttu-id="f5764-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5764-119">-InputObject</span></span>
<span data-ttu-id="f5764-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="f5764-120">IotHub object</span></span>

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

### <span data-ttu-id="f5764-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f5764-121">-IotHubName</span></span>
<span data-ttu-id="f5764-122">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="f5764-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f5764-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5764-123">-ResourceGroupName</span></span>
<span data-ttu-id="f5764-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="f5764-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f5764-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5764-125">-ResourceId</span></span>
<span data-ttu-id="f5764-126">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="f5764-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f5764-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5764-127">CommonParameters</span></span>
<span data-ttu-id="f5764-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5764-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5764-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5764-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5764-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5764-130">INPUTS</span></span>

### <span data-ttu-id="f5764-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f5764-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f5764-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f5764-132">System.String</span></span>

## <span data-ttu-id="f5764-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f5764-133">OUTPUTS</span></span>

### <span data-ttu-id="f5764-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="f5764-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="f5764-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="f5764-135">NOTES</span></span>

## <span data-ttu-id="f5764-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5764-136">RELATED LINKS</span></span>
