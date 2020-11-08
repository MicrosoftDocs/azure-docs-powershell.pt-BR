---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 44e6451542a75e97a57890261a9a5f312e5ec466
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117775"
---
# <span data-ttu-id="a78a7-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="a78a7-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="a78a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a78a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a78a7-103">Crie um módulo em um dispositivo IoT de destino em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="a78a7-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="a78a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a78a7-104">SYNTAX</span></span>

### <span data-ttu-id="a78a7-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a78a7-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a78a7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a78a7-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a78a7-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="a78a7-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a78a7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a78a7-108">DESCRIPTION</span></span>
<span data-ttu-id="a78a7-109">Crie um módulo em um dispositivo IoT de destino com um tipo de autorização diferente em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="a78a7-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="a78a7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a78a7-110">EXAMPLES</span></span>

### <span data-ttu-id="a78a7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a78a7-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod shared_private_key

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

<span data-ttu-id="a78a7-112">Crie um módulo em um dispositivo IoT de destino com autorização padrão (chave privada compartilhada).</span><span class="sxs-lookup"><span data-stu-id="a78a7-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="a78a7-113">OS</span><span class="sxs-lookup"><span data-stu-id="a78a7-113">PARAMETERS</span></span>

### <span data-ttu-id="a78a7-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="a78a7-114">-AuthMethod</span></span>
<span data-ttu-id="a78a7-115">O tipo de autorização com a qual uma entidade será criada.</span><span class="sxs-lookup"><span data-stu-id="a78a7-115">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a78a7-116">-DefaultProfile</span></span>
<span data-ttu-id="a78a7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a78a7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a78a7-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="a78a7-118">-DeviceId</span></span>
<span data-ttu-id="a78a7-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="a78a7-119">Target Device Id.</span></span>

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

### <span data-ttu-id="a78a7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a78a7-120">-InputObject</span></span>
<span data-ttu-id="a78a7-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="a78a7-121">IotHub object</span></span>

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

### <span data-ttu-id="a78a7-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a78a7-122">-IotHubName</span></span>
<span data-ttu-id="a78a7-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="a78a7-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a78a7-124">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="a78a7-124">-ModuleId</span></span>
<span data-ttu-id="a78a7-125">ID do módulo de destino.</span><span class="sxs-lookup"><span data-stu-id="a78a7-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78a7-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="a78a7-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="a78a7-127">Impressão digital de certificado autoassinado explícito para usar para a chave primária.</span><span class="sxs-lookup"><span data-stu-id="a78a7-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="a78a7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a78a7-128">-ResourceGroupName</span></span>
<span data-ttu-id="a78a7-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a78a7-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a78a7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a78a7-130">-ResourceId</span></span>
<span data-ttu-id="a78a7-131">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="a78a7-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a78a7-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="a78a7-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="a78a7-133">Impressão digital de certificado autoassinado explícito para usar para a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="a78a7-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78a7-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a78a7-134">-Confirm</span></span>
<span data-ttu-id="a78a7-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a78a7-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78a7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a78a7-136">-WhatIf</span></span>
<span data-ttu-id="a78a7-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a78a7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a78a7-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a78a7-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78a7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a78a7-139">CommonParameters</span></span>
<span data-ttu-id="a78a7-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a78a7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a78a7-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a78a7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a78a7-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a78a7-142">INPUTS</span></span>

### <span data-ttu-id="a78a7-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a78a7-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a78a7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a78a7-144">System.String</span></span>

## <span data-ttu-id="a78a7-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a78a7-145">OUTPUTS</span></span>

### <span data-ttu-id="a78a7-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="a78a7-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="a78a7-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a78a7-147">NOTES</span></span>

## <span data-ttu-id="a78a7-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a78a7-148">RELATED LINKS</span></span>