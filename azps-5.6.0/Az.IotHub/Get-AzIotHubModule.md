---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: c2515ff590543c448985f0c6635278430d8ae63e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889944"
---
# <span data-ttu-id="2ad9a-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="2ad9a-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="2ad9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ad9a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad9a-103">Obter os detalhes de um módulo de dispositivo IoT ou módulos de lista localizados em um dispositivo IoT em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="2ad9a-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="2ad9a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2ad9a-104">SYNTAX</span></span>

### <span data-ttu-id="2ad9a-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2ad9a-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ad9a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ad9a-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ad9a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2ad9a-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ad9a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2ad9a-108">DESCRIPTION</span></span>
<span data-ttu-id="2ad9a-109">Obter os detalhes de um módulo de dispositivo IoT ou módulos de lista localizados em um dispositivo IoT em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="2ad9a-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="2ad9a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ad9a-110">EXAMPLES</span></span>

### <span data-ttu-id="2ad9a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ad9a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  :
```

<span data-ttu-id="2ad9a-112">Obter os detalhes de um módulo de dispositivo IoT em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="2ad9a-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="2ad9a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2ad9a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="2ad9a-114">Mostrar todos os módulos localizados em um dispositivo IoT em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="2ad9a-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="2ad9a-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2ad9a-115">PARAMETERS</span></span>

### <span data-ttu-id="2ad9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad9a-116">-DefaultProfile</span></span>
<span data-ttu-id="2ad9a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ad9a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ad9a-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2ad9a-118">-DeviceId</span></span>
<span data-ttu-id="2ad9a-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="2ad9a-119">Target Device Id.</span></span>

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

### <span data-ttu-id="2ad9a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ad9a-120">-InputObject</span></span>
<span data-ttu-id="2ad9a-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="2ad9a-121">IotHub object</span></span>

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

### <span data-ttu-id="2ad9a-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2ad9a-122">-IotHubName</span></span>
<span data-ttu-id="2ad9a-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="2ad9a-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2ad9a-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="2ad9a-124">-ModuleId</span></span>
<span data-ttu-id="2ad9a-125">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="2ad9a-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ad9a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad9a-126">-ResourceGroupName</span></span>
<span data-ttu-id="2ad9a-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2ad9a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2ad9a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ad9a-128">-ResourceId</span></span>
<span data-ttu-id="2ad9a-129">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="2ad9a-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2ad9a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad9a-130">CommonParameters</span></span>
<span data-ttu-id="2ad9a-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ad9a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad9a-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ad9a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad9a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ad9a-133">INPUTS</span></span>

### <span data-ttu-id="2ad9a-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2ad9a-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2ad9a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2ad9a-135">System.String</span></span>

## <span data-ttu-id="2ad9a-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2ad9a-136">OUTPUTS</span></span>

### <span data-ttu-id="2ad9a-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="2ad9a-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="2ad9a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="2ad9a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="2ad9a-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="2ad9a-139">NOTES</span></span>

## <span data-ttu-id="2ad9a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ad9a-140">RELATED LINKS</span></span>
