---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: 290b2ddcea6812b840b9c19ad2d44c4a0e461e64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889954"
---
# <span data-ttu-id="6ab18-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="6ab18-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="6ab18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ab18-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab18-103">Obter as configurações de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ab18-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="6ab18-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6ab18-104">SYNTAX</span></span>

### <span data-ttu-id="6ab18-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6ab18-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ab18-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6ab18-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ab18-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6ab18-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ab18-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6ab18-108">DESCRIPTION</span></span>
<span data-ttu-id="6ab18-109">Obter as configurações de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ab18-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="6ab18-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ab18-110">EXAMPLES</span></span>

### <span data-ttu-id="6ab18-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6ab18-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="6ab18-112">Obter as configurações de rastreamento distribuído para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ab18-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="6ab18-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6ab18-113">PARAMETERS</span></span>

### <span data-ttu-id="6ab18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab18-114">-DefaultProfile</span></span>
<span data-ttu-id="6ab18-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab18-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab18-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6ab18-116">-DeviceId</span></span>
<span data-ttu-id="6ab18-117">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="6ab18-117">Target Device Id.</span></span>

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

### <span data-ttu-id="6ab18-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ab18-118">-InputObject</span></span>
<span data-ttu-id="6ab18-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="6ab18-119">IotHub object</span></span>

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

### <span data-ttu-id="6ab18-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6ab18-120">-IotHubName</span></span>
<span data-ttu-id="6ab18-121">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="6ab18-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6ab18-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab18-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ab18-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6ab18-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6ab18-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ab18-124">-ResourceId</span></span>
<span data-ttu-id="6ab18-125">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="6ab18-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6ab18-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab18-126">CommonParameters</span></span>
<span data-ttu-id="6ab18-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab18-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab18-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ab18-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab18-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ab18-129">INPUTS</span></span>

### <span data-ttu-id="6ab18-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6ab18-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6ab18-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6ab18-131">System.String</span></span>

## <span data-ttu-id="6ab18-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6ab18-132">OUTPUTS</span></span>

### <span data-ttu-id="6ab18-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="6ab18-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="6ab18-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="6ab18-134">NOTES</span></span>

## <span data-ttu-id="6ab18-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ab18-135">RELATED LINKS</span></span>
