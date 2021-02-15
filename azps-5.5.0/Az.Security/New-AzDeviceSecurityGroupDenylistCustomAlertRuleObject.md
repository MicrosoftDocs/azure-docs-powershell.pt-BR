---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118714"
---
# <span data-ttu-id="449f6-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="449f6-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="449f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="449f6-102">SYNOPSIS</span></span>
<span data-ttu-id="449f6-103">Criar nova regra de alerta personalizado da lista de negação para o grupo de segurança do dispositivo (Segurança IoT)</span><span class="sxs-lookup"><span data-stu-id="449f6-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="449f6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="449f6-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="449f6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="449f6-105">DESCRIPTION</span></span>
<span data-ttu-id="449f6-106">O New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet cria uma nova lista de regras de alerta personalizadas negadas para o grupo de segurança do dispositivo na solução de segurança de IoT.</span><span class="sxs-lookup"><span data-stu-id="449f6-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="449f6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="449f6-107">EXAMPLES</span></span>

### <span data-ttu-id="449f6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="449f6-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="449f6-109">Criar nova regra de alerta personalizado da lista de negação com o tipo "SomeRuleType" e status definido como desvível</span><span class="sxs-lookup"><span data-stu-id="449f6-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="449f6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="449f6-110">PARAMETERS</span></span>

### <span data-ttu-id="449f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="449f6-111">-DefaultProfile</span></span>
<span data-ttu-id="449f6-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="449f6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="449f6-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="449f6-113">-DenylistValue</span></span>
<span data-ttu-id="449f6-114">Negar valores de lista.</span><span class="sxs-lookup"><span data-stu-id="449f6-114">Deny list values.</span></span>

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

### <span data-ttu-id="449f6-115">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="449f6-115">-Enabled</span></span>
<span data-ttu-id="449f6-116">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="449f6-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="449f6-117">-Tipo</span><span class="sxs-lookup"><span data-stu-id="449f6-117">-Type</span></span>
<span data-ttu-id="449f6-118">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="449f6-118">Rule type.</span></span>

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

### <span data-ttu-id="449f6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="449f6-119">CommonParameters</span></span>
<span data-ttu-id="449f6-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="449f6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="449f6-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="449f6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="449f6-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="449f6-122">INPUTS</span></span>

### <span data-ttu-id="449f6-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="449f6-123">None</span></span>

## <span data-ttu-id="449f6-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="449f6-124">OUTPUTS</span></span>

### <span data-ttu-id="449f6-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="449f6-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="449f6-126">Notas</span><span class="sxs-lookup"><span data-stu-id="449f6-126">NOTES</span></span>

## <span data-ttu-id="449f6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="449f6-127">RELATED LINKS</span></span>
