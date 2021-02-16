---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113136"
---
# <span data-ttu-id="1f68c-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="1f68c-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="1f68c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f68c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f68c-103">Obter a cadeia de conexão de um módulo de dispositivo IoT de destino em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="1f68c-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="1f68c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f68c-104">SYNTAX</span></span>

### <span data-ttu-id="1f68c-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1f68c-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f68c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1f68c-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f68c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1f68c-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f68c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f68c-108">DESCRIPTION</span></span>
<span data-ttu-id="1f68c-109">Cadeia de conexão de lista de todos os módulos ou um módulo especificado de um dispositivo IoT de destino contido em um Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="1f68c-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="1f68c-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f68c-110">EXAMPLES</span></span>

### <span data-ttu-id="1f68c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f68c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="1f68c-112">Mostrar todas as cadeias de conexão de módulos de um dispositivo IoT de destino em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="1f68c-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="1f68c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1f68c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="1f68c-114">Obter a cadeia de conexão de módulo secundário de um dispositivo IoT de destino em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="1f68c-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="1f68c-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f68c-115">PARAMETERS</span></span>

### <span data-ttu-id="1f68c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f68c-116">-DefaultProfile</span></span>
<span data-ttu-id="1f68c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f68c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f68c-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1f68c-118">-DeviceId</span></span>
<span data-ttu-id="1f68c-119">ID do Dispositivo de Destino.</span><span class="sxs-lookup"><span data-stu-id="1f68c-119">Target Device Id.</span></span>

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

### <span data-ttu-id="1f68c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f68c-120">-InputObject</span></span>
<span data-ttu-id="1f68c-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="1f68c-121">IotHub object</span></span>

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

### <span data-ttu-id="1f68c-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1f68c-122">-IotHubName</span></span>
<span data-ttu-id="1f68c-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="1f68c-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1f68c-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1f68c-124">-KeyType</span></span>
<span data-ttu-id="1f68c-125">Tipo de chave de política de acesso compartilhado para auth.</span><span class="sxs-lookup"><span data-stu-id="1f68c-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="1f68c-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="1f68c-126">-ModuleId</span></span>
<span data-ttu-id="1f68c-127">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="1f68c-127">Target Module Id.</span></span>

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

### <span data-ttu-id="1f68c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f68c-128">-ResourceGroupName</span></span>
<span data-ttu-id="1f68c-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1f68c-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1f68c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f68c-130">-ResourceId</span></span>
<span data-ttu-id="1f68c-131">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="1f68c-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1f68c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f68c-132">CommonParameters</span></span>
<span data-ttu-id="1f68c-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f68c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f68c-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f68c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f68c-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="1f68c-135">INPUTS</span></span>

### <span data-ttu-id="1f68c-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1f68c-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1f68c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1f68c-137">System.String</span></span>

## <span data-ttu-id="1f68c-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="1f68c-138">OUTPUTS</span></span>

### <span data-ttu-id="1f68c-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="1f68c-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="1f68c-140">Notas</span><span class="sxs-lookup"><span data-stu-id="1f68c-140">NOTES</span></span>

## <span data-ttu-id="1f68c-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f68c-141">RELATED LINKS</span></span>
