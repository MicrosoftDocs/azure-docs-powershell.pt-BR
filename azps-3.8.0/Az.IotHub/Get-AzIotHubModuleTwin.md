---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943835"
---
# <span data-ttu-id="8f377-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="8f377-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="8f377-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f377-102">SYNOPSIS</span></span>
<span data-ttu-id="8f377-103">Obtém um módulo de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="8f377-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="8f377-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f377-104">SYNTAX</span></span>

### <span data-ttu-id="8f377-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8f377-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f377-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8f377-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f377-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="8f377-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f377-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f377-108">DESCRIPTION</span></span>
<span data-ttu-id="8f377-109">Obtém um módulo de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="8f377-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="8f377-110">Consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8f377-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="8f377-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f377-111">EXAMPLES</span></span>

### <span data-ttu-id="8f377-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f377-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="8f377-113">Retorna o objeto de módulo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f377-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="8f377-114">OS</span><span class="sxs-lookup"><span data-stu-id="8f377-114">PARAMETERS</span></span>

### <span data-ttu-id="8f377-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f377-115">-DefaultProfile</span></span>
<span data-ttu-id="8f377-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f377-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f377-117">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="8f377-117">-DeviceId</span></span>
<span data-ttu-id="8f377-118">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="8f377-118">Target Device Id.</span></span>

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

### <span data-ttu-id="8f377-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f377-119">-InputObject</span></span>
<span data-ttu-id="8f377-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="8f377-120">IotHub object</span></span>

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

### <span data-ttu-id="8f377-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8f377-121">-IotHubName</span></span>
<span data-ttu-id="8f377-122">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="8f377-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8f377-123">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="8f377-123">-ModuleId</span></span>
<span data-ttu-id="8f377-124">ID do módulo de destino.</span><span class="sxs-lookup"><span data-stu-id="8f377-124">Target Module Id.</span></span>

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

### <span data-ttu-id="8f377-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f377-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f377-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8f377-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8f377-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f377-127">-ResourceId</span></span>
<span data-ttu-id="8f377-128">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="8f377-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8f377-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f377-129">CommonParameters</span></span>
<span data-ttu-id="8f377-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f377-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f377-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f377-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f377-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f377-132">INPUTS</span></span>

### <span data-ttu-id="8f377-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8f377-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8f377-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8f377-134">System.String</span></span>

## <span data-ttu-id="8f377-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f377-135">OUTPUTS</span></span>

### <span data-ttu-id="8f377-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="8f377-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="8f377-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f377-137">NOTES</span></span>

## <span data-ttu-id="8f377-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f377-138">RELATED LINKS</span></span>
