---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943000"
---
# <span data-ttu-id="3c093-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="3c093-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="3c093-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c093-102">SYNOPSIS</span></span>
<span data-ttu-id="3c093-103">Obter a cadeia de conexão de um dispositivo IoT de destino em um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="3c093-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="3c093-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c093-104">SYNTAX</span></span>

### <span data-ttu-id="3c093-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3c093-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c093-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3c093-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c093-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="3c093-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c093-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c093-108">DESCRIPTION</span></span>
<span data-ttu-id="3c093-109">Listar cadeia de conexão de todos os dispositivos ou um dispositivo IoT de destino contido em um hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c093-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="3c093-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c093-110">EXAMPLES</span></span>

### <span data-ttu-id="3c093-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c093-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="3c093-112">Mostrar cadeia de conexão de todos os dispositivos em um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="3c093-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="3c093-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3c093-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="3c093-114">Obter a cadeia de conexão secundária de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="3c093-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="3c093-115">OS</span><span class="sxs-lookup"><span data-stu-id="3c093-115">PARAMETERS</span></span>

### <span data-ttu-id="3c093-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c093-116">-DefaultProfile</span></span>
<span data-ttu-id="3c093-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c093-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c093-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="3c093-118">-DeviceId</span></span>
<span data-ttu-id="3c093-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="3c093-119">Target Device Id.</span></span>

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

### <span data-ttu-id="3c093-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c093-120">-InputObject</span></span>
<span data-ttu-id="3c093-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="3c093-121">IotHub object</span></span>

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

### <span data-ttu-id="3c093-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3c093-122">-IotHubName</span></span>
<span data-ttu-id="3c093-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="3c093-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3c093-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3c093-124">-KeyType</span></span>
<span data-ttu-id="3c093-125">Tipo de chave da política de acesso compartilhado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="3c093-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c093-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c093-126">-ResourceGroupName</span></span>
<span data-ttu-id="3c093-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3c093-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3c093-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c093-128">-ResourceId</span></span>
<span data-ttu-id="3c093-129">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="3c093-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3c093-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c093-130">CommonParameters</span></span>
<span data-ttu-id="3c093-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c093-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c093-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c093-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c093-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c093-133">INPUTS</span></span>

### <span data-ttu-id="3c093-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3c093-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3c093-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3c093-135">System.String</span></span>

## <span data-ttu-id="3c093-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c093-136">OUTPUTS</span></span>

### <span data-ttu-id="3c093-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="3c093-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="3c093-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c093-138">NOTES</span></span>

## <span data-ttu-id="3c093-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c093-139">RELATED LINKS</span></span>
