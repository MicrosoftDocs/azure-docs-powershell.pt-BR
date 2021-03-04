---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: 0158116440ae7ffc1638ce08c6561e80ca034ae8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888713"
---
# <span data-ttu-id="5788e-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="5788e-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="5788e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5788e-102">SYNOPSIS</span></span>
<span data-ttu-id="5788e-103">Cria uma nova função para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="5788e-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="5788e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5788e-104">SYNTAX</span></span>

### <span data-ttu-id="5788e-105">ConnectionStringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5788e-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5788e-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="5788e-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5788e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5788e-107">DESCRIPTION</span></span>
<span data-ttu-id="5788e-108">O cmdlet **New-AzDataBoxEdgeRole** cria uma nova função para um dispositivo de Borda de Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="5788e-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="5788e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5788e-109">EXAMPLES</span></span>

### <span data-ttu-id="5788e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5788e-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="5788e-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5788e-111">PARAMETERS</span></span>

### <span data-ttu-id="5788e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5788e-112">-AsJob</span></span>
<span data-ttu-id="5788e-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5788e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5788e-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5788e-114">-ConnectionString</span></span>
<span data-ttu-id="5788e-115">Para fornecer cadeias de caracteres de conexão</span><span class="sxs-lookup"><span data-stu-id="5788e-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="5788e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5788e-116">-DefaultProfile</span></span>
<span data-ttu-id="5788e-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5788e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5788e-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5788e-118">-DeviceName</span></span>
<span data-ttu-id="5788e-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="5788e-119">Device Name</span></span>

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

### <span data-ttu-id="5788e-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="5788e-120">-DeviceProperty</span></span>
<span data-ttu-id="5788e-121">Para fornecer propriedades de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5788e-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="5788e-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5788e-122">-EncryptionKey</span></span>
<span data-ttu-id="5788e-123">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="5788e-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="5788e-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="5788e-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="5788e-125">Iot Device Access Key</span><span class="sxs-lookup"><span data-stu-id="5788e-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="5788e-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="5788e-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="5788e-127">Forneça cadeia de conexão do dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="5788e-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="5788e-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="5788e-128">-IotDeviceId</span></span>
<span data-ttu-id="5788e-129">ID do dispositivo Iot</span><span class="sxs-lookup"><span data-stu-id="5788e-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="5788e-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="5788e-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="5788e-131">Chave de acesso do dispositivo de Borda de Iot</span><span class="sxs-lookup"><span data-stu-id="5788e-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="5788e-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="5788e-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="5788e-133">Forneça cadeia de conexão do Dispositivo de Borda</span><span class="sxs-lookup"><span data-stu-id="5788e-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="5788e-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="5788e-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="5788e-135">ID do Dispositivo de Borda de Iot</span><span class="sxs-lookup"><span data-stu-id="5788e-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="5788e-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="5788e-136">-IotHostHub</span></span>
<span data-ttu-id="5788e-137">Endereço hosthub</span><span class="sxs-lookup"><span data-stu-id="5788e-137">Hosthub address</span></span>

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

### <span data-ttu-id="5788e-138">-Name</span><span class="sxs-lookup"><span data-stu-id="5788e-138">-Name</span></span>
<span data-ttu-id="5788e-139">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="5788e-139">Resource Name</span></span>

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

### <span data-ttu-id="5788e-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="5788e-140">-Platform</span></span>
<span data-ttu-id="5788e-141">Forneça a Plataforma, para ex: Linux</span><span class="sxs-lookup"><span data-stu-id="5788e-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="5788e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5788e-142">-ResourceGroupName</span></span>
<span data-ttu-id="5788e-143">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5788e-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5788e-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="5788e-144">-RoleStatus</span></span>
<span data-ttu-id="5788e-145">Fornecer o status enable/disable</span><span class="sxs-lookup"><span data-stu-id="5788e-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="5788e-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5788e-146">-Confirm</span></span>
<span data-ttu-id="5788e-147">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5788e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5788e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5788e-148">-WhatIf</span></span>
<span data-ttu-id="5788e-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5788e-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5788e-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5788e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5788e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5788e-151">CommonParameters</span></span>
<span data-ttu-id="5788e-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5788e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5788e-153">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5788e-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5788e-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5788e-154">INPUTS</span></span>

### <span data-ttu-id="5788e-155">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5788e-155">None</span></span>

## <span data-ttu-id="5788e-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5788e-156">OUTPUTS</span></span>

### <span data-ttu-id="5788e-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="5788e-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="5788e-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="5788e-158">NOTES</span></span>

## <span data-ttu-id="5788e-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5788e-159">RELATED LINKS</span></span>
