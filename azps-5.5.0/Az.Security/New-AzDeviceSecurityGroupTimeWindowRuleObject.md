---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116193"
---
# <span data-ttu-id="ca0e9-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="ca0e9-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="ca0e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca0e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ca0e9-103">Criar nova regra de janela de tempo para o grupo de segurança do dispositivo (Segurança de IoT)</span><span class="sxs-lookup"><span data-stu-id="ca0e9-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="ca0e9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca0e9-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca0e9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca0e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ca0e9-106">O New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet cria uma nova lista de regras de alerta de janela de tempo para o grupo de segurança do dispositivo na solução de segurança de IoT.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="ca0e9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca0e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ca0e9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca0e9-108">Example 1</span></span>
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

<span data-ttu-id="ca0e9-109">Criar nova regra de janela de tempo do tipo "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="ca0e9-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="ca0e9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca0e9-110">PARAMETERS</span></span>

### <span data-ttu-id="ca0e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca0e9-111">-DefaultProfile</span></span>
<span data-ttu-id="ca0e9-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca0e9-113">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="ca0e9-113">-Enabled</span></span>
<span data-ttu-id="ca0e9-114">A regra está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="ca0e9-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="ca0e9-115">-MaxThreshold</span></span>
<span data-ttu-id="ca0e9-116">Limite máximo.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="ca0e9-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="ca0e9-117">-MinThreshold</span></span>
<span data-ttu-id="ca0e9-118">Limite mínimo.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="ca0e9-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="ca0e9-119">-TimeWindowSize</span></span>
<span data-ttu-id="ca0e9-120">Tamanho da janela de tempo.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-120">Time window size.</span></span>

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

### <span data-ttu-id="ca0e9-121">-Tipo</span><span class="sxs-lookup"><span data-stu-id="ca0e9-121">-Type</span></span>
<span data-ttu-id="ca0e9-122">Tipo de regra.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-122">Rule type.</span></span>

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

### <span data-ttu-id="ca0e9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca0e9-123">CommonParameters</span></span>
<span data-ttu-id="ca0e9-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca0e9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca0e9-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca0e9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca0e9-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="ca0e9-126">INPUTS</span></span>

### <span data-ttu-id="ca0e9-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ca0e9-127">None</span></span>

## <span data-ttu-id="ca0e9-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="ca0e9-128">OUTPUTS</span></span>

### <span data-ttu-id="ca0e9-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="ca0e9-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="ca0e9-130">Notas</span><span class="sxs-lookup"><span data-stu-id="ca0e9-130">NOTES</span></span>

## <span data-ttu-id="ca0e9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca0e9-131">RELATED LINKS</span></span>
