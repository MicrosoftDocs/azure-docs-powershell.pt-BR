---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: 785c092333d0e083ed3ee356a0c4e76d6188b96b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892310"
---
# <span data-ttu-id="365e5-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="365e5-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="365e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="365e5-102">SYNOPSIS</span></span>
<span data-ttu-id="365e5-103">Cria uma nova função para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="365e5-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="365e5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="365e5-104">SYNTAX</span></span>

### <span data-ttu-id="365e5-105">ConnectionStringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="365e5-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="365e5-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="365e5-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="365e5-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="365e5-107">DESCRIPTION</span></span>
<span data-ttu-id="365e5-108">O cmdlet **New-AzStackEdgeRole** cria uma nova função para um dispositivo de Borda de Pilha.</span><span class="sxs-lookup"><span data-stu-id="365e5-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="365e5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="365e5-109">EXAMPLES</span></span>

### <span data-ttu-id="365e5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="365e5-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="365e5-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="365e5-111">PARAMETERS</span></span>

### <span data-ttu-id="365e5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="365e5-112">-AsJob</span></span>
<span data-ttu-id="365e5-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="365e5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="365e5-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="365e5-114">-ConnectionString</span></span>
<span data-ttu-id="365e5-115">Para fornecer cadeias de caracteres de conexão</span><span class="sxs-lookup"><span data-stu-id="365e5-115">To Provide Connection Strings</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365e5-116">-DefaultProfile</span></span>
<span data-ttu-id="365e5-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="365e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="365e5-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="365e5-118">-DeviceName</span></span>
<span data-ttu-id="365e5-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="365e5-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="365e5-120">-DeviceProperty</span></span>
<span data-ttu-id="365e5-121">Para fornecer propriedades de dispositivo</span><span class="sxs-lookup"><span data-stu-id="365e5-121">To Provide Device Properties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IotParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="365e5-122">-EncryptionKey</span></span>
<span data-ttu-id="365e5-123">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="365e5-123">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="365e5-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="365e5-125">Iot Device Access Key</span><span class="sxs-lookup"><span data-stu-id="365e5-125">Iot Device Access Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="365e5-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="365e5-127">Forneça cadeia de conexão do dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="365e5-127">Please provide connection string of IOT Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="365e5-128">-IotDeviceId</span></span>
<span data-ttu-id="365e5-129">ID do dispositivo Iot</span><span class="sxs-lookup"><span data-stu-id="365e5-129">Device Id of the Iot Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="365e5-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="365e5-131">Chave de acesso do dispositivo de Borda de Iot</span><span class="sxs-lookup"><span data-stu-id="365e5-131">Access key of the Iot Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="365e5-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="365e5-133">Forneça cadeia de conexão do Dispositivo de Borda</span><span class="sxs-lookup"><span data-stu-id="365e5-133">Please provide connection string of Edge Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="365e5-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="365e5-135">ID do Dispositivo de Borda de Iot</span><span class="sxs-lookup"><span data-stu-id="365e5-135">Id of the Iot Edge Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="365e5-136">-IotHostHub</span></span>
<span data-ttu-id="365e5-137">Endereço hosthub</span><span class="sxs-lookup"><span data-stu-id="365e5-137">Hosthub address</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-138">-Name</span><span class="sxs-lookup"><span data-stu-id="365e5-138">-Name</span></span>
<span data-ttu-id="365e5-139">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="365e5-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="365e5-140">-Platform</span></span>
<span data-ttu-id="365e5-141">Forneça a Plataforma, para ex: Linux</span><span class="sxs-lookup"><span data-stu-id="365e5-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="365e5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="365e5-142">-ResourceGroupName</span></span>
<span data-ttu-id="365e5-143">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="365e5-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365e5-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="365e5-144">-RoleStatus</span></span>
<span data-ttu-id="365e5-145">Fornecer o status enable/disable</span><span class="sxs-lookup"><span data-stu-id="365e5-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="365e5-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="365e5-146">-Confirm</span></span>
<span data-ttu-id="365e5-147">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="365e5-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="365e5-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="365e5-148">-WhatIf</span></span>
<span data-ttu-id="365e5-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="365e5-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="365e5-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="365e5-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="365e5-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365e5-151">CommonParameters</span></span>
<span data-ttu-id="365e5-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="365e5-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365e5-153">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="365e5-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365e5-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="365e5-154">INPUTS</span></span>

### <span data-ttu-id="365e5-155">Nenhum</span><span class="sxs-lookup"><span data-stu-id="365e5-155">None</span></span>

## <span data-ttu-id="365e5-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="365e5-156">OUTPUTS</span></span>

### <span data-ttu-id="365e5-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="365e5-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="365e5-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="365e5-158">NOTES</span></span>

## <span data-ttu-id="365e5-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="365e5-159">RELATED LINKS</span></span>
