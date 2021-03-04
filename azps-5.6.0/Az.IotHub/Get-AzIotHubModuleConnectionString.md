---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 739153aebdaf8b089c0d180643056725a85f450a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889943"
---
# <span data-ttu-id="82868-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="82868-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="82868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82868-102">SYNOPSIS</span></span>
<span data-ttu-id="82868-103">Obter a cadeia de conexão de um módulo de dispositivo IoT de destino em um Hub de Iot.</span><span class="sxs-lookup"><span data-stu-id="82868-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="82868-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="82868-104">SYNTAX</span></span>

### <span data-ttu-id="82868-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="82868-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82868-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="82868-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82868-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="82868-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82868-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="82868-108">DESCRIPTION</span></span>
<span data-ttu-id="82868-109">Listar cadeia de conexão de todos os módulos ou um módulo especificado de um dispositivo de IoT de destino contido em um Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="82868-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="82868-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82868-110">EXAMPLES</span></span>

### <span data-ttu-id="82868-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="82868-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="82868-112">Mostrar todas as cadeias de conexão de módulos de um dispositivo IoT de destino em um Hub de Iot.</span><span class="sxs-lookup"><span data-stu-id="82868-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="82868-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="82868-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="82868-114">Obter a cadeia de conexão de módulo secundário de um dispositivo IoT de destino em um Hub de Iot.</span><span class="sxs-lookup"><span data-stu-id="82868-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="82868-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="82868-115">PARAMETERS</span></span>

### <span data-ttu-id="82868-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82868-116">-DefaultProfile</span></span>
<span data-ttu-id="82868-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="82868-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82868-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="82868-118">-DeviceId</span></span>
<span data-ttu-id="82868-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="82868-119">Target Device Id.</span></span>

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

### <span data-ttu-id="82868-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82868-120">-InputObject</span></span>
<span data-ttu-id="82868-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="82868-121">IotHub object</span></span>

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

### <span data-ttu-id="82868-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="82868-122">-IotHubName</span></span>
<span data-ttu-id="82868-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="82868-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="82868-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="82868-124">-KeyType</span></span>
<span data-ttu-id="82868-125">Tipo de chave de política de acesso compartilhado para auth.</span><span class="sxs-lookup"><span data-stu-id="82868-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="82868-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="82868-126">-ModuleId</span></span>
<span data-ttu-id="82868-127">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="82868-127">Target Module Id.</span></span>

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

### <span data-ttu-id="82868-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82868-128">-ResourceGroupName</span></span>
<span data-ttu-id="82868-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="82868-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="82868-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82868-130">-ResourceId</span></span>
<span data-ttu-id="82868-131">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="82868-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="82868-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82868-132">CommonParameters</span></span>
<span data-ttu-id="82868-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82868-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82868-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82868-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82868-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82868-135">INPUTS</span></span>

### <span data-ttu-id="82868-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="82868-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="82868-137">System.String</span><span class="sxs-lookup"><span data-stu-id="82868-137">System.String</span></span>

## <span data-ttu-id="82868-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="82868-138">OUTPUTS</span></span>

### <span data-ttu-id="82868-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="82868-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="82868-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="82868-140">NOTES</span></span>

## <span data-ttu-id="82868-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82868-141">RELATED LINKS</span></span>
