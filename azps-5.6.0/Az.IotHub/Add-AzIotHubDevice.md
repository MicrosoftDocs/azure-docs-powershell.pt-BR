---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: 0f2e7cd2abc61cde9f060eaabf6634385b6ec258
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891367"
---
# <span data-ttu-id="dbd43-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="dbd43-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="dbd43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbd43-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd43-103">Crie um dispositivo em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="dbd43-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="dbd43-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dbd43-104">SYNTAX</span></span>

### <span data-ttu-id="dbd43-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dbd43-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbd43-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dbd43-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbd43-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dbd43-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbd43-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dbd43-108">DESCRIPTION</span></span>
<span data-ttu-id="dbd43-109">Crie um dispositivo com tipo de autorização diferente em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="dbd43-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="dbd43-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbd43-110">EXAMPLES</span></span>

### <span data-ttu-id="dbd43-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dbd43-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="dbd43-112">Crie um dispositivo IoT habilitado para borda com autorização padrão (chave privada compartilhada).</span><span class="sxs-lookup"><span data-stu-id="dbd43-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="dbd43-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dbd43-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="dbd43-114">Crie um dispositivo IoT com autorização de AC raiz com status e motivo desabilitados.</span><span class="sxs-lookup"><span data-stu-id="dbd43-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="dbd43-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="dbd43-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="dbd43-116">Crie um dispositivo IoT habilitado para borda e adicione dispositivos filho a ele.</span><span class="sxs-lookup"><span data-stu-id="dbd43-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="dbd43-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="dbd43-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="dbd43-118">Criar um dispositivo IoT e definir seu dispositivo pai.</span><span class="sxs-lookup"><span data-stu-id="dbd43-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="dbd43-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dbd43-119">PARAMETERS</span></span>

### <span data-ttu-id="dbd43-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="dbd43-120">-AuthMethod</span></span>
<span data-ttu-id="dbd43-121">O tipo de autorização com o qual uma entidade deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="dbd43-121">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="dbd43-122">-Children</span><span class="sxs-lookup"><span data-stu-id="dbd43-122">-Children</span></span>
<span data-ttu-id="dbd43-123">Adicionar lista de dispositivos filho (vírgula separada) inclui apenas dispositivos que não são de borda.</span><span class="sxs-lookup"><span data-stu-id="dbd43-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd43-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd43-124">-DefaultProfile</span></span>
<span data-ttu-id="dbd43-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd43-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbd43-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="dbd43-126">-DeviceId</span></span>
<span data-ttu-id="dbd43-127">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="dbd43-127">Target Device Id.</span></span>

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

### <span data-ttu-id="dbd43-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="dbd43-128">-EdgeEnabled</span></span>
<span data-ttu-id="dbd43-129">Sinalizador indicando a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="dbd43-129">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd43-130">-Force</span><span class="sxs-lookup"><span data-stu-id="dbd43-130">-Force</span></span>
<span data-ttu-id="dbd43-131">Substitui o dispositivo pai do dispositivo sem borda.</span><span class="sxs-lookup"><span data-stu-id="dbd43-131">Overwrites the non-edge device's parent device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd43-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbd43-132">-InputObject</span></span>
<span data-ttu-id="dbd43-133">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="dbd43-133">IotHub object</span></span>

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

### <span data-ttu-id="dbd43-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="dbd43-134">-IotHubName</span></span>
<span data-ttu-id="dbd43-135">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="dbd43-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dbd43-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="dbd43-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="dbd43-137">Impressão digital explícita de certificado auto-assinado a ser usada para chave primária.</span><span class="sxs-lookup"><span data-stu-id="dbd43-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="dbd43-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="dbd43-138">-ParentDeviceId</span></span>
<span data-ttu-id="dbd43-139">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="dbd43-139">Id of edge device.</span></span>

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

### <span data-ttu-id="dbd43-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbd43-140">-ResourceGroupName</span></span>
<span data-ttu-id="dbd43-141">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="dbd43-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dbd43-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbd43-142">-ResourceId</span></span>
<span data-ttu-id="dbd43-143">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="dbd43-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dbd43-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="dbd43-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="dbd43-145">Impressão digital explícita de certificado auto-assinado a ser usada para chave secundária.</span><span class="sxs-lookup"><span data-stu-id="dbd43-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="dbd43-146">-Status</span><span class="sxs-lookup"><span data-stu-id="dbd43-146">-Status</span></span>
<span data-ttu-id="dbd43-147">Definir o status do dispositivo após a criação.</span><span class="sxs-lookup"><span data-stu-id="dbd43-147">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd43-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="dbd43-148">-StatusReason</span></span>
<span data-ttu-id="dbd43-149">Descrição do status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbd43-149">Description for device status.</span></span>

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

### <span data-ttu-id="dbd43-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbd43-150">-Confirm</span></span>
<span data-ttu-id="dbd43-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd43-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbd43-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbd43-152">-WhatIf</span></span>
<span data-ttu-id="dbd43-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dbd43-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbd43-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dbd43-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbd43-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd43-155">CommonParameters</span></span>
<span data-ttu-id="dbd43-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd43-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd43-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd43-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd43-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbd43-158">INPUTS</span></span>

### <span data-ttu-id="dbd43-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dbd43-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dbd43-160">System.String</span><span class="sxs-lookup"><span data-stu-id="dbd43-160">System.String</span></span>

## <span data-ttu-id="dbd43-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dbd43-161">OUTPUTS</span></span>

### <span data-ttu-id="dbd43-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="dbd43-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="dbd43-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="dbd43-163">NOTES</span></span>

## <span data-ttu-id="dbd43-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbd43-164">RELATED LINKS</span></span>
