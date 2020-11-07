---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: f2244bc1d0471924ad7f69ff600e70e92fdc809a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956161"
---
# <span data-ttu-id="c9f8a-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="c9f8a-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="c9f8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f8a-103">Cria uma nova função para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="c9f8a-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="c9f8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9f8a-104">SYNTAX</span></span>

### <span data-ttu-id="c9f8a-105">ConnectionStringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c9f8a-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f8a-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9f8a-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9f8a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9f8a-107">DESCRIPTION</span></span>
<span data-ttu-id="c9f8a-108">O cmdlet **New-AzStackEdgeRole** cria uma nova função para um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="c9f8a-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="c9f8a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9f8a-109">EXAMPLES</span></span>

### <span data-ttu-id="c9f8a-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c9f8a-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="c9f8a-111">OS</span><span class="sxs-lookup"><span data-stu-id="c9f8a-111">PARAMETERS</span></span>

### <span data-ttu-id="c9f8a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9f8a-112">-AsJob</span></span>
<span data-ttu-id="c9f8a-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c9f8a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9f8a-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c9f8a-114">-ConnectionString</span></span>
<span data-ttu-id="c9f8a-115">Para fornecer cadeias de conexão</span><span class="sxs-lookup"><span data-stu-id="c9f8a-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="c9f8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f8a-116">-DefaultProfile</span></span>
<span data-ttu-id="c9f8a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f8a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9f8a-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c9f8a-118">-DeviceName</span></span>
<span data-ttu-id="c9f8a-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c9f8a-119">Device Name</span></span>

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

### <span data-ttu-id="c9f8a-120">-Deviceproperty</span><span class="sxs-lookup"><span data-stu-id="c9f8a-120">-DeviceProperty</span></span>
<span data-ttu-id="c9f8a-121">Para fornecer propriedades de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c9f8a-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="c9f8a-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c9f8a-122">-EncryptionKey</span></span>
<span data-ttu-id="c9f8a-123">Chave de criptografia do dispositivo de borda</span><span class="sxs-lookup"><span data-stu-id="c9f8a-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="c9f8a-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="c9f8a-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="c9f8a-125">Chave de acesso a dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="c9f8a-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="c9f8a-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="c9f8a-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="c9f8a-127">Forneça uma cadeia de conexão de dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="c9f8a-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="c9f8a-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="c9f8a-128">-IotDeviceId</span></span>
<span data-ttu-id="c9f8a-129">ID do dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="c9f8a-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="c9f8a-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="c9f8a-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="c9f8a-131">Chave de acesso do dispositivo de borda IOT</span><span class="sxs-lookup"><span data-stu-id="c9f8a-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="c9f8a-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="c9f8a-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="c9f8a-133">Forneça uma cadeia de conexão de dispositivo de borda</span><span class="sxs-lookup"><span data-stu-id="c9f8a-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="c9f8a-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="c9f8a-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="c9f8a-135">ID do dispositivo de borda IOT</span><span class="sxs-lookup"><span data-stu-id="c9f8a-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="c9f8a-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="c9f8a-136">-IotHostHub</span></span>
<span data-ttu-id="c9f8a-137">Endereço de Hosthub</span><span class="sxs-lookup"><span data-stu-id="c9f8a-137">Hosthub address</span></span>

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

### <span data-ttu-id="c9f8a-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9f8a-138">-Name</span></span>
<span data-ttu-id="c9f8a-139">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="c9f8a-139">Resource Name</span></span>

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

### <span data-ttu-id="c9f8a-140">-Plataforma</span><span class="sxs-lookup"><span data-stu-id="c9f8a-140">-Platform</span></span>
<span data-ttu-id="c9f8a-141">Fornecer a plataforma, por exemplo: Linux</span><span class="sxs-lookup"><span data-stu-id="c9f8a-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="c9f8a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f8a-142">-ResourceGroupName</span></span>
<span data-ttu-id="c9f8a-143">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c9f8a-143">Resource Group Name</span></span>

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

### <span data-ttu-id="c9f8a-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="c9f8a-144">-RoleStatus</span></span>
<span data-ttu-id="c9f8a-145">Fornecer o status habilitar/desabilitar</span><span class="sxs-lookup"><span data-stu-id="c9f8a-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="c9f8a-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c9f8a-146">-Confirm</span></span>
<span data-ttu-id="c9f8a-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9f8a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f8a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f8a-148">-WhatIf</span></span>
<span data-ttu-id="c9f8a-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c9f8a-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9f8a-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9f8a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f8a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f8a-151">CommonParameters</span></span>
<span data-ttu-id="c9f8a-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9f8a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f8a-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9f8a-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f8a-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9f8a-154">INPUTS</span></span>

### <span data-ttu-id="c9f8a-155">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c9f8a-155">None</span></span>

## <span data-ttu-id="c9f8a-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9f8a-156">OUTPUTS</span></span>

### <span data-ttu-id="c9f8a-157">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="c9f8a-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="c9f8a-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9f8a-158">NOTES</span></span>

## <span data-ttu-id="c9f8a-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9f8a-159">RELATED LINKS</span></span>
