---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: 0f46a0f009085aa7ef7b66ac91d621338a7358b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888796"
---
# <span data-ttu-id="61e7e-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="61e7e-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="61e7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61e7e-102">SYNOPSIS</span></span>
<span data-ttu-id="61e7e-103">Criar nova regra de alerta personalizado de lista de permitir para o grupo de segurança do dispositivo (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="61e7e-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="61e7e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="61e7e-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61e7e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="61e7e-105">DESCRIPTION</span></span>
<span data-ttu-id="61e7e-106">O New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet cria uma nova lista de regras de alerta personalizadas permitidas para o grupo de segurança de dispositivos na solução de segurança da IoT.</span><span class="sxs-lookup"><span data-stu-id="61e7e-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="61e7e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61e7e-107">EXAMPLES</span></span>

### <span data-ttu-id="61e7e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61e7e-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="61e7e-109">Criar nova lista de permissão rull de alerta personalizado do tipo "LocalUserNotAllowed" com status definido para desabilitar</span><span class="sxs-lookup"><span data-stu-id="61e7e-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="61e7e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="61e7e-110">PARAMETERS</span></span>

### <span data-ttu-id="61e7e-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="61e7e-111">-AllowlistValue</span></span>
<span data-ttu-id="61e7e-112">Permitir valores de lista.</span><span class="sxs-lookup"><span data-stu-id="61e7e-112">Allow list values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e7e-113">-DefaultProfile</span></span>
<span data-ttu-id="61e7e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61e7e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61e7e-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="61e7e-115">-Enabled</span></span>
<span data-ttu-id="61e7e-116">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="61e7e-116">Is rule enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e7e-117">-Type</span><span class="sxs-lookup"><span data-stu-id="61e7e-117">-Type</span></span>
<span data-ttu-id="61e7e-118">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="61e7e-118">Rule type.</span></span>

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

### <span data-ttu-id="61e7e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e7e-119">CommonParameters</span></span>
<span data-ttu-id="61e7e-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e7e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e7e-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61e7e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e7e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61e7e-122">INPUTS</span></span>

### <span data-ttu-id="61e7e-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="61e7e-123">None</span></span>

## <span data-ttu-id="61e7e-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="61e7e-124">OUTPUTS</span></span>

### <span data-ttu-id="61e7e-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="61e7e-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="61e7e-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="61e7e-126">NOTES</span></span>

## <span data-ttu-id="61e7e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61e7e-127">RELATED LINKS</span></span>
