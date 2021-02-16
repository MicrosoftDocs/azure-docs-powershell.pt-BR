---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c88ee9af5d03b50ed80bf677ccff6e7236668756
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113121"
---
# <span data-ttu-id="318b4-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="318b4-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="318b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="318b4-102">SYNOPSIS</span></span>
<span data-ttu-id="318b4-103">Atualize um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="318b4-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="318b4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="318b4-104">SYNTAX</span></span>

### <span data-ttu-id="318b4-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="318b4-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="318b4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="318b4-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="318b4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="318b4-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="318b4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="318b4-108">DESCRIPTION</span></span>
<span data-ttu-id="318b4-109">Atualize um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="318b4-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="318b4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="318b4-110">EXAMPLES</span></span>

### <span data-ttu-id="318b4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="318b4-111">Example 1</span></span>
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

<span data-ttu-id="318b4-112">Tipo de autorização de atualização de um módulo de dispositivo Iot.</span><span class="sxs-lookup"><span data-stu-id="318b4-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="318b4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="318b4-113">PARAMETERS</span></span>

### <span data-ttu-id="318b4-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="318b4-114">-AuthMethod</span></span>
<span data-ttu-id="318b4-115">O tipo de autorização com o qual uma entidade deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="318b4-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="318b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318b4-116">-DefaultProfile</span></span>
<span data-ttu-id="318b4-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="318b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="318b4-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="318b4-118">-DeviceId</span></span>
<span data-ttu-id="318b4-119">ID do Dispositivo de Destino.</span><span class="sxs-lookup"><span data-stu-id="318b4-119">Target Device Id.</span></span>

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

### <span data-ttu-id="318b4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="318b4-120">-InputObject</span></span>
<span data-ttu-id="318b4-121">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="318b4-121">IotHub object</span></span>

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

### <span data-ttu-id="318b4-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="318b4-122">-IotHubName</span></span>
<span data-ttu-id="318b4-123">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="318b4-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="318b4-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="318b4-124">-ModuleId</span></span>
<span data-ttu-id="318b4-125">ID do Módulo de Destino.</span><span class="sxs-lookup"><span data-stu-id="318b4-125">Target Module Id.</span></span>

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

### <span data-ttu-id="318b4-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="318b4-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="318b4-127">Impressão explícita de certificado auto-assinado a ser usada para chave primária.</span><span class="sxs-lookup"><span data-stu-id="318b4-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="318b4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="318b4-128">-ResourceGroupName</span></span>
<span data-ttu-id="318b4-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="318b4-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="318b4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="318b4-130">-ResourceId</span></span>
<span data-ttu-id="318b4-131">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="318b4-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="318b4-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="318b4-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="318b4-133">Impressão explícita de certificado auto-assinado a ser usada para chave secundária.</span><span class="sxs-lookup"><span data-stu-id="318b4-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="318b4-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="318b4-134">-Confirm</span></span>
<span data-ttu-id="318b4-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="318b4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="318b4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="318b4-136">-WhatIf</span></span>
<span data-ttu-id="318b4-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="318b4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="318b4-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="318b4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="318b4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318b4-139">CommonParameters</span></span>
<span data-ttu-id="318b4-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318b4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318b4-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="318b4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318b4-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="318b4-142">INPUTS</span></span>

### <span data-ttu-id="318b4-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="318b4-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="318b4-144">System.String</span><span class="sxs-lookup"><span data-stu-id="318b4-144">System.String</span></span>

## <span data-ttu-id="318b4-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="318b4-145">OUTPUTS</span></span>

### <span data-ttu-id="318b4-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="318b4-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="318b4-147">Notas</span><span class="sxs-lookup"><span data-stu-id="318b4-147">NOTES</span></span>

## <span data-ttu-id="318b4-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="318b4-148">RELATED LINKS</span></span>