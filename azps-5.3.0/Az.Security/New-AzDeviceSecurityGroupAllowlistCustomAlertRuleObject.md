---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271544"
---
# <span data-ttu-id="9e70d-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="9e70d-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="9e70d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e70d-102">SYNOPSIS</span></span>
<span data-ttu-id="9e70d-103">Criar uma nova regra de alerta personalizada de lista de permissões para o grupo de segurança de dispositivo (segurança IoT)</span><span class="sxs-lookup"><span data-stu-id="9e70d-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="9e70d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e70d-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e70d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e70d-105">DESCRIPTION</span></span>
<span data-ttu-id="9e70d-106">O cmdlet New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cria uma nova lista de regras de alerta personalizadas permitidas para o grupo de segurança de dispositivos na solução de segurança IoT.</span><span class="sxs-lookup"><span data-stu-id="9e70d-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="9e70d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e70d-107">EXAMPLES</span></span>

### <span data-ttu-id="9e70d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9e70d-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="9e70d-109">Criar uma nova lista de permissões Rull de alerta personalizada do tipo "LocalUserNotAllowed" com o status definido como Disable</span><span class="sxs-lookup"><span data-stu-id="9e70d-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="9e70d-110">OS</span><span class="sxs-lookup"><span data-stu-id="9e70d-110">PARAMETERS</span></span>

### <span data-ttu-id="9e70d-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="9e70d-111">-AllowlistValue</span></span>
<span data-ttu-id="9e70d-112">Permitir valores de lista.</span><span class="sxs-lookup"><span data-stu-id="9e70d-112">Allow list values.</span></span>

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

### <span data-ttu-id="9e70d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e70d-113">-DefaultProfile</span></span>
<span data-ttu-id="9e70d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e70d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e70d-115">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="9e70d-115">-Enabled</span></span>
<span data-ttu-id="9e70d-116">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="9e70d-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="9e70d-117">-Digite</span><span class="sxs-lookup"><span data-stu-id="9e70d-117">-Type</span></span>
<span data-ttu-id="9e70d-118">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="9e70d-118">Rule type.</span></span>

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

### <span data-ttu-id="9e70d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e70d-119">CommonParameters</span></span>
<span data-ttu-id="9e70d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e70d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e70d-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e70d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e70d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e70d-122">INPUTS</span></span>

### <span data-ttu-id="9e70d-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9e70d-123">None</span></span>

## <span data-ttu-id="9e70d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e70d-124">OUTPUTS</span></span>

### <span data-ttu-id="9e70d-125">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="9e70d-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="9e70d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e70d-126">NOTES</span></span>

## <span data-ttu-id="9e70d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e70d-127">RELATED LINKS</span></span>
