---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271543"
---
# <span data-ttu-id="7a11a-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="7a11a-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="7a11a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a11a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a11a-103">Criar nova regra de alerta personalizado de limite para o grupo de segurança do dispositivo (segurança de IoT)</span><span class="sxs-lookup"><span data-stu-id="7a11a-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="7a11a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a11a-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a11a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a11a-105">DESCRIPTION</span></span>
<span data-ttu-id="7a11a-106">O cmdlet New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cria uma nova lista de regras de alerta personalizadas de limite para o grupo de segurança de dispositivos na solução de segurança IoT.</span><span class="sxs-lookup"><span data-stu-id="7a11a-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="7a11a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a11a-107">EXAMPLES</span></span>

### <span data-ttu-id="7a11a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a11a-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="7a11a-109">Criar nova regra de alerta personalizado de limite do tipo "SomeRuleType" com o status habilitado para valores Ant para o limite mínimo e máximo</span><span class="sxs-lookup"><span data-stu-id="7a11a-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="7a11a-110">OS</span><span class="sxs-lookup"><span data-stu-id="7a11a-110">PARAMETERS</span></span>

### <span data-ttu-id="7a11a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a11a-111">-DefaultProfile</span></span>
<span data-ttu-id="7a11a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a11a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a11a-113">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="7a11a-113">-Enabled</span></span>
<span data-ttu-id="7a11a-114">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="7a11a-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="7a11a-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="7a11a-115">-MaxThreshold</span></span>
<span data-ttu-id="7a11a-116">Limite máximo.</span><span class="sxs-lookup"><span data-stu-id="7a11a-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="7a11a-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="7a11a-117">-MinThreshold</span></span>
<span data-ttu-id="7a11a-118">Limite mínimo.</span><span class="sxs-lookup"><span data-stu-id="7a11a-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="7a11a-119">-Digite</span><span class="sxs-lookup"><span data-stu-id="7a11a-119">-Type</span></span>
<span data-ttu-id="7a11a-120">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="7a11a-120">Rule type.</span></span>

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

### <span data-ttu-id="7a11a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a11a-121">CommonParameters</span></span>
<span data-ttu-id="7a11a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a11a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a11a-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a11a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a11a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a11a-124">INPUTS</span></span>

### <span data-ttu-id="7a11a-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7a11a-125">None</span></span>

## <span data-ttu-id="7a11a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a11a-126">OUTPUTS</span></span>

### <span data-ttu-id="7a11a-127">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="7a11a-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="7a11a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a11a-128">NOTES</span></span>

## <span data-ttu-id="7a11a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a11a-129">RELATED LINKS</span></span>
