---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 269d333c9b74ed0e3e959ef609531bcea41b724c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258353"
---
# <span data-ttu-id="b022b-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b022b-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="b022b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b022b-102">SYNOPSIS</span></span>
<span data-ttu-id="b022b-103">Criar ou atualizar o grupo de segurança de dispositivos</span><span class="sxs-lookup"><span data-stu-id="b022b-103">Create or update device security group</span></span>

## <span data-ttu-id="b022b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b022b-104">SYNTAX</span></span>

### <span data-ttu-id="b022b-105">ResourceIdLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="b022b-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b022b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b022b-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b022b-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="b022b-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b022b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b022b-108">DESCRIPTION</span></span>
<span data-ttu-id="b022b-109">O cmdlet Set-AzDeviceSecurityGroup cria ou atualiza um grupo de segurança de dispositivo definido na solução de segurança IOT.</span><span class="sxs-lookup"><span data-stu-id="b022b-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="b022b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b022b-110">EXAMPLES</span></span>

### <span data-ttu-id="b022b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b022b-111">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> $TimeWindowRule = New-AzDeviceSecurityGroupTimeWindowRuleObject -Type "ActiveConnectionsNotInAllowedRange" -Enabled $true 
-MaxThreshold 30 -MinThreshold 0 -TimeWindowSize $TimeWindowSize
PS C:\> Set-AzDeviceSecurityGroup -Name "MySecurityGroup" 
-HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 
-TimeWindowRule $TimeWindowRules

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: true
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT5M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="b022b-112">Atualize o grupo de segurança do dispositivo existente do Hub IoT "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" com o tipo de regra "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="b022b-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="b022b-113">OS</span><span class="sxs-lookup"><span data-stu-id="b022b-113">PARAMETERS</span></span>

### <span data-ttu-id="b022b-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="b022b-114">-AllowlistRule</span></span>
<span data-ttu-id="b022b-115">Permitir regras de lista.</span><span class="sxs-lookup"><span data-stu-id="b022b-115">Allow list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b022b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b022b-116">-DefaultProfile</span></span>
<span data-ttu-id="b022b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b022b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b022b-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="b022b-118">-DenylistRule</span></span>
<span data-ttu-id="b022b-119">Negar regras de lista.</span><span class="sxs-lookup"><span data-stu-id="b022b-119">Deny list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b022b-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="b022b-120">-HubResourceId</span></span>
<span data-ttu-id="b022b-121">ID do recurso do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="b022b-121">IoT Hub resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b022b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b022b-122">-InputObject</span></span>
<span data-ttu-id="b022b-123">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="b022b-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b022b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b022b-124">-Name</span></span>
<span data-ttu-id="b022b-125">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b022b-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b022b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b022b-126">-ResourceId</span></span>
<span data-ttu-id="b022b-127">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="b022b-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b022b-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="b022b-128">-ThresholdRule</span></span>
<span data-ttu-id="b022b-129">Regras de limite.</span><span class="sxs-lookup"><span data-stu-id="b022b-129">Threshold rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b022b-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="b022b-130">-TimeWindowRule</span></span>
<span data-ttu-id="b022b-131">Regras de janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="b022b-131">Time window rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b022b-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b022b-132">-Confirm</span></span>
<span data-ttu-id="b022b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b022b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b022b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b022b-134">-WhatIf</span></span>
<span data-ttu-id="b022b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b022b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b022b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b022b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b022b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b022b-137">CommonParameters</span></span>
<span data-ttu-id="b022b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b022b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b022b-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b022b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b022b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b022b-140">INPUTS</span></span>

### <span data-ttu-id="b022b-141">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSThresholdCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="b022b-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="b022b-142">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="b022b-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="b022b-143">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSAllowlistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="b022b-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="b022b-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="b022b-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="b022b-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b022b-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="b022b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b022b-146">System.String</span></span>

## <span data-ttu-id="b022b-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b022b-147">OUTPUTS</span></span>

### <span data-ttu-id="b022b-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b022b-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="b022b-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b022b-149">NOTES</span></span>

## <span data-ttu-id="b022b-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b022b-150">RELATED LINKS</span></span>
