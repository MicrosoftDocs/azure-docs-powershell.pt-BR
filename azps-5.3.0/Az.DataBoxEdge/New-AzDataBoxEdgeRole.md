---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429952"
---
# <span data-ttu-id="513fb-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="513fb-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="513fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="513fb-102">SYNOPSIS</span></span>
<span data-ttu-id="513fb-103">Cria uma nova função para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="513fb-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="513fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="513fb-104">SYNTAX</span></span>

### <span data-ttu-id="513fb-105">ConnectionStringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="513fb-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="513fb-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="513fb-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="513fb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="513fb-107">DESCRIPTION</span></span>
<span data-ttu-id="513fb-108">O cmdlet **New-AzDataBoxEdgeRole** cria uma nova função para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="513fb-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="513fb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="513fb-109">EXAMPLES</span></span>

### <span data-ttu-id="513fb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="513fb-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="513fb-111">OS</span><span class="sxs-lookup"><span data-stu-id="513fb-111">PARAMETERS</span></span>

### <span data-ttu-id="513fb-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="513fb-112">-AsJob</span></span>
<span data-ttu-id="513fb-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="513fb-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="513fb-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="513fb-114">-ConnectionString</span></span>
<span data-ttu-id="513fb-115">Para fornecer cadeias de conexão</span><span class="sxs-lookup"><span data-stu-id="513fb-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="513fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513fb-116">-DefaultProfile</span></span>
<span data-ttu-id="513fb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="513fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="513fb-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="513fb-118">-DeviceName</span></span>
<span data-ttu-id="513fb-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="513fb-119">Device Name</span></span>

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

### <span data-ttu-id="513fb-120">-Deviceproperty</span><span class="sxs-lookup"><span data-stu-id="513fb-120">-DeviceProperty</span></span>
<span data-ttu-id="513fb-121">Para fornecer propriedades de dispositivo</span><span class="sxs-lookup"><span data-stu-id="513fb-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="513fb-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="513fb-122">-EncryptionKey</span></span>
<span data-ttu-id="513fb-123">Chave de criptografia do dispositivo de borda</span><span class="sxs-lookup"><span data-stu-id="513fb-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="513fb-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="513fb-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="513fb-125">Chave de acesso a dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="513fb-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="513fb-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="513fb-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="513fb-127">Forneça uma cadeia de conexão de dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="513fb-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="513fb-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="513fb-128">-IotDeviceId</span></span>
<span data-ttu-id="513fb-129">ID do dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="513fb-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="513fb-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="513fb-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="513fb-131">Chave de acesso do dispositivo de borda IOT</span><span class="sxs-lookup"><span data-stu-id="513fb-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="513fb-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="513fb-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="513fb-133">Forneça uma cadeia de conexão de dispositivo de borda</span><span class="sxs-lookup"><span data-stu-id="513fb-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="513fb-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="513fb-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="513fb-135">ID do dispositivo de borda IOT</span><span class="sxs-lookup"><span data-stu-id="513fb-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="513fb-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="513fb-136">-IotHostHub</span></span>
<span data-ttu-id="513fb-137">Endereço de Hosthub</span><span class="sxs-lookup"><span data-stu-id="513fb-137">Hosthub address</span></span>

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

### <span data-ttu-id="513fb-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="513fb-138">-Name</span></span>
<span data-ttu-id="513fb-139">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="513fb-139">Resource Name</span></span>

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

### <span data-ttu-id="513fb-140">-Plataforma</span><span class="sxs-lookup"><span data-stu-id="513fb-140">-Platform</span></span>
<span data-ttu-id="513fb-141">Fornecer a plataforma, por exemplo: Linux</span><span class="sxs-lookup"><span data-stu-id="513fb-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="513fb-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="513fb-142">-ResourceGroupName</span></span>
<span data-ttu-id="513fb-143">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="513fb-143">Resource Group Name</span></span>

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

### <span data-ttu-id="513fb-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="513fb-144">-RoleStatus</span></span>
<span data-ttu-id="513fb-145">Fornecer o status habilitar/desabilitar</span><span class="sxs-lookup"><span data-stu-id="513fb-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="513fb-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="513fb-146">-Confirm</span></span>
<span data-ttu-id="513fb-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="513fb-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="513fb-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="513fb-148">-WhatIf</span></span>
<span data-ttu-id="513fb-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="513fb-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="513fb-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="513fb-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="513fb-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513fb-151">CommonParameters</span></span>
<span data-ttu-id="513fb-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="513fb-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513fb-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="513fb-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513fb-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="513fb-154">INPUTS</span></span>

### <span data-ttu-id="513fb-155">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="513fb-155">None</span></span>

## <span data-ttu-id="513fb-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="513fb-156">OUTPUTS</span></span>

### <span data-ttu-id="513fb-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="513fb-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="513fb-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="513fb-158">NOTES</span></span>

## <span data-ttu-id="513fb-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="513fb-159">RELATED LINKS</span></span>
