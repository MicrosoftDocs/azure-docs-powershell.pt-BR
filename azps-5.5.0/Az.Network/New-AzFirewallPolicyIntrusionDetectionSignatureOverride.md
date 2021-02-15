---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: d2389a8d4880b576e51cda41ac3c15bd091257c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112834"
---
# <span data-ttu-id="3c701-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="3c701-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="3c701-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c701-102">SYNOPSIS</span></span>
<span data-ttu-id="3c701-103">Cria uma nova Substituição de Assinatura de Detecção de Invasão de Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="3c701-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="3c701-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c701-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c701-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c701-105">DESCRIPTION</span></span>
<span data-ttu-id="3c701-106">O cmdlet **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cria um Objeto de Substituição de Assinatura de Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c701-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="3c701-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3c701-107">EXAMPLES</span></span>

### <span data-ttu-id="3c701-108">Exemplo 1: 1.</span><span class="sxs-lookup"><span data-stu-id="3c701-108">Example 1: 1.</span></span> <span data-ttu-id="3c701-109">Criar detecção de invasão com substituições de assinatura</span><span class="sxs-lookup"><span data-stu-id="3c701-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="3c701-110">Este exemplo cria a detecção de invasão com substituição de assinatura específica para o modo Negar</span><span class="sxs-lookup"><span data-stu-id="3c701-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="3c701-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c701-111">PARAMETERS</span></span>

### <span data-ttu-id="3c701-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c701-112">-DefaultProfile</span></span>
<span data-ttu-id="3c701-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c701-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c701-114">-ID</span><span class="sxs-lookup"><span data-stu-id="3c701-114">-Id</span></span>
<span data-ttu-id="3c701-115">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3c701-115">Signature id.</span></span>

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

### <span data-ttu-id="3c701-116">-Modo</span><span class="sxs-lookup"><span data-stu-id="3c701-116">-Mode</span></span>
<span data-ttu-id="3c701-117">Estado da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3c701-117">Signature state.</span></span>

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

### <span data-ttu-id="3c701-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3c701-118">-Confirm</span></span>
<span data-ttu-id="3c701-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c701-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c701-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c701-120">-WhatIf</span></span>
<span data-ttu-id="3c701-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3c701-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c701-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c701-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c701-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c701-123">CommonParameters</span></span>
<span data-ttu-id="3c701-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c701-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c701-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c701-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c701-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="3c701-126">INPUTS</span></span>

### <span data-ttu-id="3c701-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3c701-127">None</span></span>

## <span data-ttu-id="3c701-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="3c701-128">OUTPUTS</span></span>

### <span data-ttu-id="3c701-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="3c701-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="3c701-130">Notas</span><span class="sxs-lookup"><span data-stu-id="3c701-130">NOTES</span></span>

## <span data-ttu-id="3c701-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c701-131">RELATED LINKS</span></span>
