---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110902"
---
# <span data-ttu-id="fdf4d-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="fdf4d-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="fdf4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdf4d-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf4d-103">Criar uma nova regra de alerta personalizada da lista de negações para o grupo de segurança do dispositivo (segurança de IoT)</span><span class="sxs-lookup"><span data-stu-id="fdf4d-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="fdf4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdf4d-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf4d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdf4d-105">DESCRIPTION</span></span>
<span data-ttu-id="fdf4d-106">O cmdlet New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cria uma nova lista de regras de alerta personalizadas negadas para o grupo de segurança de dispositivos na solução de segurança IoT.</span><span class="sxs-lookup"><span data-stu-id="fdf4d-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="fdf4d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdf4d-107">EXAMPLES</span></span>

### <span data-ttu-id="fdf4d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fdf4d-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="fdf4d-109">Criar uma nova regra de alerta personalizada da lista de negações com o tipo de Rull "SomeRuleType" e o status definido como desable</span><span class="sxs-lookup"><span data-stu-id="fdf4d-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="fdf4d-110">OS</span><span class="sxs-lookup"><span data-stu-id="fdf4d-110">PARAMETERS</span></span>

### <span data-ttu-id="fdf4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf4d-111">-DefaultProfile</span></span>
<span data-ttu-id="fdf4d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdf4d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdf4d-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="fdf4d-113">-DenylistValue</span></span>
<span data-ttu-id="fdf4d-114">Negar valores de lista.</span><span class="sxs-lookup"><span data-stu-id="fdf4d-114">Deny list values.</span></span>

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

### <span data-ttu-id="fdf4d-115">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="fdf4d-115">-Enabled</span></span>
<span data-ttu-id="fdf4d-116">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="fdf4d-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="fdf4d-117">-Digite</span><span class="sxs-lookup"><span data-stu-id="fdf4d-117">-Type</span></span>
<span data-ttu-id="fdf4d-118">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="fdf4d-118">Rule type.</span></span>

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

### <span data-ttu-id="fdf4d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf4d-119">CommonParameters</span></span>
<span data-ttu-id="fdf4d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf4d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf4d-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdf4d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf4d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdf4d-122">INPUTS</span></span>

### <span data-ttu-id="fdf4d-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fdf4d-123">None</span></span>

## <span data-ttu-id="fdf4d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdf4d-124">OUTPUTS</span></span>

### <span data-ttu-id="fdf4d-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="fdf4d-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="fdf4d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdf4d-126">NOTES</span></span>

## <span data-ttu-id="fdf4d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdf4d-127">RELATED LINKS</span></span>
