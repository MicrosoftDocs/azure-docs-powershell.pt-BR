---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: 256509a42b844b196728b89b30abcdb6c5b9b386
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886728"
---
# <span data-ttu-id="0bb48-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="0bb48-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="0bb48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bb48-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb48-103">Cria uma configuração de política para a política de firewall</span><span class="sxs-lookup"><span data-stu-id="0bb48-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="0bb48-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0bb48-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0bb48-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0bb48-105">DESCRIPTION</span></span>
<span data-ttu-id="0bb48-106">O **New-AzApplicationGatewayFirewallPolicySetting** cria uma configuração de política para uma política de firewall.</span><span class="sxs-lookup"><span data-stu-id="0bb48-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="0bb48-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bb48-107">EXAMPLES</span></span>

### <span data-ttu-id="0bb48-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0bb48-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="0bb48-109">O comando cria uma configuração de política com estado como $enabledState, modo como $enabledMode, RequestBodyCheck como false, FileUploadLimitInMb como $fileUploadLimitInMb e MaxRequestBodySizeInKb como $$maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="0bb48-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="0bb48-110">A nova policySettings é armazenada para $condition.</span><span class="sxs-lookup"><span data-stu-id="0bb48-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="0bb48-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0bb48-111">PARAMETERS</span></span>

### <span data-ttu-id="0bb48-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb48-112">-DefaultProfile</span></span>
<span data-ttu-id="0bb48-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb48-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bb48-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="0bb48-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="0bb48-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span><span class="sxs-lookup"><span data-stu-id="0bb48-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb48-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="0bb48-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="0bb48-117">Tamanho máximo de fileUpload em MB.</span><span class="sxs-lookup"><span data-stu-id="0bb48-117">Maximum fileUpload size in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb48-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="0bb48-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="0bb48-119">MaxRequestBodySizeInKb nas configurações de política da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="0bb48-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 128
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb48-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="0bb48-120">-Mode</span></span>
<span data-ttu-id="0bb48-121">Modo firewall nas configurações de política da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="0bb48-121">Firewall Mode in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: Detection
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb48-122">-State</span><span class="sxs-lookup"><span data-stu-id="0bb48-122">-State</span></span>
<span data-ttu-id="0bb48-123">Variável de estado nas configurações de política da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="0bb48-123">State variable in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bb48-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb48-124">CommonParameters</span></span>
<span data-ttu-id="0bb48-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb48-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb48-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bb48-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb48-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bb48-127">INPUTS</span></span>

### <span data-ttu-id="0bb48-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0bb48-128">None</span></span>

## <span data-ttu-id="0bb48-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0bb48-129">OUTPUTS</span></span>

### <span data-ttu-id="0bb48-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="0bb48-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="0bb48-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="0bb48-131">NOTES</span></span>

## <span data-ttu-id="0bb48-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bb48-132">RELATED LINKS</span></span>
