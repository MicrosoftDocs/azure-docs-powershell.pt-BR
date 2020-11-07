---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942995"
---
# <span data-ttu-id="3f215-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="3f215-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="3f215-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f215-102">SYNOPSIS</span></span>
<span data-ttu-id="3f215-103">Obtém um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f215-103">Gets a device twin.</span></span>

## <span data-ttu-id="3f215-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f215-104">SYNTAX</span></span>

### <span data-ttu-id="3f215-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f215-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f215-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3f215-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f215-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="3f215-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f215-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f215-108">DESCRIPTION</span></span>
<span data-ttu-id="3f215-109">Obtém um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f215-109">Gets a device twin.</span></span> <span data-ttu-id="3f215-110">Consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3f215-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="3f215-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f215-111">EXAMPLES</span></span>

### <span data-ttu-id="3f215-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f215-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="3f215-113">Retorna o objeto adddevice.</span><span class="sxs-lookup"><span data-stu-id="3f215-113">Returns the device twin object.</span></span>

## <span data-ttu-id="3f215-114">OS</span><span class="sxs-lookup"><span data-stu-id="3f215-114">PARAMETERS</span></span>

### <span data-ttu-id="3f215-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f215-115">-DefaultProfile</span></span>
<span data-ttu-id="3f215-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f215-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f215-117">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="3f215-117">-DeviceId</span></span>
<span data-ttu-id="3f215-118">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="3f215-118">Target Device Id.</span></span>

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

### <span data-ttu-id="3f215-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f215-119">-InputObject</span></span>
<span data-ttu-id="3f215-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="3f215-120">IotHub object</span></span>

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

### <span data-ttu-id="3f215-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3f215-121">-IotHubName</span></span>
<span data-ttu-id="3f215-122">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="3f215-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3f215-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f215-123">-ResourceGroupName</span></span>
<span data-ttu-id="3f215-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3f215-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3f215-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f215-125">-ResourceId</span></span>
<span data-ttu-id="3f215-126">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="3f215-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3f215-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f215-127">CommonParameters</span></span>
<span data-ttu-id="3f215-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f215-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f215-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f215-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f215-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f215-130">INPUTS</span></span>

### <span data-ttu-id="3f215-131">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3f215-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3f215-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3f215-132">System.String</span></span>

## <span data-ttu-id="3f215-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f215-133">OUTPUTS</span></span>

### <span data-ttu-id="3f215-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="3f215-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="3f215-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f215-135">NOTES</span></span>

## <span data-ttu-id="3f215-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f215-136">RELATED LINKS</span></span>
