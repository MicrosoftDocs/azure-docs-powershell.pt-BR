---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: c6aa2bb9bf3866e35ad59e59bdf5ded333fd2816
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893137"
---
# <span data-ttu-id="e262b-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="e262b-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="e262b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e262b-102">SYNOPSIS</span></span>
<span data-ttu-id="e262b-103">Cria uma nova Substituição de Assinatura de Detecção de Invasão de Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e262b-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="e262b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e262b-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e262b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e262b-105">DESCRIPTION</span></span>
<span data-ttu-id="e262b-106">O cmdlet **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cria um objeto de substituição de assinatura de política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="e262b-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="e262b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e262b-107">EXAMPLES</span></span>

### <span data-ttu-id="e262b-108">Exemplo 1: 1.</span><span class="sxs-lookup"><span data-stu-id="e262b-108">Example 1: 1.</span></span> <span data-ttu-id="e262b-109">Criar detecção de intrusão com substituições de assinatura</span><span class="sxs-lookup"><span data-stu-id="e262b-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="e262b-110">Este exemplo cria a detecção de intrusão com substituição de assinatura específica para o modo Negar</span><span class="sxs-lookup"><span data-stu-id="e262b-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="e262b-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e262b-111">PARAMETERS</span></span>

### <span data-ttu-id="e262b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e262b-112">-DefaultProfile</span></span>
<span data-ttu-id="e262b-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e262b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e262b-114">-Id</span><span class="sxs-lookup"><span data-stu-id="e262b-114">-Id</span></span>
<span data-ttu-id="e262b-115">ID de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e262b-115">Signature id.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e262b-116">-Mode</span><span class="sxs-lookup"><span data-stu-id="e262b-116">-Mode</span></span>
<span data-ttu-id="e262b-117">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e262b-117">Signature state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e262b-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e262b-118">-Confirm</span></span>
<span data-ttu-id="e262b-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e262b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e262b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e262b-120">-WhatIf</span></span>
<span data-ttu-id="e262b-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e262b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e262b-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e262b-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e262b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e262b-123">CommonParameters</span></span>
<span data-ttu-id="e262b-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e262b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e262b-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e262b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e262b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e262b-126">INPUTS</span></span>

### <span data-ttu-id="e262b-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e262b-127">None</span></span>

## <span data-ttu-id="e262b-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e262b-128">OUTPUTS</span></span>

### <span data-ttu-id="e262b-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="e262b-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="e262b-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="e262b-130">NOTES</span></span>

## <span data-ttu-id="e262b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e262b-131">RELATED LINKS</span></span>
