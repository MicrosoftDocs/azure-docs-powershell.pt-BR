---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 52fae225184b83675f21af941fa125576252ffbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901437"
---
# <span data-ttu-id="44c7e-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="44c7e-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="44c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="44c7e-103">Obter grupo de segurança de dispositivos (segurança do Hub IoT)</span><span class="sxs-lookup"><span data-stu-id="44c7e-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="44c7e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="44c7e-104">SYNTAX</span></span>

### <span data-ttu-id="44c7e-105">ResourceIdScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="44c7e-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44c7e-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="44c7e-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44c7e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="44c7e-107">DESCRIPTION</span></span>
<span data-ttu-id="44c7e-108">O Get-AzDeviceSecurityGroup cmdlet retorna um grupo de segurança de dispositivo definido na solução de segurança iot</span><span class="sxs-lookup"><span data-stu-id="44c7e-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="44c7e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44c7e-109">EXAMPLES</span></span>

### <span data-ttu-id="44c7e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44c7e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" -Name "MySecurityGroup" 

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }
            {
              RuleType: "AmqpC2DMessagesNotInAllowedRange"
              DisplayName: "Number of cloud to device messages (AMQP protocol) is not in allowed range"
              Description: "Get an alert when the number of cloud to device messages (AMQP protocol) in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
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

<span data-ttu-id="44c7e-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="44c7e-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="44c7e-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="44c7e-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="44c7e-113">Obter lista do grupo de segurança de dispositivos no Hub IoT com id de reasource "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="44c7e-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="44c7e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="44c7e-114">PARAMETERS</span></span>

### <span data-ttu-id="44c7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c7e-115">-DefaultProfile</span></span>
<span data-ttu-id="44c7e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44c7e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44c7e-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="44c7e-117">-HubResourceId</span></span>
<span data-ttu-id="44c7e-118">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="44c7e-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="44c7e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="44c7e-119">-Name</span></span>
<span data-ttu-id="44c7e-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="44c7e-120">Resource name.</span></span>

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

### <span data-ttu-id="44c7e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c7e-121">CommonParameters</span></span>
<span data-ttu-id="44c7e-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c7e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c7e-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44c7e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c7e-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44c7e-124">INPUTS</span></span>

### <span data-ttu-id="44c7e-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="44c7e-125">None</span></span>

## <span data-ttu-id="44c7e-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="44c7e-126">OUTPUTS</span></span>

### <span data-ttu-id="44c7e-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="44c7e-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="44c7e-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="44c7e-128">NOTES</span></span>

## <span data-ttu-id="44c7e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44c7e-129">RELATED LINKS</span></span>
