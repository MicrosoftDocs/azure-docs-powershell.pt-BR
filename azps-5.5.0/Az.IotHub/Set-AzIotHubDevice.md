---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116730"
---
# <span data-ttu-id="e8d9d-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="e8d9d-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="e8d9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d9d-103">Atualizar um dispositivo do Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="e8d9d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8d9d-104">SYNTAX</span></span>

### <span data-ttu-id="e8d9d-105">ResourceSetForStatus (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e8d9d-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8d9d-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="e8d9d-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8d9d-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="e8d9d-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8d9d-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="e8d9d-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8d9d-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="e8d9d-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8d9d-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="e8d9d-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8d9d-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="e8d9d-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8d9d-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="e8d9d-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8d9d-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="e8d9d-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8d9d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8d9d-114">DESCRIPTION</span></span>
<span data-ttu-id="e8d9d-115">Atualizar um dispositivo do Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="e8d9d-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e8d9d-116">EXAMPLES</span></span>

### <span data-ttu-id="e8d9d-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8d9d-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="e8d9d-118">Ativar recursos de borda para dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="e8d9d-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e8d9d-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="e8d9d-120">Desabilitar o status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-120">Disable device status.</span></span>

### <span data-ttu-id="e8d9d-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e8d9d-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="e8d9d-122">Tipo de autorização de atualização de um dispositivo Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="e8d9d-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8d9d-123">PARAMETERS</span></span>

### <span data-ttu-id="e8d9d-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="e8d9d-124">-AuthMethod</span></span>
<span data-ttu-id="e8d9d-125">O tipo de autorização com o qual uma entidade deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="e8d9d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d9d-126">-DefaultProfile</span></span>
<span data-ttu-id="e8d9d-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8d9d-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e8d9d-128">-DeviceId</span></span>
<span data-ttu-id="e8d9d-129">ID do Dispositivo de Destino.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-129">Target Device Id.</span></span>

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

### <span data-ttu-id="e8d9d-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="e8d9d-130">-EdgeEnabled</span></span>
<span data-ttu-id="e8d9d-131">Sinalizador indicando a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="e8d9d-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8d9d-132">-InputObject</span></span>
<span data-ttu-id="e8d9d-133">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="e8d9d-133">IotHub object</span></span>

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

### <span data-ttu-id="e8d9d-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e8d9d-134">-IotHubName</span></span>
<span data-ttu-id="e8d9d-135">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="e8d9d-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e8d9d-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="e8d9d-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="e8d9d-137">Impressão explícita de certificado auto-assinado a ser usada para chave primária.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="e8d9d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8d9d-138">-ResourceGroupName</span></span>
<span data-ttu-id="e8d9d-139">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e8d9d-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e8d9d-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8d9d-140">-ResourceId</span></span>
<span data-ttu-id="e8d9d-141">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="e8d9d-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e8d9d-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="e8d9d-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="e8d9d-143">Impressão explícita de certificado auto-assinado a ser usada para chave secundária.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="e8d9d-144">-Status</span><span class="sxs-lookup"><span data-stu-id="e8d9d-144">-Status</span></span>
<span data-ttu-id="e8d9d-145">Definir o status do dispositivo durante a criação.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="e8d9d-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="e8d9d-146">-StatusReason</span></span>
<span data-ttu-id="e8d9d-147">Descrição do status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-147">Description for device status.</span></span>

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

### <span data-ttu-id="e8d9d-148">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e8d9d-148">-Confirm</span></span>
<span data-ttu-id="e8d9d-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8d9d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8d9d-150">-WhatIf</span></span>
<span data-ttu-id="e8d9d-151">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8d9d-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8d9d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d9d-153">CommonParameters</span></span>
<span data-ttu-id="e8d9d-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8d9d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d9d-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8d9d-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d9d-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="e8d9d-156">INPUTS</span></span>

### <span data-ttu-id="e8d9d-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e8d9d-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e8d9d-158">System.String</span><span class="sxs-lookup"><span data-stu-id="e8d9d-158">System.String</span></span>

## <span data-ttu-id="e8d9d-159">Saídas</span><span class="sxs-lookup"><span data-stu-id="e8d9d-159">OUTPUTS</span></span>

### <span data-ttu-id="e8d9d-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="e8d9d-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="e8d9d-161">Notas</span><span class="sxs-lookup"><span data-stu-id="e8d9d-161">NOTES</span></span>

## <span data-ttu-id="e8d9d-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8d9d-162">RELATED LINKS</span></span>
