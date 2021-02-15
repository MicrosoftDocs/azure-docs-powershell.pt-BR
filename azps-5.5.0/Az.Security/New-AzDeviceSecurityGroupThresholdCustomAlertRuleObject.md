---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116197"
---
# <span data-ttu-id="33f16-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="33f16-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="33f16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33f16-102">SYNOPSIS</span></span>
<span data-ttu-id="33f16-103">Criar nova regra de alerta personalizado de limite para o grupo de segurança do dispositivo (Segurança IoT)</span><span class="sxs-lookup"><span data-stu-id="33f16-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="33f16-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33f16-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33f16-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="33f16-105">DESCRIPTION</span></span>
<span data-ttu-id="33f16-106">O New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet cria uma nova lista de regras de alerta personalizado limite para o grupo de segurança do dispositivo na solução de segurança de IoT.</span><span class="sxs-lookup"><span data-stu-id="33f16-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="33f16-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="33f16-107">EXAMPLES</span></span>

### <span data-ttu-id="33f16-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="33f16-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="33f16-109">Criar nova regra de alerta personalizado de limite do tipo "SomeRuleType" com valores de status habilitados para limite mínimo e máximo</span><span class="sxs-lookup"><span data-stu-id="33f16-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="33f16-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33f16-110">PARAMETERS</span></span>

### <span data-ttu-id="33f16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f16-111">-DefaultProfile</span></span>
<span data-ttu-id="33f16-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33f16-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33f16-113">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="33f16-113">-Enabled</span></span>
<span data-ttu-id="33f16-114">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="33f16-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="33f16-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="33f16-115">-MaxThreshold</span></span>
<span data-ttu-id="33f16-116">Limite máximo.</span><span class="sxs-lookup"><span data-stu-id="33f16-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="33f16-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="33f16-117">-MinThreshold</span></span>
<span data-ttu-id="33f16-118">Limite mínimo.</span><span class="sxs-lookup"><span data-stu-id="33f16-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="33f16-119">-Tipo</span><span class="sxs-lookup"><span data-stu-id="33f16-119">-Type</span></span>
<span data-ttu-id="33f16-120">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="33f16-120">Rule type.</span></span>

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

### <span data-ttu-id="33f16-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f16-121">CommonParameters</span></span>
<span data-ttu-id="33f16-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f16-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f16-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33f16-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f16-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="33f16-124">INPUTS</span></span>

### <span data-ttu-id="33f16-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="33f16-125">None</span></span>

## <span data-ttu-id="33f16-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="33f16-126">OUTPUTS</span></span>

### <span data-ttu-id="33f16-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="33f16-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="33f16-128">Notas</span><span class="sxs-lookup"><span data-stu-id="33f16-128">NOTES</span></span>

## <span data-ttu-id="33f16-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33f16-129">RELATED LINKS</span></span>
