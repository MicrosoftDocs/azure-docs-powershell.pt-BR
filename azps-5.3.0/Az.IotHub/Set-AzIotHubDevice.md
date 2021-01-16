---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272801"
---
# <span data-ttu-id="ed015-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ed015-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="ed015-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed015-102">SYNOPSIS</span></span>
<span data-ttu-id="ed015-103">Atualizar um dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="ed015-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="ed015-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed015-104">SYNTAX</span></span>

### <span data-ttu-id="ed015-105">ResourceSetForStatus (padrão)</span><span class="sxs-lookup"><span data-stu-id="ed015-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed015-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="ed015-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed015-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="ed015-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed015-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="ed015-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed015-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="ed015-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed015-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="ed015-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed015-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="ed015-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed015-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="ed015-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed015-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="ed015-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed015-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed015-114">DESCRIPTION</span></span>
<span data-ttu-id="ed015-115">Atualizar um dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="ed015-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="ed015-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed015-116">EXAMPLES</span></span>

### <span data-ttu-id="ed015-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed015-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="ed015-118">Ative os recursos de borda do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed015-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="ed015-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ed015-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="ed015-120">Desabilite o status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed015-120">Disable device status.</span></span>

### <span data-ttu-id="ed015-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ed015-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="ed015-122">Atualize o tipo de autorização de um dispositivo Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="ed015-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="ed015-123">OS</span><span class="sxs-lookup"><span data-stu-id="ed015-123">PARAMETERS</span></span>

### <span data-ttu-id="ed015-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="ed015-124">-AuthMethod</span></span>
<span data-ttu-id="ed015-125">O tipo de autorização com a qual uma entidade será criada.</span><span class="sxs-lookup"><span data-stu-id="ed015-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="ed015-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed015-126">-DefaultProfile</span></span>
<span data-ttu-id="ed015-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed015-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed015-128">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="ed015-128">-DeviceId</span></span>
<span data-ttu-id="ed015-129">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="ed015-129">Target Device Id.</span></span>

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

### <span data-ttu-id="ed015-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="ed015-130">-EdgeEnabled</span></span>
<span data-ttu-id="ed015-131">Sinalizador que indica a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="ed015-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="ed015-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed015-132">-InputObject</span></span>
<span data-ttu-id="ed015-133">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="ed015-133">IotHub object</span></span>

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

### <span data-ttu-id="ed015-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ed015-134">-IotHubName</span></span>
<span data-ttu-id="ed015-135">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="ed015-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ed015-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="ed015-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="ed015-137">Impressão digital de certificado autoassinado explícito para usar para a chave primária.</span><span class="sxs-lookup"><span data-stu-id="ed015-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="ed015-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed015-138">-ResourceGroupName</span></span>
<span data-ttu-id="ed015-139">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ed015-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ed015-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed015-140">-ResourceId</span></span>
<span data-ttu-id="ed015-141">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="ed015-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ed015-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="ed015-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="ed015-143">Impressão digital de certificado autoassinado explícito para usar para a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="ed015-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="ed015-144">-Status</span><span class="sxs-lookup"><span data-stu-id="ed015-144">-Status</span></span>
<span data-ttu-id="ed015-145">Definir o status do dispositivo durante a criação.</span><span class="sxs-lookup"><span data-stu-id="ed015-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="ed015-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="ed015-146">-StatusReason</span></span>
<span data-ttu-id="ed015-147">Descrição do status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed015-147">Description for device status.</span></span>

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

### <span data-ttu-id="ed015-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ed015-148">-Confirm</span></span>
<span data-ttu-id="ed015-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed015-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed015-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed015-150">-WhatIf</span></span>
<span data-ttu-id="ed015-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed015-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed015-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed015-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed015-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed015-153">CommonParameters</span></span>
<span data-ttu-id="ed015-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed015-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed015-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed015-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed015-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed015-156">INPUTS</span></span>

### <span data-ttu-id="ed015-157">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ed015-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ed015-158">System. String</span><span class="sxs-lookup"><span data-stu-id="ed015-158">System.String</span></span>

## <span data-ttu-id="ed015-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed015-159">OUTPUTS</span></span>

### <span data-ttu-id="ed015-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="ed015-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="ed015-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed015-161">NOTES</span></span>

## <span data-ttu-id="ed015-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed015-162">RELATED LINKS</span></span>
