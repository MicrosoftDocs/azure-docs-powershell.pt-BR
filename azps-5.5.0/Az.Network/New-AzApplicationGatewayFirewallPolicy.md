---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113490"
---
# <span data-ttu-id="98366-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="98366-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="98366-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98366-102">SYNOPSIS</span></span>
<span data-ttu-id="98366-103">Cria uma política de firewall do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="98366-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="98366-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98366-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98366-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="98366-105">DESCRIPTION</span></span>
<span data-ttu-id="98366-106">O **cmdlet New-AzApplicationGatewayFirewallPolicy** cria uma política de firewall do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="98366-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="98366-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="98366-107">EXAMPLES</span></span>

### <span data-ttu-id="98366-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98366-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="98366-109">Este comando cria uma nova política de firewall do gateway de aplicativo do Azure chamada "wafResource1" no grupo de recursos "rg1" no local "westus" com regras personalizadas definidas na variável $customRule</span><span class="sxs-lookup"><span data-stu-id="98366-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="98366-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98366-110">PARAMETERS</span></span>

### <span data-ttu-id="98366-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98366-111">-AsJob</span></span>
<span data-ttu-id="98366-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="98366-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98366-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="98366-113">-CustomRule</span></span>
<span data-ttu-id="98366-114">A lista de CustomRules</span><span class="sxs-lookup"><span data-stu-id="98366-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="98366-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98366-115">-DefaultProfile</span></span>
<span data-ttu-id="98366-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98366-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98366-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="98366-117">-Force</span></span>
<span data-ttu-id="98366-118">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="98366-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="98366-119">-Local</span><span class="sxs-lookup"><span data-stu-id="98366-119">-Location</span></span>
<span data-ttu-id="98366-120">Localização.</span><span class="sxs-lookup"><span data-stu-id="98366-120">location.</span></span>

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

### <span data-ttu-id="98366-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="98366-121">-ManagedRule</span></span>
<span data-ttu-id="98366-122">Configuração de Regra Gerenciada</span><span class="sxs-lookup"><span data-stu-id="98366-122">Managed Rule Setting</span></span>

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

### <span data-ttu-id="98366-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="98366-123">-Name</span></span>
<span data-ttu-id="98366-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="98366-124">The resource name.</span></span>

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

### <span data-ttu-id="98366-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="98366-125">-PolicySetting</span></span>
<span data-ttu-id="98366-126">Configurações de Política para Firewall do Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="98366-126">Policy Settings for Web Application Firewall</span></span>

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

### <span data-ttu-id="98366-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98366-127">-ResourceGroupName</span></span>
<span data-ttu-id="98366-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="98366-128">The resource group name.</span></span>

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

### <span data-ttu-id="98366-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="98366-129">-Tag</span></span>
<span data-ttu-id="98366-130">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="98366-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="98366-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="98366-131">-Confirm</span></span>
<span data-ttu-id="98366-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98366-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98366-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98366-133">-WhatIf</span></span>
<span data-ttu-id="98366-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="98366-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98366-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98366-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98366-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98366-136">CommonParameters</span></span>
<span data-ttu-id="98366-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98366-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98366-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98366-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98366-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="98366-139">INPUTS</span></span>

### <span data-ttu-id="98366-140">System.String</span><span class="sxs-lookup"><span data-stu-id="98366-140">System.String</span></span>

### <span data-ttu-id="98366-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span><span class="sxs-lookup"><span data-stu-id="98366-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="98366-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="98366-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="98366-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="98366-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="98366-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="98366-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="98366-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="98366-145">OUTPUTS</span></span>

### <span data-ttu-id="98366-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="98366-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="98366-147">Notas</span><span class="sxs-lookup"><span data-stu-id="98366-147">NOTES</span></span>

## <span data-ttu-id="98366-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98366-148">RELATED LINKS</span></span>
