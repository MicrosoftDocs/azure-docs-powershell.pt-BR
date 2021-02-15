---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115142"
---
# <span data-ttu-id="29989-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="29989-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="29989-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29989-102">SYNOPSIS</span></span>
<span data-ttu-id="29989-103">Cria uma configuração de política para a política de firewall</span><span class="sxs-lookup"><span data-stu-id="29989-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="29989-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29989-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29989-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="29989-105">DESCRIPTION</span></span>
<span data-ttu-id="29989-106">O **New-AzApplicationGatewayFirewallPolicySetting** cria uma configurações de política para uma política de firewall.</span><span class="sxs-lookup"><span data-stu-id="29989-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="29989-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="29989-107">EXAMPLES</span></span>

### <span data-ttu-id="29989-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29989-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="29989-109">O comando cria uma configuração de política com estado como $enabledState, modo como $enabledMode, RequestCheck como falso, FileUploadLimitInMb como $fileUploadLimitInMb e MaxRequestLoadSizeInKb como $$maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="29989-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="29989-110">As novasconjunções de política são armazenadas em $condition.</span><span class="sxs-lookup"><span data-stu-id="29989-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="29989-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29989-111">PARAMETERS</span></span>

### <span data-ttu-id="29989-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29989-112">-DefaultProfile</span></span>
<span data-ttu-id="29989-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29989-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29989-114">-DisableRequestCheck</span><span class="sxs-lookup"><span data-stu-id="29989-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="29989-115">Disca a solicitaçãoCheck Nas configurações de política da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="29989-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="29989-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="29989-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="29989-117">Tamanho máximo de fileUpload em MB.</span><span class="sxs-lookup"><span data-stu-id="29989-117">Maximum fileUpload size in MB.</span></span>

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

### <span data-ttu-id="29989-118">-MaxRequest WidgetSizeInKb</span><span class="sxs-lookup"><span data-stu-id="29989-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="29989-119">MaxRequestEsizeInKb nas configurações de política da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="29989-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="29989-120">-Modo</span><span class="sxs-lookup"><span data-stu-id="29989-120">-Mode</span></span>
<span data-ttu-id="29989-121">Modo de Firewall nas configurações de política da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="29989-121">Firewall Mode in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="29989-122">-Estado</span><span class="sxs-lookup"><span data-stu-id="29989-122">-State</span></span>
<span data-ttu-id="29989-123">Variável de estado nas configurações de política da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="29989-123">State variable in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="29989-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29989-124">CommonParameters</span></span>
<span data-ttu-id="29989-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29989-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29989-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29989-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29989-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="29989-127">INPUTS</span></span>

### <span data-ttu-id="29989-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="29989-128">None</span></span>

## <span data-ttu-id="29989-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="29989-129">OUTPUTS</span></span>

### <span data-ttu-id="29989-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="29989-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="29989-131">Notas</span><span class="sxs-lookup"><span data-stu-id="29989-131">NOTES</span></span>

## <span data-ttu-id="29989-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29989-132">RELATED LINKS</span></span>
