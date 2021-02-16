---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: f2244bc1d0471924ad7f69ff600e70e92fdc809a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118593"
---
# <span data-ttu-id="4a6dc-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="4a6dc-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="4a6dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6dc-103">Cria uma nova função para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="4a6dc-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="4a6dc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a6dc-104">SYNTAX</span></span>

### <span data-ttu-id="4a6dc-105">ConnectionStringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4a6dc-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a6dc-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a6dc-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a6dc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a6dc-107">DESCRIPTION</span></span>
<span data-ttu-id="4a6dc-108">O **cmdlet New-AzSt stackEdgeRole** cria uma nova função para um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="4a6dc-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4a6dc-109">EXAMPLES</span></span>

### <span data-ttu-id="4a6dc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a6dc-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="4a6dc-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a6dc-111">PARAMETERS</span></span>

### <span data-ttu-id="4a6dc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a6dc-112">-AsJob</span></span>
<span data-ttu-id="4a6dc-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4a6dc-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a6dc-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="4a6dc-114">-ConnectionString</span></span>
<span data-ttu-id="4a6dc-115">Para fornecer cadeias de conexão</span><span class="sxs-lookup"><span data-stu-id="4a6dc-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="4a6dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6dc-116">-DefaultProfile</span></span>
<span data-ttu-id="4a6dc-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a6dc-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4a6dc-118">-DeviceName</span></span>
<span data-ttu-id="4a6dc-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="4a6dc-119">Device Name</span></span>

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

### <span data-ttu-id="4a6dc-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="4a6dc-120">-DeviceProperty</span></span>
<span data-ttu-id="4a6dc-121">Para fornecer propriedades do dispositivo</span><span class="sxs-lookup"><span data-stu-id="4a6dc-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="4a6dc-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4a6dc-122">-EncryptionKey</span></span>
<span data-ttu-id="4a6dc-123">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="4a6dc-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="4a6dc-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="4a6dc-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="4a6dc-125">Iot Device Access Key</span><span class="sxs-lookup"><span data-stu-id="4a6dc-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="4a6dc-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="4a6dc-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="4a6dc-127">Forneça a cadeia de conexão do dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="4a6dc-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="4a6dc-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="4a6dc-128">-IotDeviceId</span></span>
<span data-ttu-id="4a6dc-129">ID do dispositivo Iot</span><span class="sxs-lookup"><span data-stu-id="4a6dc-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="4a6dc-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="4a6dc-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="4a6dc-131">Tecla de acesso do dispositivo Iot Edge</span><span class="sxs-lookup"><span data-stu-id="4a6dc-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="4a6dc-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="4a6dc-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="4a6dc-133">Forneça a cadeia de conexão do Dispositivo de Borda</span><span class="sxs-lookup"><span data-stu-id="4a6dc-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="4a6dc-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="4a6dc-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="4a6dc-135">ID do Dispositivo de Borda Iot</span><span class="sxs-lookup"><span data-stu-id="4a6dc-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="4a6dc-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="4a6dc-136">-IotHostHub</span></span>
<span data-ttu-id="4a6dc-137">Endereço do Hosthub</span><span class="sxs-lookup"><span data-stu-id="4a6dc-137">Hosthub address</span></span>

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

### <span data-ttu-id="4a6dc-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a6dc-138">-Name</span></span>
<span data-ttu-id="4a6dc-139">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="4a6dc-139">Resource Name</span></span>

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

### <span data-ttu-id="4a6dc-140">-Plataforma</span><span class="sxs-lookup"><span data-stu-id="4a6dc-140">-Platform</span></span>
<span data-ttu-id="4a6dc-141">Forneça a Plataforma, por exemplo: Linux</span><span class="sxs-lookup"><span data-stu-id="4a6dc-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="4a6dc-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a6dc-142">-ResourceGroupName</span></span>
<span data-ttu-id="4a6dc-143">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="4a6dc-143">Resource Group Name</span></span>

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

### <span data-ttu-id="4a6dc-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="4a6dc-144">-RoleStatus</span></span>
<span data-ttu-id="4a6dc-145">Fornecer o status de habilitar/desabilitar</span><span class="sxs-lookup"><span data-stu-id="4a6dc-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="4a6dc-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4a6dc-146">-Confirm</span></span>
<span data-ttu-id="4a6dc-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a6dc-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a6dc-148">-WhatIf</span></span>
<span data-ttu-id="4a6dc-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a6dc-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a6dc-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6dc-151">CommonParameters</span></span>
<span data-ttu-id="4a6dc-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a6dc-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6dc-153">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a6dc-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6dc-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="4a6dc-154">INPUTS</span></span>

### <span data-ttu-id="4a6dc-155">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4a6dc-155">None</span></span>

## <span data-ttu-id="4a6dc-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="4a6dc-156">OUTPUTS</span></span>

### <span data-ttu-id="4a6dc-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="4a6dc-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="4a6dc-158">Notas</span><span class="sxs-lookup"><span data-stu-id="4a6dc-158">NOTES</span></span>

## <span data-ttu-id="4a6dc-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a6dc-159">RELATED LINKS</span></span>
