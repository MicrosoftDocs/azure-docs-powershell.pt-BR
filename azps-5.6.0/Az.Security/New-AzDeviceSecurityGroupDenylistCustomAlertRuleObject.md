---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0b915176858c0641ca3076ea10022ae193718807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888795"
---
# <span data-ttu-id="6f8c9-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="6f8c9-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="6f8c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8c9-103">Criar nova regra de alerta personalizado de lista de negação para o grupo de segurança do dispositivo (Segurança de IoT)</span><span class="sxs-lookup"><span data-stu-id="6f8c9-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="6f8c9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6f8c9-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f8c9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6f8c9-105">DESCRIPTION</span></span>
<span data-ttu-id="6f8c9-106">O New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet cria uma nova lista de regras de alerta personalizadas negadas para o grupo de segurança de dispositivos na solução de segurança da IoT.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="6f8c9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f8c9-107">EXAMPLES</span></span>

### <span data-ttu-id="6f8c9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f8c9-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="6f8c9-109">Criar nova regra de alerta personalizada de lista de negação com o tipo rull "SomeRuleType" e o status definido como desable</span><span class="sxs-lookup"><span data-stu-id="6f8c9-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="6f8c9-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6f8c9-110">PARAMETERS</span></span>

### <span data-ttu-id="6f8c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8c9-111">-DefaultProfile</span></span>
<span data-ttu-id="6f8c9-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f8c9-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="6f8c9-113">-DenylistValue</span></span>
<span data-ttu-id="6f8c9-114">Negar valores de lista.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-114">Deny list values.</span></span>

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

### <span data-ttu-id="6f8c9-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="6f8c9-115">-Enabled</span></span>
<span data-ttu-id="6f8c9-116">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="6f8c9-117">-Type</span><span class="sxs-lookup"><span data-stu-id="6f8c9-117">-Type</span></span>
<span data-ttu-id="6f8c9-118">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-118">Rule type.</span></span>

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

### <span data-ttu-id="6f8c9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8c9-119">CommonParameters</span></span>
<span data-ttu-id="6f8c9-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f8c9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8c9-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f8c9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8c9-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f8c9-122">INPUTS</span></span>

### <span data-ttu-id="6f8c9-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6f8c9-123">None</span></span>

## <span data-ttu-id="6f8c9-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6f8c9-124">OUTPUTS</span></span>

### <span data-ttu-id="6f8c9-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="6f8c9-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="6f8c9-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="6f8c9-126">NOTES</span></span>

## <span data-ttu-id="6f8c9-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f8c9-127">RELATED LINKS</span></span>
