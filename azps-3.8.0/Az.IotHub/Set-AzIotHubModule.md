---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c88ee9af5d03b50ed80bf677ccff6e7236668756
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941397"
---
# <span data-ttu-id="5fc9a-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="5fc9a-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="5fc9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc9a-103">Atualize um módulo em um dispositivo IoT de destino em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="5fc9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fc9a-104">SYNTAX</span></span>

### <span data-ttu-id="5fc9a-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5fc9a-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fc9a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5fc9a-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fc9a-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="5fc9a-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fc9a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fc9a-108">DESCRIPTION</span></span>
<span data-ttu-id="5fc9a-109">Atualize um módulo em um dispositivo IoT de destino em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="5fc9a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fc9a-110">EXAMPLES</span></span>

### <span data-ttu-id="5fc9a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5fc9a-111">Example 1</span></span>
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

<span data-ttu-id="5fc9a-112">Atualize o tipo de autorização de um módulo de dispositivo IOT.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="5fc9a-113">OS</span><span class="sxs-lookup"><span data-stu-id="5fc9a-113">PARAMETERS</span></span>

### <span data-ttu-id="5fc9a-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="5fc9a-114">-AuthMethod</span></span>
<span data-ttu-id="5fc9a-115">O tipo de autorização com a qual uma entidade será criada.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="5fc9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc9a-116">-DefaultProfile</span></span>
<span data-ttu-id="5fc9a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fc9a-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="5fc9a-118">-DeviceId</span></span>
<span data-ttu-id="5fc9a-119">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-119">Target Device Id.</span></span>

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

### <span data-ttu-id="5fc9a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fc9a-120">-InputObject</span></span>
<span data-ttu-id="5fc9a-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="5fc9a-121">IotHub object</span></span>

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

### <span data-ttu-id="5fc9a-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5fc9a-122">-IotHubName</span></span>
<span data-ttu-id="5fc9a-123">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="5fc9a-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5fc9a-124">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="5fc9a-124">-ModuleId</span></span>
<span data-ttu-id="5fc9a-125">ID do módulo de destino.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-125">Target Module Id.</span></span>

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

### <span data-ttu-id="5fc9a-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="5fc9a-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="5fc9a-127">Impressão digital de certificado autoassinado explícito para usar para a chave primária.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="5fc9a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fc9a-128">-ResourceGroupName</span></span>
<span data-ttu-id="5fc9a-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5fc9a-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5fc9a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fc9a-130">-ResourceId</span></span>
<span data-ttu-id="5fc9a-131">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="5fc9a-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5fc9a-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="5fc9a-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="5fc9a-133">Impressão digital de certificado autoassinado explícito para usar para a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="5fc9a-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5fc9a-134">-Confirm</span></span>
<span data-ttu-id="5fc9a-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fc9a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fc9a-136">-WhatIf</span></span>
<span data-ttu-id="5fc9a-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fc9a-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fc9a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc9a-139">CommonParameters</span></span>
<span data-ttu-id="5fc9a-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fc9a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc9a-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fc9a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc9a-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fc9a-142">INPUTS</span></span>

### <span data-ttu-id="5fc9a-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5fc9a-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5fc9a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5fc9a-144">System.String</span></span>

## <span data-ttu-id="5fc9a-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fc9a-145">OUTPUTS</span></span>

### <span data-ttu-id="5fc9a-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="5fc9a-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="5fc9a-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fc9a-147">NOTES</span></span>

## <span data-ttu-id="5fc9a-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fc9a-148">RELATED LINKS</span></span>