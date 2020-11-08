---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113366"
---
# <span data-ttu-id="560cd-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="560cd-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="560cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="560cd-102">SYNOPSIS</span></span>
<span data-ttu-id="560cd-103">Lista todos os dispositivos ou um determinado dispositivo contido em um hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="560cd-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="560cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="560cd-104">SYNTAX</span></span>

### <span data-ttu-id="560cd-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="560cd-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="560cd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="560cd-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="560cd-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="560cd-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="560cd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="560cd-108">DESCRIPTION</span></span>
<span data-ttu-id="560cd-109">Obtenha os detalhes de um dispositivo Hub IOT ou liste todos os dispositivos em um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="560cd-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="560cd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="560cd-110">EXAMPLES</span></span>

### <span data-ttu-id="560cd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="560cd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="560cd-112">Mostrar todos os dispositivos em um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="560cd-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="560cd-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="560cd-113">Example 2</span></span>
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

<span data-ttu-id="560cd-114">Obter os detalhes de um dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="560cd-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="560cd-115">OS</span><span class="sxs-lookup"><span data-stu-id="560cd-115">PARAMETERS</span></span>

### <span data-ttu-id="560cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="560cd-116">-DefaultProfile</span></span>
<span data-ttu-id="560cd-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="560cd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="560cd-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="560cd-118">-DeviceId</span></span>
<span data-ttu-id="560cd-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="560cd-119">Target Device Id.</span></span>

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

### <span data-ttu-id="560cd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="560cd-120">-InputObject</span></span>
<span data-ttu-id="560cd-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="560cd-121">IotHub object</span></span>

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

### <span data-ttu-id="560cd-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="560cd-122">-IotHubName</span></span>
<span data-ttu-id="560cd-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="560cd-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="560cd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="560cd-124">-ResourceGroupName</span></span>
<span data-ttu-id="560cd-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="560cd-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="560cd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="560cd-126">-ResourceId</span></span>
<span data-ttu-id="560cd-127">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="560cd-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="560cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560cd-128">CommonParameters</span></span>
<span data-ttu-id="560cd-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="560cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560cd-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="560cd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560cd-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="560cd-131">INPUTS</span></span>

### <span data-ttu-id="560cd-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="560cd-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="560cd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="560cd-133">System.String</span></span>

## <span data-ttu-id="560cd-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="560cd-134">OUTPUTS</span></span>

### <span data-ttu-id="560cd-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="560cd-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="560cd-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices []</span><span class="sxs-lookup"><span data-stu-id="560cd-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="560cd-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="560cd-137">NOTES</span></span>

## <span data-ttu-id="560cd-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="560cd-138">RELATED LINKS</span></span>
