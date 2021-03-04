---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: f90aabda20192c046692f357432728dc46581cd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889965"
---
# <span data-ttu-id="7c5bf-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7c5bf-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="7c5bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="7c5bf-103">Lista todos os dispositivos ou um dispositivo específico contido em um Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c5bf-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="7c5bf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7c5bf-104">SYNTAX</span></span>

### <span data-ttu-id="7c5bf-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7c5bf-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c5bf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c5bf-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c5bf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7c5bf-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c5bf-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7c5bf-108">DESCRIPTION</span></span>
<span data-ttu-id="7c5bf-109">Obter os detalhes de um dispositivo de Hub de Iot ou listar todos os dispositivos em um Hub de Iot.</span><span class="sxs-lookup"><span data-stu-id="7c5bf-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="7c5bf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c5bf-110">EXAMPLES</span></span>

### <span data-ttu-id="7c5bf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7c5bf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="7c5bf-112">Mostrar todos os dispositivos em um Hub de Iot.</span><span class="sxs-lookup"><span data-stu-id="7c5bf-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="7c5bf-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7c5bf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Disabled
StatusReason               : Reason1
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                :
```

<span data-ttu-id="7c5bf-114">Obter os detalhes de um dispositivo IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="7c5bf-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="7c5bf-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7c5bf-115">PARAMETERS</span></span>

### <span data-ttu-id="7c5bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c5bf-116">-DefaultProfile</span></span>
<span data-ttu-id="7c5bf-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c5bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c5bf-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7c5bf-118">-DeviceId</span></span>
<span data-ttu-id="7c5bf-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="7c5bf-119">Target Device Id.</span></span>

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

### <span data-ttu-id="7c5bf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c5bf-120">-InputObject</span></span>
<span data-ttu-id="7c5bf-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="7c5bf-121">IotHub object</span></span>

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

### <span data-ttu-id="7c5bf-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7c5bf-122">-IotHubName</span></span>
<span data-ttu-id="7c5bf-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="7c5bf-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7c5bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c5bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c5bf-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7c5bf-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7c5bf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c5bf-126">-ResourceId</span></span>
<span data-ttu-id="7c5bf-127">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="7c5bf-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7c5bf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c5bf-128">CommonParameters</span></span>
<span data-ttu-id="7c5bf-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c5bf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c5bf-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c5bf-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c5bf-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c5bf-131">INPUTS</span></span>

### <span data-ttu-id="7c5bf-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7c5bf-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7c5bf-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7c5bf-133">System.String</span></span>

## <span data-ttu-id="7c5bf-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7c5bf-134">OUTPUTS</span></span>

### <span data-ttu-id="7c5bf-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="7c5bf-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="7c5bf-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span><span class="sxs-lookup"><span data-stu-id="7c5bf-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="7c5bf-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="7c5bf-137">NOTES</span></span>

## <span data-ttu-id="7c5bf-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c5bf-138">RELATED LINKS</span></span>
