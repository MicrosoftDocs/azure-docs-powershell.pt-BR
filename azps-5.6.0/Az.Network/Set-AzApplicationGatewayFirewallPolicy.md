---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e6b9c873110118392e9380418276bfa0f4d938a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889099"
---
# <span data-ttu-id="7cf52-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf52-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="7cf52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cf52-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf52-103">Atualiza uma política de firewall de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7cf52-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="7cf52-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7cf52-104">SYNTAX</span></span>

### <span data-ttu-id="7cf52-105">ByFactoryObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7cf52-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf52-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="7cf52-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf52-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf52-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf52-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7cf52-108">DESCRIPTION</span></span>
<span data-ttu-id="7cf52-109">O cmdlet **Set-AzApplicationGatewayFirewallPolicy** atualiza uma política de firewall de gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf52-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="7cf52-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cf52-110">EXAMPLES</span></span>

### <span data-ttu-id="7cf52-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7cf52-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="7cf52-112">Esse comando atualiza a política de firewall do gateway de aplicativo com configurações na variável $AppGwFirewallPolicy e armazena o gateway atualizado na variável $UpdatedAppGwFirewallPolicy de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7cf52-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="7cf52-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7cf52-113">PARAMETERS</span></span>

### <span data-ttu-id="7cf52-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cf52-114">-AsJob</span></span>
<span data-ttu-id="7cf52-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7cf52-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7cf52-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="7cf52-116">-CustomRule</span></span>
<span data-ttu-id="7cf52-117">A lista de CustomRules</span><span class="sxs-lookup"><span data-stu-id="7cf52-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="7cf52-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf52-118">-DefaultProfile</span></span>
<span data-ttu-id="7cf52-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf52-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cf52-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cf52-120">-InputObject</span></span>
<span data-ttu-id="7cf52-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf52-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf52-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="7cf52-122">-ManagedRule</span></span>
<span data-ttu-id="7cf52-123">ManagedRules da política de firewall</span><span class="sxs-lookup"><span data-stu-id="7cf52-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="7cf52-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7cf52-124">-Name</span></span>
<span data-ttu-id="7cf52-125">O Nome da Política de Firewall.</span><span class="sxs-lookup"><span data-stu-id="7cf52-125">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf52-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="7cf52-126">-PolicySetting</span></span>
<span data-ttu-id="7cf52-127">Policysettings of the firewall policy</span><span class="sxs-lookup"><span data-stu-id="7cf52-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="7cf52-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf52-128">-ResourceGroupName</span></span>
<span data-ttu-id="7cf52-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7cf52-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf52-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf52-130">-ResourceId</span></span>
<span data-ttu-id="7cf52-131">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf52-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf52-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cf52-132">-Confirm</span></span>
<span data-ttu-id="7cf52-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf52-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf52-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf52-134">-WhatIf</span></span>
<span data-ttu-id="7cf52-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7cf52-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cf52-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7cf52-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf52-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf52-137">CommonParameters</span></span>
<span data-ttu-id="7cf52-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf52-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf52-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cf52-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf52-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cf52-140">INPUTS</span></span>

### <span data-ttu-id="7cf52-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf52-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="7cf52-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7cf52-142">OUTPUTS</span></span>

### <span data-ttu-id="7cf52-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf52-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="7cf52-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="7cf52-144">NOTES</span></span>

## <span data-ttu-id="7cf52-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cf52-145">RELATED LINKS</span></span>
