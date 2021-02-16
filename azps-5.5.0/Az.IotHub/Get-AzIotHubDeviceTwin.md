---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113147"
---
# <span data-ttu-id="52f31-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="52f31-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="52f31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52f31-102">SYNOPSIS</span></span>
<span data-ttu-id="52f31-103">Obtém um dispositivo duplo.</span><span class="sxs-lookup"><span data-stu-id="52f31-103">Gets a device twin.</span></span>

## <span data-ttu-id="52f31-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52f31-104">SYNTAX</span></span>

### <span data-ttu-id="52f31-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="52f31-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52f31-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="52f31-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52f31-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="52f31-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52f31-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="52f31-108">DESCRIPTION</span></span>
<span data-ttu-id="52f31-109">Obtém um dispositivo duplo.</span><span class="sxs-lookup"><span data-stu-id="52f31-109">Gets a device twin.</span></span> <span data-ttu-id="52f31-110">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins mais informações.</span><span class="sxs-lookup"><span data-stu-id="52f31-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="52f31-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52f31-111">EXAMPLES</span></span>

### <span data-ttu-id="52f31-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52f31-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="52f31-113">Retorna o objeto de brilho do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="52f31-113">Returns the device twin object.</span></span>

## <span data-ttu-id="52f31-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52f31-114">PARAMETERS</span></span>

### <span data-ttu-id="52f31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f31-115">-DefaultProfile</span></span>
<span data-ttu-id="52f31-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52f31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52f31-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="52f31-117">-DeviceId</span></span>
<span data-ttu-id="52f31-118">ID do Dispositivo de Destino.</span><span class="sxs-lookup"><span data-stu-id="52f31-118">Target Device Id.</span></span>

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

### <span data-ttu-id="52f31-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52f31-119">-InputObject</span></span>
<span data-ttu-id="52f31-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="52f31-120">IotHub object</span></span>

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

### <span data-ttu-id="52f31-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="52f31-121">-IotHubName</span></span>
<span data-ttu-id="52f31-122">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="52f31-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="52f31-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f31-123">-ResourceGroupName</span></span>
<span data-ttu-id="52f31-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="52f31-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="52f31-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52f31-125">-ResourceId</span></span>
<span data-ttu-id="52f31-126">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="52f31-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="52f31-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f31-127">CommonParameters</span></span>
<span data-ttu-id="52f31-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f31-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f31-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f31-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f31-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="52f31-130">INPUTS</span></span>

### <span data-ttu-id="52f31-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="52f31-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="52f31-132">System.String</span><span class="sxs-lookup"><span data-stu-id="52f31-132">System.String</span></span>

## <span data-ttu-id="52f31-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="52f31-133">OUTPUTS</span></span>

### <span data-ttu-id="52f31-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="52f31-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="52f31-135">Notas</span><span class="sxs-lookup"><span data-stu-id="52f31-135">NOTES</span></span>

## <span data-ttu-id="52f31-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52f31-136">RELATED LINKS</span></span>
