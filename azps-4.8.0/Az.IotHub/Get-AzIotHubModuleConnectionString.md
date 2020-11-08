---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114920"
---
# <span data-ttu-id="05636-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="05636-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="05636-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05636-102">SYNOPSIS</span></span>
<span data-ttu-id="05636-103">Obter a cadeia de conexão de um módulo de dispositivo IoT de destino em um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="05636-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="05636-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05636-104">SYNTAX</span></span>

### <span data-ttu-id="05636-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="05636-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05636-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="05636-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05636-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="05636-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05636-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05636-108">DESCRIPTION</span></span>
<span data-ttu-id="05636-109">Listar a cadeia de conexão de todos os módulos ou um módulo especificado de um dispositivo IoT de destino contido em um hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="05636-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="05636-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05636-110">EXAMPLES</span></span>

### <span data-ttu-id="05636-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="05636-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="05636-112">Mostrar todos os módulos cadeia de conexão de um dispositivo IoT de destino em um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="05636-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="05636-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="05636-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="05636-114">Obtenha a cadeia de conexão do módulo secundário de um dispositivo IoT de destino em um hub IOT.</span><span class="sxs-lookup"><span data-stu-id="05636-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="05636-115">OS</span><span class="sxs-lookup"><span data-stu-id="05636-115">PARAMETERS</span></span>

### <span data-ttu-id="05636-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05636-116">-DefaultProfile</span></span>
<span data-ttu-id="05636-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05636-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05636-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="05636-118">-DeviceId</span></span>
<span data-ttu-id="05636-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="05636-119">Target Device Id.</span></span>

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

### <span data-ttu-id="05636-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05636-120">-InputObject</span></span>
<span data-ttu-id="05636-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="05636-121">IotHub object</span></span>

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

### <span data-ttu-id="05636-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="05636-122">-IotHubName</span></span>
<span data-ttu-id="05636-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="05636-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="05636-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="05636-124">-KeyType</span></span>
<span data-ttu-id="05636-125">Tipo de chave da política de acesso compartilhado para autenticação.</span><span class="sxs-lookup"><span data-stu-id="05636-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="05636-126">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="05636-126">-ModuleId</span></span>
<span data-ttu-id="05636-127">ID do módulo de destino.</span><span class="sxs-lookup"><span data-stu-id="05636-127">Target Module Id.</span></span>

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

### <span data-ttu-id="05636-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05636-128">-ResourceGroupName</span></span>
<span data-ttu-id="05636-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="05636-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="05636-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05636-130">-ResourceId</span></span>
<span data-ttu-id="05636-131">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="05636-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="05636-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05636-132">CommonParameters</span></span>
<span data-ttu-id="05636-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05636-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05636-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05636-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05636-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05636-135">INPUTS</span></span>

### <span data-ttu-id="05636-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="05636-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="05636-137">System. String</span><span class="sxs-lookup"><span data-stu-id="05636-137">System.String</span></span>

## <span data-ttu-id="05636-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05636-138">OUTPUTS</span></span>

### <span data-ttu-id="05636-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="05636-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="05636-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05636-140">NOTES</span></span>

## <span data-ttu-id="05636-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05636-141">RELATED LINKS</span></span>
