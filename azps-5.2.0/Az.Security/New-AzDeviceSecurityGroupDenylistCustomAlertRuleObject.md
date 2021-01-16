---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258944"
---
# <span data-ttu-id="d9cfe-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="d9cfe-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="d9cfe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9cfe-102">SYNOPSIS</span></span>
<span data-ttu-id="d9cfe-103">Criar uma nova regra de alerta personalizada da lista de negações para o grupo de segurança do dispositivo (segurança de IoT)</span><span class="sxs-lookup"><span data-stu-id="d9cfe-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="d9cfe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9cfe-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9cfe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9cfe-105">DESCRIPTION</span></span>
<span data-ttu-id="d9cfe-106">O cmdlet New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cria uma nova lista de regras de alerta personalizadas negadas para o grupo de segurança de dispositivos na solução de segurança IoT.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="d9cfe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9cfe-107">EXAMPLES</span></span>

### <span data-ttu-id="d9cfe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d9cfe-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="d9cfe-109">Criar uma nova regra de alerta personalizada da lista de negações com o tipo de Rull "SomeRuleType" e o status definido como desable</span><span class="sxs-lookup"><span data-stu-id="d9cfe-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="d9cfe-110">OS</span><span class="sxs-lookup"><span data-stu-id="d9cfe-110">PARAMETERS</span></span>

### <span data-ttu-id="d9cfe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9cfe-111">-DefaultProfile</span></span>
<span data-ttu-id="d9cfe-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9cfe-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="d9cfe-113">-DenylistValue</span></span>
<span data-ttu-id="d9cfe-114">Negar valores de lista.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-114">Deny list values.</span></span>

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

### <span data-ttu-id="d9cfe-115">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="d9cfe-115">-Enabled</span></span>
<span data-ttu-id="d9cfe-116">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="d9cfe-117">-Digite</span><span class="sxs-lookup"><span data-stu-id="d9cfe-117">-Type</span></span>
<span data-ttu-id="d9cfe-118">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-118">Rule type.</span></span>

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

### <span data-ttu-id="d9cfe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9cfe-119">CommonParameters</span></span>
<span data-ttu-id="d9cfe-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9cfe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9cfe-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9cfe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9cfe-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9cfe-122">INPUTS</span></span>

### <span data-ttu-id="d9cfe-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d9cfe-123">None</span></span>

## <span data-ttu-id="d9cfe-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9cfe-124">OUTPUTS</span></span>

### <span data-ttu-id="d9cfe-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="d9cfe-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="d9cfe-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9cfe-126">NOTES</span></span>

## <span data-ttu-id="d9cfe-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9cfe-127">RELATED LINKS</span></span>
