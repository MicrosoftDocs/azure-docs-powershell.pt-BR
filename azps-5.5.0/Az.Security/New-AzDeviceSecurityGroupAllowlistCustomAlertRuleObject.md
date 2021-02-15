---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116196"
---
# <span data-ttu-id="df215-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="df215-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="df215-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df215-102">SYNOPSIS</span></span>
<span data-ttu-id="df215-103">Criar nova regra de alerta personalizado de lista de permitir para o grupo de segurança do dispositivo (Segurança IoT)</span><span class="sxs-lookup"><span data-stu-id="df215-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="df215-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df215-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df215-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="df215-105">DESCRIPTION</span></span>
<span data-ttu-id="df215-106">O New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet cria uma nova lista de regras de alerta personalizadas permitidas para o grupo de segurança do dispositivo na solução de segurança de IoT.</span><span class="sxs-lookup"><span data-stu-id="df215-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="df215-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df215-107">EXAMPLES</span></span>

### <span data-ttu-id="df215-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df215-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="df215-109">Criar nova lista de permissão de alerta personalizado a partir do tipo "LocalUserNotAllowed" com status definido para desabilitar</span><span class="sxs-lookup"><span data-stu-id="df215-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="df215-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df215-110">PARAMETERS</span></span>

### <span data-ttu-id="df215-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="df215-111">-AllowlistValue</span></span>
<span data-ttu-id="df215-112">Permitir valores de lista.</span><span class="sxs-lookup"><span data-stu-id="df215-112">Allow list values.</span></span>

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

### <span data-ttu-id="df215-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df215-113">-DefaultProfile</span></span>
<span data-ttu-id="df215-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df215-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df215-115">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="df215-115">-Enabled</span></span>
<span data-ttu-id="df215-116">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="df215-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="df215-117">-Tipo</span><span class="sxs-lookup"><span data-stu-id="df215-117">-Type</span></span>
<span data-ttu-id="df215-118">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="df215-118">Rule type.</span></span>

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

### <span data-ttu-id="df215-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df215-119">CommonParameters</span></span>
<span data-ttu-id="df215-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df215-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df215-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df215-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df215-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="df215-122">INPUTS</span></span>

### <span data-ttu-id="df215-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="df215-123">None</span></span>

## <span data-ttu-id="df215-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="df215-124">OUTPUTS</span></span>

### <span data-ttu-id="df215-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="df215-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="df215-126">Notas</span><span class="sxs-lookup"><span data-stu-id="df215-126">NOTES</span></span>

## <span data-ttu-id="df215-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df215-127">RELATED LINKS</span></span>
