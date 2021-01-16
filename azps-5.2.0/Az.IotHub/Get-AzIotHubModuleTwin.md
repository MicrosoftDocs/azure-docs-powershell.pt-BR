---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261686"
---
# <span data-ttu-id="fe6b6-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="fe6b6-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="fe6b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe6b6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6b6-103">Obtém um módulo de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="fe6b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe6b6-104">SYNTAX</span></span>

### <span data-ttu-id="fe6b6-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fe6b6-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe6b6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fe6b6-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe6b6-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="fe6b6-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe6b6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe6b6-108">DESCRIPTION</span></span>
<span data-ttu-id="fe6b6-109">Obtém um módulo de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="fe6b6-110">Consulte https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="fe6b6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe6b6-111">EXAMPLES</span></span>

### <span data-ttu-id="fe6b6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe6b6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="fe6b6-113">Retorna o objeto de módulo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="fe6b6-114">OS</span><span class="sxs-lookup"><span data-stu-id="fe6b6-114">PARAMETERS</span></span>

### <span data-ttu-id="fe6b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe6b6-115">-DefaultProfile</span></span>
<span data-ttu-id="fe6b6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe6b6-117">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="fe6b6-117">-DeviceId</span></span>
<span data-ttu-id="fe6b6-118">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-118">Target Device Id.</span></span>

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

### <span data-ttu-id="fe6b6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe6b6-119">-InputObject</span></span>
<span data-ttu-id="fe6b6-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="fe6b6-120">IotHub object</span></span>

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

### <span data-ttu-id="fe6b6-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fe6b6-121">-IotHubName</span></span>
<span data-ttu-id="fe6b6-122">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="fe6b6-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fe6b6-123">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="fe6b6-123">-ModuleId</span></span>
<span data-ttu-id="fe6b6-124">ID do módulo de destino.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-124">Target Module Id.</span></span>

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

### <span data-ttu-id="fe6b6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe6b6-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe6b6-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fe6b6-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fe6b6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe6b6-127">-ResourceId</span></span>
<span data-ttu-id="fe6b6-128">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="fe6b6-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fe6b6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6b6-129">CommonParameters</span></span>
<span data-ttu-id="fe6b6-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe6b6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6b6-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe6b6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6b6-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe6b6-132">INPUTS</span></span>

### <span data-ttu-id="fe6b6-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fe6b6-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fe6b6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fe6b6-134">System.String</span></span>

## <span data-ttu-id="fe6b6-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe6b6-135">OUTPUTS</span></span>

### <span data-ttu-id="fe6b6-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="fe6b6-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="fe6b6-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe6b6-137">NOTES</span></span>

## <span data-ttu-id="fe6b6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe6b6-138">RELATED LINKS</span></span>
