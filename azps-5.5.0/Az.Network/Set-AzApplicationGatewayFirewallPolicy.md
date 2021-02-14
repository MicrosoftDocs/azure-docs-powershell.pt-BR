---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117329"
---
# <span data-ttu-id="fff81-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fff81-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="fff81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fff81-102">SYNOPSIS</span></span>
<span data-ttu-id="fff81-103">Atualiza uma política de firewall do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fff81-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="fff81-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fff81-104">SYNTAX</span></span>

### <span data-ttu-id="fff81-105">ByFactoryObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fff81-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fff81-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="fff81-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fff81-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fff81-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fff81-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fff81-108">DESCRIPTION</span></span>
<span data-ttu-id="fff81-109">O cmdlet **Set-AzApplicationGatewayFirewallPolicy** atualiza uma política de firewall do gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="fff81-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="fff81-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fff81-110">EXAMPLES</span></span>

### <span data-ttu-id="fff81-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fff81-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="fff81-112">Esse comando atualiza a política de firewall do gateway de aplicativo com configurações na variável $AppGwFirewallPolicy e armazena o gateway atualizado na variável $UpdatedAppGwFirewallPolicy aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fff81-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="fff81-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fff81-113">PARAMETERS</span></span>

### <span data-ttu-id="fff81-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fff81-114">-AsJob</span></span>
<span data-ttu-id="fff81-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fff81-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fff81-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="fff81-116">-CustomRule</span></span>
<span data-ttu-id="fff81-117">A lista de CustomRules</span><span class="sxs-lookup"><span data-stu-id="fff81-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="fff81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff81-118">-DefaultProfile</span></span>
<span data-ttu-id="fff81-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fff81-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fff81-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fff81-120">-InputObject</span></span>
<span data-ttu-id="fff81-121">O aplicativoGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fff81-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="fff81-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="fff81-122">-ManagedRule</span></span>
<span data-ttu-id="fff81-123">ManagedRules da política de firewall</span><span class="sxs-lookup"><span data-stu-id="fff81-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="fff81-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="fff81-124">-Name</span></span>
<span data-ttu-id="fff81-125">O Nome da Política de Firewall.</span><span class="sxs-lookup"><span data-stu-id="fff81-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="fff81-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="fff81-126">-PolicySetting</span></span>
<span data-ttu-id="fff81-127">Configurações de política da política de firewall</span><span class="sxs-lookup"><span data-stu-id="fff81-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="fff81-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fff81-128">-ResourceGroupName</span></span>
<span data-ttu-id="fff81-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fff81-129">The resource group name.</span></span>

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

### <span data-ttu-id="fff81-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fff81-130">-ResourceId</span></span>
<span data-ttu-id="fff81-131">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="fff81-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fff81-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fff81-132">-Confirm</span></span>
<span data-ttu-id="fff81-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fff81-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fff81-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fff81-134">-WhatIf</span></span>
<span data-ttu-id="fff81-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fff81-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fff81-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fff81-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fff81-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff81-137">CommonParameters</span></span>
<span data-ttu-id="fff81-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff81-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff81-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fff81-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff81-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="fff81-140">INPUTS</span></span>

### <span data-ttu-id="fff81-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fff81-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="fff81-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="fff81-142">OUTPUTS</span></span>

### <span data-ttu-id="fff81-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="fff81-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="fff81-144">Notas</span><span class="sxs-lookup"><span data-stu-id="fff81-144">NOTES</span></span>

## <span data-ttu-id="fff81-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fff81-145">RELATED LINKS</span></span>
