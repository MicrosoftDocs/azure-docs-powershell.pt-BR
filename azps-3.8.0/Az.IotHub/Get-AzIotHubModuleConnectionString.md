---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943383"
---
# <span data-ttu-id="3e733-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="3e733-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="3e733-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e733-102">SYNOPSIS</span></span>
<span data-ttu-id="3e733-103">Obter a cadeia de conexão de um módulo de dispositivo IoT de destino em um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="3e733-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="3e733-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e733-104">SYNTAX</span></span>

### <span data-ttu-id="3e733-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3e733-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e733-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3e733-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e733-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="3e733-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e733-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e733-108">DESCRIPTION</span></span>
<span data-ttu-id="3e733-109">Listar a cadeia de conexão de todos os módulos ou um módulo especificado de um dispositivo IoT de destino contido em um hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e733-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="3e733-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e733-110">EXAMPLES</span></span>

### <span data-ttu-id="3e733-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3e733-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="3e733-112">Mostrar todos os módulos cadeia de conexão de um dispositivo IoT de destino em um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="3e733-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="3e733-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3e733-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="3e733-114">Obtenha a cadeia de conexão do módulo secundário de um dispositivo IoT de destino em um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="3e733-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="3e733-115">OS</span><span class="sxs-lookup"><span data-stu-id="3e733-115">PARAMETERS</span></span>

### <span data-ttu-id="3e733-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e733-116">-DefaultProfile</span></span>
<span data-ttu-id="3e733-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e733-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e733-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="3e733-118">-DeviceId</span></span>
<span data-ttu-id="3e733-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="3e733-119">Target Device Id.</span></span>

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

### <span data-ttu-id="3e733-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e733-120">-InputObject</span></span>
<span data-ttu-id="3e733-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="3e733-121">IotHub object</span></span>

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

### <span data-ttu-id="3e733-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3e733-122">-IotHubName</span></span>
<span data-ttu-id="3e733-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="3e733-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3e733-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3e733-124">-KeyType</span></span>
<span data-ttu-id="3e733-125">Tipo de chave da política de acesso compartilhado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="3e733-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="3e733-126">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="3e733-126">-ModuleId</span></span>
<span data-ttu-id="3e733-127">ID do módulo de destino.</span><span class="sxs-lookup"><span data-stu-id="3e733-127">Target Module Id.</span></span>

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

### <span data-ttu-id="3e733-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e733-128">-ResourceGroupName</span></span>
<span data-ttu-id="3e733-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3e733-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3e733-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e733-130">-ResourceId</span></span>
<span data-ttu-id="3e733-131">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="3e733-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3e733-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e733-132">CommonParameters</span></span>
<span data-ttu-id="3e733-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e733-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e733-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e733-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e733-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e733-135">INPUTS</span></span>

### <span data-ttu-id="3e733-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3e733-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3e733-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3e733-137">System.String</span></span>

## <span data-ttu-id="3e733-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e733-138">OUTPUTS</span></span>

### <span data-ttu-id="3e733-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="3e733-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="3e733-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e733-140">NOTES</span></span>

## <span data-ttu-id="3e733-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e733-141">RELATED LINKS</span></span>
