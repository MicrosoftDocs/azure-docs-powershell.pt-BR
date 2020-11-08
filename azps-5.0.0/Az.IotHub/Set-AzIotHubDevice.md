---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126191"
---
# <span data-ttu-id="7e31b-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="7e31b-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="7e31b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e31b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e31b-103">Atualizar um dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="7e31b-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="7e31b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e31b-104">SYNTAX</span></span>

### <span data-ttu-id="7e31b-105">ResourceSetForStatus (padrão)</span><span class="sxs-lookup"><span data-stu-id="7e31b-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e31b-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="7e31b-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e31b-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="7e31b-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e31b-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7e31b-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e31b-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="7e31b-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e31b-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7e31b-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e31b-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="7e31b-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e31b-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="7e31b-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e31b-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7e31b-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e31b-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e31b-114">DESCRIPTION</span></span>
<span data-ttu-id="7e31b-115">Atualizar um dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="7e31b-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="7e31b-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e31b-116">EXAMPLES</span></span>

### <span data-ttu-id="7e31b-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7e31b-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="7e31b-118">Ative os recursos de borda do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e31b-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="7e31b-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7e31b-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="7e31b-120">Desabilite o status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e31b-120">Disable device status.</span></span>

### <span data-ttu-id="7e31b-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7e31b-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="7e31b-122">Atualize o tipo de autorização de um dispositivo Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="7e31b-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="7e31b-123">OS</span><span class="sxs-lookup"><span data-stu-id="7e31b-123">PARAMETERS</span></span>

### <span data-ttu-id="7e31b-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="7e31b-124">-AuthMethod</span></span>
<span data-ttu-id="7e31b-125">O tipo de autorização com a qual uma entidade será criada.</span><span class="sxs-lookup"><span data-stu-id="7e31b-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="7e31b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e31b-126">-DefaultProfile</span></span>
<span data-ttu-id="7e31b-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e31b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e31b-128">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="7e31b-128">-DeviceId</span></span>
<span data-ttu-id="7e31b-129">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="7e31b-129">Target Device Id.</span></span>

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

### <span data-ttu-id="7e31b-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7e31b-130">-EdgeEnabled</span></span>
<span data-ttu-id="7e31b-131">Sinalizador que indica a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="7e31b-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="7e31b-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e31b-132">-InputObject</span></span>
<span data-ttu-id="7e31b-133">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="7e31b-133">IotHub object</span></span>

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

### <span data-ttu-id="7e31b-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7e31b-134">-IotHubName</span></span>
<span data-ttu-id="7e31b-135">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="7e31b-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7e31b-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="7e31b-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="7e31b-137">Impressão digital de certificado autoassinado explícito para usar para a chave primária.</span><span class="sxs-lookup"><span data-stu-id="7e31b-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="7e31b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e31b-138">-ResourceGroupName</span></span>
<span data-ttu-id="7e31b-139">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7e31b-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7e31b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e31b-140">-ResourceId</span></span>
<span data-ttu-id="7e31b-141">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="7e31b-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7e31b-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="7e31b-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="7e31b-143">Impressão digital de certificado autoassinado explícito para usar para a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="7e31b-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="7e31b-144">-Status</span><span class="sxs-lookup"><span data-stu-id="7e31b-144">-Status</span></span>
<span data-ttu-id="7e31b-145">Definir o status do dispositivo durante a criação.</span><span class="sxs-lookup"><span data-stu-id="7e31b-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="7e31b-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="7e31b-146">-StatusReason</span></span>
<span data-ttu-id="7e31b-147">Descrição do status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e31b-147">Description for device status.</span></span>

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

### <span data-ttu-id="7e31b-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e31b-148">-Confirm</span></span>
<span data-ttu-id="7e31b-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e31b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e31b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e31b-150">-WhatIf</span></span>
<span data-ttu-id="7e31b-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e31b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e31b-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e31b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e31b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e31b-153">CommonParameters</span></span>
<span data-ttu-id="7e31b-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e31b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e31b-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e31b-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e31b-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e31b-156">INPUTS</span></span>

### <span data-ttu-id="7e31b-157">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7e31b-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7e31b-158">System. String</span><span class="sxs-lookup"><span data-stu-id="7e31b-158">System.String</span></span>

## <span data-ttu-id="7e31b-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e31b-159">OUTPUTS</span></span>

### <span data-ttu-id="7e31b-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="7e31b-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="7e31b-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e31b-161">NOTES</span></span>

## <span data-ttu-id="7e31b-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e31b-162">RELATED LINKS</span></span>
