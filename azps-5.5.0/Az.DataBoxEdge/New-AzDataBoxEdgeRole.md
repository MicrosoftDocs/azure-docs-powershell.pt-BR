---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117760"
---
# <span data-ttu-id="20689-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="20689-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="20689-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20689-102">SYNOPSIS</span></span>
<span data-ttu-id="20689-103">Cria uma nova função para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="20689-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="20689-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20689-104">SYNTAX</span></span>

### <span data-ttu-id="20689-105">ConnectionStringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="20689-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20689-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="20689-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20689-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="20689-107">DESCRIPTION</span></span>
<span data-ttu-id="20689-108">O cmdlet **New-AzDataBoxEdgeRole** cria uma nova função para um dispositivo de borda de caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="20689-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="20689-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20689-109">EXAMPLES</span></span>

### <span data-ttu-id="20689-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20689-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="20689-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20689-111">PARAMETERS</span></span>

### <span data-ttu-id="20689-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20689-112">-AsJob</span></span>
<span data-ttu-id="20689-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="20689-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20689-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="20689-114">-ConnectionString</span></span>
<span data-ttu-id="20689-115">Para fornecer cadeias de conexão</span><span class="sxs-lookup"><span data-stu-id="20689-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="20689-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20689-116">-DefaultProfile</span></span>
<span data-ttu-id="20689-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20689-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20689-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="20689-118">-DeviceName</span></span>
<span data-ttu-id="20689-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="20689-119">Device Name</span></span>

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

### <span data-ttu-id="20689-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="20689-120">-DeviceProperty</span></span>
<span data-ttu-id="20689-121">Para fornecer propriedades do dispositivo</span><span class="sxs-lookup"><span data-stu-id="20689-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="20689-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="20689-122">-EncryptionKey</span></span>
<span data-ttu-id="20689-123">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="20689-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="20689-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="20689-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="20689-125">Iot Device Access Key</span><span class="sxs-lookup"><span data-stu-id="20689-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="20689-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="20689-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="20689-127">Forneça a cadeia de conexão do dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="20689-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="20689-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="20689-128">-IotDeviceId</span></span>
<span data-ttu-id="20689-129">ID do dispositivo Iot</span><span class="sxs-lookup"><span data-stu-id="20689-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="20689-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="20689-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="20689-131">Tecla de acesso do dispositivo Iot Edge</span><span class="sxs-lookup"><span data-stu-id="20689-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="20689-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="20689-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="20689-133">Forneça a cadeia de conexão do Dispositivo de Borda</span><span class="sxs-lookup"><span data-stu-id="20689-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="20689-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="20689-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="20689-135">ID do Dispositivo de Borda Iot</span><span class="sxs-lookup"><span data-stu-id="20689-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="20689-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="20689-136">-IotHostHub</span></span>
<span data-ttu-id="20689-137">Endereço do Hosthub</span><span class="sxs-lookup"><span data-stu-id="20689-137">Hosthub address</span></span>

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

### <span data-ttu-id="20689-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="20689-138">-Name</span></span>
<span data-ttu-id="20689-139">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="20689-139">Resource Name</span></span>

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

### <span data-ttu-id="20689-140">-Plataforma</span><span class="sxs-lookup"><span data-stu-id="20689-140">-Platform</span></span>
<span data-ttu-id="20689-141">Forneça a Plataforma, por exemplo: Linux</span><span class="sxs-lookup"><span data-stu-id="20689-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="20689-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20689-142">-ResourceGroupName</span></span>
<span data-ttu-id="20689-143">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="20689-143">Resource Group Name</span></span>

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

### <span data-ttu-id="20689-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="20689-144">-RoleStatus</span></span>
<span data-ttu-id="20689-145">Fornecer o status habilitar/desabilitar</span><span class="sxs-lookup"><span data-stu-id="20689-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="20689-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="20689-146">-Confirm</span></span>
<span data-ttu-id="20689-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20689-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20689-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20689-148">-WhatIf</span></span>
<span data-ttu-id="20689-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="20689-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20689-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20689-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20689-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20689-151">CommonParameters</span></span>
<span data-ttu-id="20689-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20689-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20689-153">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20689-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20689-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="20689-154">INPUTS</span></span>

### <span data-ttu-id="20689-155">Nenhum</span><span class="sxs-lookup"><span data-stu-id="20689-155">None</span></span>

## <span data-ttu-id="20689-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="20689-156">OUTPUTS</span></span>

### <span data-ttu-id="20689-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="20689-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="20689-158">Notas</span><span class="sxs-lookup"><span data-stu-id="20689-158">NOTES</span></span>

## <span data-ttu-id="20689-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20689-159">RELATED LINKS</span></span>
