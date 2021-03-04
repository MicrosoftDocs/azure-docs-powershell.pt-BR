---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 09a4201d8add325c068358615a48a86c5e60911a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891354"
---
# <span data-ttu-id="2b7bf-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="2b7bf-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="2b7bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b7bf-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7bf-103">Crie um módulo em um dispositivo de IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="2b7bf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2b7bf-104">SYNTAX</span></span>

### <span data-ttu-id="2b7bf-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b7bf-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b7bf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2b7bf-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b7bf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2b7bf-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b7bf-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2b7bf-108">DESCRIPTION</span></span>
<span data-ttu-id="2b7bf-109">Crie um módulo em um dispositivo de IoT de destino com tipo de autorização diferente em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="2b7bf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b7bf-110">EXAMPLES</span></span>

### <span data-ttu-id="2b7bf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b7bf-111">Example 1</span></span>
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

<span data-ttu-id="2b7bf-112">Crie um módulo em um dispositivo de IoT de destino com autorização padrão (chave privada compartilhada).</span><span class="sxs-lookup"><span data-stu-id="2b7bf-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="2b7bf-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2b7bf-113">PARAMETERS</span></span>

### <span data-ttu-id="2b7bf-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="2b7bf-114">-AuthMethod</span></span>
<span data-ttu-id="2b7bf-115">O tipo de autorização com o qual uma entidade deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="2b7bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7bf-116">-DefaultProfile</span></span>
<span data-ttu-id="2b7bf-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b7bf-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2b7bf-118">-DeviceId</span></span>
<span data-ttu-id="2b7bf-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-119">Target Device Id.</span></span>

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

### <span data-ttu-id="2b7bf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b7bf-120">-InputObject</span></span>
<span data-ttu-id="2b7bf-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="2b7bf-121">IotHub object</span></span>

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

### <span data-ttu-id="2b7bf-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2b7bf-122">-IotHubName</span></span>
<span data-ttu-id="2b7bf-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="2b7bf-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2b7bf-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="2b7bf-124">-ModuleId</span></span>
<span data-ttu-id="2b7bf-125">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-125">Target Module Id.</span></span>

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

### <span data-ttu-id="2b7bf-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="2b7bf-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="2b7bf-127">Impressão digital explícita de certificado auto-assinado a ser usada para chave primária.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="2b7bf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b7bf-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b7bf-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2b7bf-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2b7bf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b7bf-130">-ResourceId</span></span>
<span data-ttu-id="2b7bf-131">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="2b7bf-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2b7bf-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="2b7bf-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="2b7bf-133">Impressão digital explícita de certificado auto-assinado a ser usada para chave secundária.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="2b7bf-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b7bf-134">-Confirm</span></span>
<span data-ttu-id="2b7bf-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b7bf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b7bf-136">-WhatIf</span></span>
<span data-ttu-id="2b7bf-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b7bf-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b7bf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7bf-139">CommonParameters</span></span>
<span data-ttu-id="2b7bf-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b7bf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7bf-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b7bf-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7bf-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b7bf-142">INPUTS</span></span>

### <span data-ttu-id="2b7bf-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2b7bf-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2b7bf-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2b7bf-144">System.String</span></span>

## <span data-ttu-id="2b7bf-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2b7bf-145">OUTPUTS</span></span>

### <span data-ttu-id="2b7bf-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="2b7bf-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="2b7bf-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="2b7bf-147">NOTES</span></span>

## <span data-ttu-id="2b7bf-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b7bf-148">RELATED LINKS</span></span>