---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 915fdf5bd0e53e7e8ed2817d83438597d515007d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889941"
---
# <span data-ttu-id="cb0e4-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="cb0e4-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="cb0e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0e4-103">Obtém um módulo de dispositivo IoT duplo.</span><span class="sxs-lookup"><span data-stu-id="cb0e4-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="cb0e4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cb0e4-104">SYNTAX</span></span>

### <span data-ttu-id="cb0e4-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cb0e4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb0e4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb0e4-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb0e4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cb0e4-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb0e4-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cb0e4-108">DESCRIPTION</span></span>
<span data-ttu-id="cb0e4-109">Obtém um módulo de dispositivo IoT duplo.</span><span class="sxs-lookup"><span data-stu-id="cb0e4-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="cb0e4-110">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins mais informações.</span><span class="sxs-lookup"><span data-stu-id="cb0e4-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="cb0e4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb0e4-111">EXAMPLES</span></span>

### <span data-ttu-id="cb0e4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cb0e4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="cb0e4-113">Retorna o objeto duplo do módulo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cb0e4-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="cb0e4-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cb0e4-114">PARAMETERS</span></span>

### <span data-ttu-id="cb0e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0e4-115">-DefaultProfile</span></span>
<span data-ttu-id="cb0e4-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb0e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb0e4-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="cb0e4-117">-DeviceId</span></span>
<span data-ttu-id="cb0e4-118">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="cb0e4-118">Target Device Id.</span></span>

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

### <span data-ttu-id="cb0e4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb0e4-119">-InputObject</span></span>
<span data-ttu-id="cb0e4-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="cb0e4-120">IotHub object</span></span>

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

### <span data-ttu-id="cb0e4-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="cb0e4-121">-IotHubName</span></span>
<span data-ttu-id="cb0e4-122">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="cb0e4-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cb0e4-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="cb0e4-123">-ModuleId</span></span>
<span data-ttu-id="cb0e4-124">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="cb0e4-124">Target Module Id.</span></span>

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

### <span data-ttu-id="cb0e4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb0e4-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb0e4-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="cb0e4-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cb0e4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb0e4-127">-ResourceId</span></span>
<span data-ttu-id="cb0e4-128">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="cb0e4-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cb0e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0e4-129">CommonParameters</span></span>
<span data-ttu-id="cb0e4-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb0e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0e4-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb0e4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0e4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb0e4-132">INPUTS</span></span>

### <span data-ttu-id="cb0e4-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cb0e4-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cb0e4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="cb0e4-134">System.String</span></span>

## <span data-ttu-id="cb0e4-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cb0e4-135">OUTPUTS</span></span>

### <span data-ttu-id="cb0e4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="cb0e4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="cb0e4-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="cb0e4-137">NOTES</span></span>

## <span data-ttu-id="cb0e4-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb0e4-138">RELATED LINKS</span></span>
