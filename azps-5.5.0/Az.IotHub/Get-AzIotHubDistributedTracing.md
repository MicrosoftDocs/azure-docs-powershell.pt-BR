---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113146"
---
# <span data-ttu-id="d4018-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="d4018-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="d4018-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4018-102">SYNOPSIS</span></span>
<span data-ttu-id="d4018-103">Obter as configurações de rastreamento distribuídas para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4018-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="d4018-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4018-104">SYNTAX</span></span>

### <span data-ttu-id="d4018-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d4018-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4018-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4018-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4018-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d4018-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4018-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4018-108">DESCRIPTION</span></span>
<span data-ttu-id="d4018-109">Obter as configurações de rastreamento distribuídas para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4018-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="d4018-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d4018-110">EXAMPLES</span></span>

### <span data-ttu-id="d4018-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d4018-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="d4018-112">Obter as configurações de rastreamento distribuídas para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4018-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="d4018-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4018-113">PARAMETERS</span></span>

### <span data-ttu-id="d4018-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4018-114">-DefaultProfile</span></span>
<span data-ttu-id="d4018-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4018-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4018-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d4018-116">-DeviceId</span></span>
<span data-ttu-id="d4018-117">ID do Dispositivo de Destino.</span><span class="sxs-lookup"><span data-stu-id="d4018-117">Target Device Id.</span></span>

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

### <span data-ttu-id="d4018-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4018-118">-InputObject</span></span>
<span data-ttu-id="d4018-119">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="d4018-119">IotHub object</span></span>

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

### <span data-ttu-id="d4018-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d4018-120">-IotHubName</span></span>
<span data-ttu-id="d4018-121">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="d4018-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d4018-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4018-122">-ResourceGroupName</span></span>
<span data-ttu-id="d4018-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d4018-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d4018-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4018-124">-ResourceId</span></span>
<span data-ttu-id="d4018-125">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="d4018-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d4018-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4018-126">CommonParameters</span></span>
<span data-ttu-id="d4018-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4018-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4018-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4018-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4018-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="d4018-129">INPUTS</span></span>

### <span data-ttu-id="d4018-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d4018-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d4018-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d4018-131">System.String</span></span>

## <span data-ttu-id="d4018-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="d4018-132">OUTPUTS</span></span>

### <span data-ttu-id="d4018-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="d4018-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="d4018-134">Notas</span><span class="sxs-lookup"><span data-stu-id="d4018-134">NOTES</span></span>

## <span data-ttu-id="d4018-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4018-135">RELATED LINKS</span></span>
