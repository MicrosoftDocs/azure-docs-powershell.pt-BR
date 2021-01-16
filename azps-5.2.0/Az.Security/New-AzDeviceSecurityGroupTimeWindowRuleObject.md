---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258931"
---
# <span data-ttu-id="cf99c-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="cf99c-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="cf99c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf99c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf99c-103">Criar nova regra de janela de horário para o grupo de segurança de dispositivo (segurança IoT)</span><span class="sxs-lookup"><span data-stu-id="cf99c-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="cf99c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf99c-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf99c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf99c-105">DESCRIPTION</span></span>
<span data-ttu-id="cf99c-106">O cmdlet New-AzDeviceSecurityGroupTimeWindowRuleObject cria uma nova lista de regras de alerta da janela de tempo para o grupo de segurança de dispositivos na solução de segurança IoT.</span><span class="sxs-lookup"><span data-stu-id="cf99c-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="cf99c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf99c-107">EXAMPLES</span></span>

### <span data-ttu-id="cf99c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cf99c-108">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize $TimeWindowSize -MinThreshold 0 -MaxThreshold 30 -Enabled $true -Type "ActiveConnectionsNotInAllowedRange"

RuleType: "ActiveConnectionsNotInAllowedRange"
DisplayName: "Number of active connections is not in allowed range"
Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 30
TimeWindowSize: "PT5M"
```

<span data-ttu-id="cf99c-109">Criar nova regra de janela de horário do tipo "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="cf99c-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="cf99c-110">OS</span><span class="sxs-lookup"><span data-stu-id="cf99c-110">PARAMETERS</span></span>

### <span data-ttu-id="cf99c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf99c-111">-DefaultProfile</span></span>
<span data-ttu-id="cf99c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf99c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf99c-113">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="cf99c-113">-Enabled</span></span>
<span data-ttu-id="cf99c-114">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="cf99c-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="cf99c-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="cf99c-115">-MaxThreshold</span></span>
<span data-ttu-id="cf99c-116">Limite máximo.</span><span class="sxs-lookup"><span data-stu-id="cf99c-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="cf99c-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="cf99c-117">-MinThreshold</span></span>
<span data-ttu-id="cf99c-118">Limite mínimo.</span><span class="sxs-lookup"><span data-stu-id="cf99c-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="cf99c-119">-Janelas-ponto</span><span class="sxs-lookup"><span data-stu-id="cf99c-119">-TimeWindowSize</span></span>
<span data-ttu-id="cf99c-120">Tamanho da janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="cf99c-120">Time window size.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf99c-121">-Digite</span><span class="sxs-lookup"><span data-stu-id="cf99c-121">-Type</span></span>
<span data-ttu-id="cf99c-122">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="cf99c-122">Rule type.</span></span>

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

### <span data-ttu-id="cf99c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf99c-123">CommonParameters</span></span>
<span data-ttu-id="cf99c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf99c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf99c-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf99c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf99c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf99c-126">INPUTS</span></span>

### <span data-ttu-id="cf99c-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cf99c-127">None</span></span>

## <span data-ttu-id="cf99c-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf99c-128">OUTPUTS</span></span>

### <span data-ttu-id="cf99c-129">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="cf99c-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="cf99c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf99c-130">NOTES</span></span>

## <span data-ttu-id="cf99c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf99c-131">RELATED LINKS</span></span>
