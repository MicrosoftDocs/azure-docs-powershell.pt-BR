---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944810"
---
# <span data-ttu-id="cad75-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="cad75-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="cad75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cad75-102">SYNOPSIS</span></span>
<span data-ttu-id="cad75-103">Cria uma configuração de política para a política de firewall</span><span class="sxs-lookup"><span data-stu-id="cad75-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="cad75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cad75-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cad75-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cad75-105">DESCRIPTION</span></span>
<span data-ttu-id="cad75-106">O **New-AzApplicationGatewayFirewallPolicySetting** cria configurações de política para uma política de firewall.</span><span class="sxs-lookup"><span data-stu-id="cad75-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="cad75-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cad75-107">EXAMPLES</span></span>

### <span data-ttu-id="cad75-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cad75-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="cad75-109">O comando cria uma configuração de política com estado como $enabledState, Mode como $enabledMode, RequestBodyCheck como false, FileUploadLimitInMb como $fileUploadLimitInMb e MaxRequestBodySizeInKb como $ $maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="cad75-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="cad75-110">O novo policySettings é armazenado em $condition.</span><span class="sxs-lookup"><span data-stu-id="cad75-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="cad75-111">OS</span><span class="sxs-lookup"><span data-stu-id="cad75-111">PARAMETERS</span></span>

### <span data-ttu-id="cad75-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad75-112">-DefaultProfile</span></span>
<span data-ttu-id="cad75-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cad75-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cad75-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="cad75-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="cad75-115">Permite que o requestBodyCheck nas configurações de política da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="cad75-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="cad75-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="cad75-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="cad75-117">Tamanho máximo do carregamento do filevolume em MB.</span><span class="sxs-lookup"><span data-stu-id="cad75-117">Maximum fileUpload size in MB.</span></span>

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

### <span data-ttu-id="cad75-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="cad75-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="cad75-119">MaxRequestBodySizeInKb em configurações de política da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="cad75-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="cad75-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="cad75-120">-Mode</span></span>
<span data-ttu-id="cad75-121">Modo de firewall nas configurações de política da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="cad75-121">Firewall Mode in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="cad75-122">-Estado</span><span class="sxs-lookup"><span data-stu-id="cad75-122">-State</span></span>
<span data-ttu-id="cad75-123">Variável de estado nas configurações de política da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="cad75-123">State variable in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="cad75-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad75-124">CommonParameters</span></span>
<span data-ttu-id="cad75-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cad75-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad75-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cad75-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad75-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cad75-127">INPUTS</span></span>

### <span data-ttu-id="cad75-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cad75-128">None</span></span>

## <span data-ttu-id="cad75-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cad75-129">OUTPUTS</span></span>

### <span data-ttu-id="cad75-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="cad75-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="cad75-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cad75-131">NOTES</span></span>

## <span data-ttu-id="cad75-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cad75-132">RELATED LINKS</span></span>
