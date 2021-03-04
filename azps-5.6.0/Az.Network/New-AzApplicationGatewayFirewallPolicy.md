---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e643bf488073f6da685265cea4a2a0c6cb7cebf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887700"
---
# <span data-ttu-id="c22c7-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c22c7-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="c22c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c22c7-102">SYNOPSIS</span></span>
<span data-ttu-id="c22c7-103">Cria uma política de firewall de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c22c7-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="c22c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c22c7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c22c7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c22c7-105">DESCRIPTION</span></span>
<span data-ttu-id="c22c7-106">O cmdlet **New-AzApplicationGatewayFirewallPolicy** cria uma política de firewall de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c22c7-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="c22c7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c22c7-107">EXAMPLES</span></span>

### <span data-ttu-id="c22c7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c22c7-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="c22c7-109">Este comando cria uma nova política de firewall de gateway de aplicativo do Azure chamada "wafResource1" no grupo de recursos "rg1" no local "westus" com regras personalizadas definidas na variável $customRule</span><span class="sxs-lookup"><span data-stu-id="c22c7-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="c22c7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c22c7-110">PARAMETERS</span></span>

### <span data-ttu-id="c22c7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c22c7-111">-AsJob</span></span>
<span data-ttu-id="c22c7-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c22c7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c22c7-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="c22c7-113">-CustomRule</span></span>
<span data-ttu-id="c22c7-114">A lista de CustomRules</span><span class="sxs-lookup"><span data-stu-id="c22c7-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22c7-115">-DefaultProfile</span></span>
<span data-ttu-id="c22c7-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c22c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c22c7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c22c7-117">-Force</span></span>
<span data-ttu-id="c22c7-118">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="c22c7-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c22c7-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c22c7-119">-Location</span></span>
<span data-ttu-id="c22c7-120">location.</span><span class="sxs-lookup"><span data-stu-id="c22c7-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22c7-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="c22c7-121">-ManagedRule</span></span>
<span data-ttu-id="c22c7-122">Configuração de Regra Gerenciada</span><span class="sxs-lookup"><span data-stu-id="c22c7-122">Managed Rule Setting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22c7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c22c7-123">-Name</span></span>
<span data-ttu-id="c22c7-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c22c7-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22c7-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="c22c7-125">-PolicySetting</span></span>
<span data-ttu-id="c22c7-126">Configurações de Política para Firewall de Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="c22c7-126">Policy Settings for Web Application Firewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22c7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c22c7-127">-ResourceGroupName</span></span>
<span data-ttu-id="c22c7-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c22c7-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22c7-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="c22c7-129">-Tag</span></span>
<span data-ttu-id="c22c7-130">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="c22c7-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22c7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c22c7-131">-Confirm</span></span>
<span data-ttu-id="c22c7-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c22c7-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22c7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c22c7-133">-WhatIf</span></span>
<span data-ttu-id="c22c7-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c22c7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c22c7-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c22c7-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22c7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22c7-136">CommonParameters</span></span>
<span data-ttu-id="c22c7-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c22c7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22c7-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c22c7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22c7-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c22c7-139">INPUTS</span></span>

### <span data-ttu-id="c22c7-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c22c7-140">System.String</span></span>

### <span data-ttu-id="c22c7-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span><span class="sxs-lookup"><span data-stu-id="c22c7-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="c22c7-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="c22c7-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="c22c7-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="c22c7-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="c22c7-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c22c7-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c22c7-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c22c7-145">OUTPUTS</span></span>

### <span data-ttu-id="c22c7-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c22c7-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="c22c7-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="c22c7-147">NOTES</span></span>

## <span data-ttu-id="c22c7-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c22c7-148">RELATED LINKS</span></span>
