---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: bacb7575f7c4bf8a29d84e507e40d45ffc69ec1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889960"
---
# <span data-ttu-id="a9218-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="a9218-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="a9218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9218-102">SYNOPSIS</span></span>
<span data-ttu-id="a9218-103">Obter a cadeia de conexão de um dispositivo de IoT de destino em um Hub de Iot.</span><span class="sxs-lookup"><span data-stu-id="a9218-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="a9218-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a9218-104">SYNTAX</span></span>

### <span data-ttu-id="a9218-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a9218-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9218-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9218-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9218-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a9218-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9218-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a9218-108">DESCRIPTION</span></span>
<span data-ttu-id="a9218-109">Listar cadeia de conexão de todos os dispositivos ou um dispositivo IoT de destino contido em um Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9218-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="a9218-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9218-110">EXAMPLES</span></span>

### <span data-ttu-id="a9218-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9218-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="a9218-112">Mostrar todas as cadeias de conexão de dispositivos em um Hub de Iot.</span><span class="sxs-lookup"><span data-stu-id="a9218-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="a9218-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a9218-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="a9218-114">Obter a cadeia de caracteres de conexão secundária de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="a9218-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="a9218-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a9218-115">PARAMETERS</span></span>

### <span data-ttu-id="a9218-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9218-116">-DefaultProfile</span></span>
<span data-ttu-id="a9218-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9218-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9218-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a9218-118">-DeviceId</span></span>
<span data-ttu-id="a9218-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="a9218-119">Target Device Id.</span></span>

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

### <span data-ttu-id="a9218-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9218-120">-InputObject</span></span>
<span data-ttu-id="a9218-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="a9218-121">IotHub object</span></span>

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

### <span data-ttu-id="a9218-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a9218-122">-IotHubName</span></span>
<span data-ttu-id="a9218-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="a9218-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a9218-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="a9218-124">-KeyType</span></span>
<span data-ttu-id="a9218-125">Tipo de chave de política de acesso compartilhado para auth.</span><span class="sxs-lookup"><span data-stu-id="a9218-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="a9218-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9218-126">-ResourceGroupName</span></span>
<span data-ttu-id="a9218-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="a9218-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a9218-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9218-128">-ResourceId</span></span>
<span data-ttu-id="a9218-129">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="a9218-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a9218-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9218-130">CommonParameters</span></span>
<span data-ttu-id="a9218-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9218-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9218-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9218-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9218-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9218-133">INPUTS</span></span>

### <span data-ttu-id="a9218-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a9218-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a9218-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a9218-135">System.String</span></span>

## <span data-ttu-id="a9218-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a9218-136">OUTPUTS</span></span>

### <span data-ttu-id="a9218-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="a9218-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="a9218-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="a9218-138">NOTES</span></span>

## <span data-ttu-id="a9218-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9218-139">RELATED LINKS</span></span>
