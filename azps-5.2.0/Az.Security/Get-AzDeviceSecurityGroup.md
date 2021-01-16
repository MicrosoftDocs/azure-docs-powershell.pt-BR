---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258962"
---
# <span data-ttu-id="b4751-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b4751-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="b4751-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4751-102">SYNOPSIS</span></span>
<span data-ttu-id="b4751-103">Obter grupo de segurança de dispositivo (segurança de Hub IoT)</span><span class="sxs-lookup"><span data-stu-id="b4751-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="b4751-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4751-104">SYNTAX</span></span>

### <span data-ttu-id="b4751-105">ResourceIdScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="b4751-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4751-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="b4751-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4751-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4751-107">DESCRIPTION</span></span>
<span data-ttu-id="b4751-108">O cmdlet Get-AzDeviceSecurityGroup retorna um grupo de segurança de dispositivo definido na solução de segurança IOT</span><span class="sxs-lookup"><span data-stu-id="b4751-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="b4751-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4751-109">EXAMPLES</span></span>

### <span data-ttu-id="b4751-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4751-110">Example 1</span></span>
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

<span data-ttu-id="b4751-111">Obter o grupo de segurança do dispositivo "mysecurity Group" no Hub IoT com ID reasource "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="b4751-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="b4751-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b4751-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="b4751-113">Obter a lista de grupos de segurança de dispositivos no Hub IoT com ID de reasource "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="b4751-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="b4751-114">OS</span><span class="sxs-lookup"><span data-stu-id="b4751-114">PARAMETERS</span></span>

### <span data-ttu-id="b4751-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4751-115">-DefaultProfile</span></span>
<span data-ttu-id="b4751-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4751-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4751-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="b4751-117">-HubResourceId</span></span>
<span data-ttu-id="b4751-118">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="b4751-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="b4751-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4751-119">-Name</span></span>
<span data-ttu-id="b4751-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b4751-120">Resource name.</span></span>

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

### <span data-ttu-id="b4751-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4751-121">CommonParameters</span></span>
<span data-ttu-id="b4751-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4751-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4751-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4751-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4751-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4751-124">INPUTS</span></span>

### <span data-ttu-id="b4751-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b4751-125">None</span></span>

## <span data-ttu-id="b4751-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4751-126">OUTPUTS</span></span>

### <span data-ttu-id="b4751-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b4751-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="b4751-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4751-128">NOTES</span></span>

## <span data-ttu-id="b4751-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4751-129">RELATED LINKS</span></span>
