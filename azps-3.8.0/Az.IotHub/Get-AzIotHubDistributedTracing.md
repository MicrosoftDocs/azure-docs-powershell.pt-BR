---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942993"
---
# <span data-ttu-id="fb506-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="fb506-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="fb506-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb506-102">SYNOPSIS</span></span>
<span data-ttu-id="fb506-103">Obter as configurações de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb506-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="fb506-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb506-104">SYNTAX</span></span>

### <span data-ttu-id="fb506-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb506-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb506-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fb506-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb506-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="fb506-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb506-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb506-108">DESCRIPTION</span></span>
<span data-ttu-id="fb506-109">Obter as configurações de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb506-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="fb506-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb506-110">EXAMPLES</span></span>

### <span data-ttu-id="fb506-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb506-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="fb506-112">Obter as configurações de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb506-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="fb506-113">OS</span><span class="sxs-lookup"><span data-stu-id="fb506-113">PARAMETERS</span></span>

### <span data-ttu-id="fb506-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb506-114">-DefaultProfile</span></span>
<span data-ttu-id="fb506-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb506-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb506-116">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="fb506-116">-DeviceId</span></span>
<span data-ttu-id="fb506-117">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="fb506-117">Target Device Id.</span></span>

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

### <span data-ttu-id="fb506-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb506-118">-InputObject</span></span>
<span data-ttu-id="fb506-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="fb506-119">IotHub object</span></span>

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

### <span data-ttu-id="fb506-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fb506-120">-IotHubName</span></span>
<span data-ttu-id="fb506-121">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="fb506-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fb506-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb506-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb506-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fb506-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fb506-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb506-124">-ResourceId</span></span>
<span data-ttu-id="fb506-125">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="fb506-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fb506-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb506-126">CommonParameters</span></span>
<span data-ttu-id="fb506-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb506-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb506-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb506-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb506-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb506-129">INPUTS</span></span>

### <span data-ttu-id="fb506-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fb506-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fb506-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fb506-131">System.String</span></span>

## <span data-ttu-id="fb506-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb506-132">OUTPUTS</span></span>

### <span data-ttu-id="fb506-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="fb506-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="fb506-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb506-134">NOTES</span></span>

## <span data-ttu-id="fb506-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb506-135">RELATED LINKS</span></span>
