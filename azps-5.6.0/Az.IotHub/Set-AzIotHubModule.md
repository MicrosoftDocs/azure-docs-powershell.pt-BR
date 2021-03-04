---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c5e31e1f1fcaf4e889e0b1f3bb85b55a4b0388b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893162"
---
# <span data-ttu-id="6f205-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="6f205-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="6f205-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f205-102">SYNOPSIS</span></span>
<span data-ttu-id="6f205-103">Atualize um módulo em um dispositivo de IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="6f205-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="6f205-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6f205-104">SYNTAX</span></span>

### <span data-ttu-id="6f205-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6f205-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f205-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f205-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f205-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6f205-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f205-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6f205-108">DESCRIPTION</span></span>
<span data-ttu-id="6f205-109">Atualize um módulo em um dispositivo de IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="6f205-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="6f205-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f205-110">EXAMPLES</span></span>

### <span data-ttu-id="6f205-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f205-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod "shared_private_key"

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

<span data-ttu-id="6f205-112">Atualizar o tipo de autorização de um módulo de dispositivo Iot.</span><span class="sxs-lookup"><span data-stu-id="6f205-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="6f205-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6f205-113">PARAMETERS</span></span>

### <span data-ttu-id="6f205-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="6f205-114">-AuthMethod</span></span>
<span data-ttu-id="6f205-115">O tipo de autorização com o qual uma entidade deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="6f205-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="6f205-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f205-116">-DefaultProfile</span></span>
<span data-ttu-id="6f205-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f205-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f205-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6f205-118">-DeviceId</span></span>
<span data-ttu-id="6f205-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="6f205-119">Target Device Id.</span></span>

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

### <span data-ttu-id="6f205-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f205-120">-InputObject</span></span>
<span data-ttu-id="6f205-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="6f205-121">IotHub object</span></span>

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

### <span data-ttu-id="6f205-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6f205-122">-IotHubName</span></span>
<span data-ttu-id="6f205-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="6f205-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6f205-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="6f205-124">-ModuleId</span></span>
<span data-ttu-id="6f205-125">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="6f205-125">Target Module Id.</span></span>

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

### <span data-ttu-id="6f205-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="6f205-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="6f205-127">Impressão digital explícita de certificado auto-assinado a ser usada para chave primária.</span><span class="sxs-lookup"><span data-stu-id="6f205-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="6f205-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f205-128">-ResourceGroupName</span></span>
<span data-ttu-id="6f205-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="6f205-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6f205-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f205-130">-ResourceId</span></span>
<span data-ttu-id="6f205-131">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="6f205-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6f205-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="6f205-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="6f205-133">Impressão digital explícita de certificado auto-assinado a ser usada para chave secundária.</span><span class="sxs-lookup"><span data-stu-id="6f205-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="6f205-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f205-134">-Confirm</span></span>
<span data-ttu-id="6f205-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f205-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f205-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f205-136">-WhatIf</span></span>
<span data-ttu-id="6f205-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6f205-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f205-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6f205-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f205-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f205-139">CommonParameters</span></span>
<span data-ttu-id="6f205-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f205-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f205-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f205-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f205-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f205-142">INPUTS</span></span>

### <span data-ttu-id="6f205-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6f205-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6f205-144">System.String</span><span class="sxs-lookup"><span data-stu-id="6f205-144">System.String</span></span>

## <span data-ttu-id="6f205-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6f205-145">OUTPUTS</span></span>

### <span data-ttu-id="6f205-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="6f205-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="6f205-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="6f205-147">NOTES</span></span>

## <span data-ttu-id="6f205-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f205-148">RELATED LINKS</span></span>