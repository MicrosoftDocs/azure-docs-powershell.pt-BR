---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433746"
---
# <span data-ttu-id="76c69-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="76c69-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="76c69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76c69-102">SYNOPSIS</span></span>
<span data-ttu-id="76c69-103">Crie um dispositivo em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="76c69-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="76c69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76c69-104">SYNTAX</span></span>

### <span data-ttu-id="76c69-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="76c69-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76c69-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="76c69-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76c69-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="76c69-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76c69-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76c69-108">DESCRIPTION</span></span>
<span data-ttu-id="76c69-109">Crie um dispositivo com um tipo de autorização diferente em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="76c69-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="76c69-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76c69-110">EXAMPLES</span></span>

### <span data-ttu-id="76c69-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76c69-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="76c69-112">Crie um dispositivo IoT habilitado para borda com autorização padrão (chave privada compartilhada).</span><span class="sxs-lookup"><span data-stu-id="76c69-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="76c69-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="76c69-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="76c69-114">Crie um dispositivo IoT com a autorização da CA raiz com status desativado e motivo.</span><span class="sxs-lookup"><span data-stu-id="76c69-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="76c69-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="76c69-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="76c69-116">Crie um dispositivo IoT habilitado para borda e adicione dispositivos filho a ele.</span><span class="sxs-lookup"><span data-stu-id="76c69-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="76c69-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="76c69-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="76c69-118">Crie um dispositivo IoT e defina seu dispositivo pai.</span><span class="sxs-lookup"><span data-stu-id="76c69-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="76c69-119">OS</span><span class="sxs-lookup"><span data-stu-id="76c69-119">PARAMETERS</span></span>

### <span data-ttu-id="76c69-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="76c69-120">-AuthMethod</span></span>
<span data-ttu-id="76c69-121">O tipo de autorização com a qual uma entidade será criada.</span><span class="sxs-lookup"><span data-stu-id="76c69-121">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="76c69-122">-Filhos</span><span class="sxs-lookup"><span data-stu-id="76c69-122">-Children</span></span>
<span data-ttu-id="76c69-123">Adicionar lista de dispositivos filho (separados por vírgulas) inclui apenas dispositivos que não estão no Edge.</span><span class="sxs-lookup"><span data-stu-id="76c69-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="76c69-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c69-124">-DefaultProfile</span></span>
<span data-ttu-id="76c69-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76c69-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c69-126">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="76c69-126">-DeviceId</span></span>
<span data-ttu-id="76c69-127">ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="76c69-127">Target Device Id.</span></span>

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

### <span data-ttu-id="76c69-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="76c69-128">-EdgeEnabled</span></span>
<span data-ttu-id="76c69-129">Sinalizador que indica a habilitação de borda.</span><span class="sxs-lookup"><span data-stu-id="76c69-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="76c69-130">-Force</span><span class="sxs-lookup"><span data-stu-id="76c69-130">-Force</span></span>
<span data-ttu-id="76c69-131">Substitui o dispositivo pai do dispositivo não-Edge.</span><span class="sxs-lookup"><span data-stu-id="76c69-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="76c69-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76c69-132">-InputObject</span></span>
<span data-ttu-id="76c69-133">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="76c69-133">IotHub object</span></span>

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

### <span data-ttu-id="76c69-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="76c69-134">-IotHubName</span></span>
<span data-ttu-id="76c69-135">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="76c69-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="76c69-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="76c69-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="76c69-137">Impressão digital de certificado autoassinado explícito para usar para a chave primária.</span><span class="sxs-lookup"><span data-stu-id="76c69-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="76c69-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="76c69-138">-ParentDeviceId</span></span>
<span data-ttu-id="76c69-139">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="76c69-139">Id of edge device.</span></span>

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

### <span data-ttu-id="76c69-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c69-140">-ResourceGroupName</span></span>
<span data-ttu-id="76c69-141">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="76c69-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="76c69-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76c69-142">-ResourceId</span></span>
<span data-ttu-id="76c69-143">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="76c69-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="76c69-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="76c69-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="76c69-145">Impressão digital de certificado autoassinado explícito para usar para a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="76c69-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="76c69-146">-Status</span><span class="sxs-lookup"><span data-stu-id="76c69-146">-Status</span></span>
<span data-ttu-id="76c69-147">Definir o status do dispositivo durante a criação.</span><span class="sxs-lookup"><span data-stu-id="76c69-147">Set device status upon creation.</span></span>

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

### <span data-ttu-id="76c69-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="76c69-148">-StatusReason</span></span>
<span data-ttu-id="76c69-149">Descrição do status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76c69-149">Description for device status.</span></span>

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

### <span data-ttu-id="76c69-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="76c69-150">-Confirm</span></span>
<span data-ttu-id="76c69-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76c69-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c69-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c69-152">-WhatIf</span></span>
<span data-ttu-id="76c69-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76c69-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c69-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76c69-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c69-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c69-155">CommonParameters</span></span>
<span data-ttu-id="76c69-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c69-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c69-157">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c69-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c69-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76c69-158">INPUTS</span></span>

### <span data-ttu-id="76c69-159">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="76c69-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="76c69-160">System. String</span><span class="sxs-lookup"><span data-stu-id="76c69-160">System.String</span></span>

## <span data-ttu-id="76c69-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76c69-161">OUTPUTS</span></span>

### <span data-ttu-id="76c69-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="76c69-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="76c69-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76c69-163">NOTES</span></span>

## <span data-ttu-id="76c69-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76c69-164">RELATED LINKS</span></span>
