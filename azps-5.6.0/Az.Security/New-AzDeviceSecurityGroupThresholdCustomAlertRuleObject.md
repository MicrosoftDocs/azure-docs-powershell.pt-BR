---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 869512fb91e86d90381bbcba9e492198b9a51005
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889408"
---
# <span data-ttu-id="98aa9-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="98aa9-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="98aa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="98aa9-103">Criar nova regra de alerta personalizada de limite para o grupo de segurança do dispositivo (Segurança de IoT)</span><span class="sxs-lookup"><span data-stu-id="98aa9-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="98aa9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="98aa9-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98aa9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="98aa9-105">DESCRIPTION</span></span>
<span data-ttu-id="98aa9-106">O New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet cria uma nova lista de regras de alerta personalizadas de limite para o grupo de segurança de dispositivos na solução de segurança de IoT.</span><span class="sxs-lookup"><span data-stu-id="98aa9-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="98aa9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98aa9-107">EXAMPLES</span></span>

### <span data-ttu-id="98aa9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98aa9-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="98aa9-109">Criar nova regra de alerta personalizada de limite do tipo "SomeRuleType" com valores de ant habilitados para status para limite mínimo e máximo</span><span class="sxs-lookup"><span data-stu-id="98aa9-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="98aa9-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="98aa9-110">PARAMETERS</span></span>

### <span data-ttu-id="98aa9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98aa9-111">-DefaultProfile</span></span>
<span data-ttu-id="98aa9-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98aa9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98aa9-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="98aa9-113">-Enabled</span></span>
<span data-ttu-id="98aa9-114">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="98aa9-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="98aa9-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="98aa9-115">-MaxThreshold</span></span>
<span data-ttu-id="98aa9-116">Limite máximo.</span><span class="sxs-lookup"><span data-stu-id="98aa9-116">Maximum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98aa9-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="98aa9-117">-MinThreshold</span></span>
<span data-ttu-id="98aa9-118">Limite mínimo.</span><span class="sxs-lookup"><span data-stu-id="98aa9-118">Minimum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98aa9-119">-Type</span><span class="sxs-lookup"><span data-stu-id="98aa9-119">-Type</span></span>
<span data-ttu-id="98aa9-120">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="98aa9-120">Rule type.</span></span>

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

### <span data-ttu-id="98aa9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98aa9-121">CommonParameters</span></span>
<span data-ttu-id="98aa9-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98aa9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98aa9-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98aa9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98aa9-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98aa9-124">INPUTS</span></span>

### <span data-ttu-id="98aa9-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="98aa9-125">None</span></span>

## <span data-ttu-id="98aa9-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="98aa9-126">OUTPUTS</span></span>

### <span data-ttu-id="98aa9-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="98aa9-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="98aa9-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="98aa9-128">NOTES</span></span>

## <span data-ttu-id="98aa9-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98aa9-129">RELATED LINKS</span></span>
