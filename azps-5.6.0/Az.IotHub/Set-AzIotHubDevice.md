---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: c164286e71b198ab19dd1928d6ee495014295306
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885869"
---
# <span data-ttu-id="9b3be-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="9b3be-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="9b3be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b3be-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3be-103">Atualize um dispositivo IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="9b3be-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="9b3be-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9b3be-104">SYNTAX</span></span>

### <span data-ttu-id="9b3be-105">ResourceSetForStatus (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9b3be-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3be-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="9b3be-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3be-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="9b3be-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3be-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9b3be-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3be-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="9b3be-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b3be-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9b3be-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3be-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="9b3be-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3be-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="9b3be-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b3be-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9b3be-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b3be-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9b3be-114">DESCRIPTION</span></span>
<span data-ttu-id="9b3be-115">Atualize um dispositivo IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="9b3be-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="9b3be-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b3be-116">EXAMPLES</span></span>

### <span data-ttu-id="9b3be-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b3be-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="9b3be-118">Ativar recursos de borda para dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b3be-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="9b3be-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9b3be-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="9b3be-120">Desabilitar o status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b3be-120">Disable device status.</span></span>

### <span data-ttu-id="9b3be-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9b3be-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="9b3be-122">Atualizar o tipo de autorização de um dispositivo Iot Hub.</span><span class="sxs-lookup"><span data-stu-id="9b3be-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="9b3be-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9b3be-123">PARAMETERS</span></span>

### <span data-ttu-id="9b3be-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="9b3be-124">-AuthMethod</span></span>
<span data-ttu-id="9b3be-125">O tipo de autorização com o qual uma entidade deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="9b3be-125">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3be-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3be-126">-DefaultProfile</span></span>
<span data-ttu-id="9b3be-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b3be-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b3be-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9b3be-128">-DeviceId</span></span>
<span data-ttu-id="9b3be-129">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="9b3be-129">Target Device Id.</span></span>

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

### <span data-ttu-id="9b3be-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9b3be-130">-EdgeEnabled</span></span>
<span data-ttu-id="9b3be-131">Sinalizador indicando a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="9b3be-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: InputObjectSetForEdgeEnabled, ResourceSetForEdgeEnabled, ResourceIdSetForEdgeEnabled
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3be-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b3be-132">-InputObject</span></span>
<span data-ttu-id="9b3be-133">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="9b3be-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSetForAuth, InputObjectSetForStatus, InputObjectSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b3be-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9b3be-134">-IotHubName</span></span>
<span data-ttu-id="9b3be-135">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="9b3be-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3be-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9b3be-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="9b3be-137">Impressão digital explícita de certificado auto-assinado a ser usada para chave primária.</span><span class="sxs-lookup"><span data-stu-id="9b3be-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3be-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b3be-138">-ResourceGroupName</span></span>
<span data-ttu-id="9b3be-139">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="9b3be-139">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3be-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b3be-140">-ResourceId</span></span>
<span data-ttu-id="9b3be-141">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="9b3be-141">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetForAuth, ResourceIdSetForStatus, ResourceIdSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b3be-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="9b3be-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="9b3be-143">Impressão digital explícita de certificado auto-assinado a ser usada para chave secundária.</span><span class="sxs-lookup"><span data-stu-id="9b3be-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3be-144">-Status</span><span class="sxs-lookup"><span data-stu-id="9b3be-144">-Status</span></span>
<span data-ttu-id="9b3be-145">Definir o status do dispositivo após a criação.</span><span class="sxs-lookup"><span data-stu-id="9b3be-145">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3be-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="9b3be-146">-StatusReason</span></span>
<span data-ttu-id="9b3be-147">Descrição do status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b3be-147">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3be-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b3be-148">-Confirm</span></span>
<span data-ttu-id="9b3be-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b3be-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b3be-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b3be-150">-WhatIf</span></span>
<span data-ttu-id="9b3be-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b3be-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b3be-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b3be-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b3be-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3be-153">CommonParameters</span></span>
<span data-ttu-id="9b3be-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b3be-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3be-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b3be-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3be-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b3be-156">INPUTS</span></span>

### <span data-ttu-id="9b3be-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9b3be-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9b3be-158">System.String</span><span class="sxs-lookup"><span data-stu-id="9b3be-158">System.String</span></span>

## <span data-ttu-id="9b3be-159">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9b3be-159">OUTPUTS</span></span>

### <span data-ttu-id="9b3be-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="9b3be-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="9b3be-161">NOTES</span><span class="sxs-lookup"><span data-stu-id="9b3be-161">NOTES</span></span>

## <span data-ttu-id="9b3be-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b3be-162">RELATED LINKS</span></span>
