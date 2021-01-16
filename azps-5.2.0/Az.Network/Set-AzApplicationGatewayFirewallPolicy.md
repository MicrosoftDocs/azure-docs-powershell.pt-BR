---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261349"
---
# <span data-ttu-id="1ec00-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1ec00-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="1ec00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ec00-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec00-103">Atualiza uma política de firewall do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1ec00-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="1ec00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ec00-104">SYNTAX</span></span>

### <span data-ttu-id="1ec00-105">ByFactoryObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ec00-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ec00-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="1ec00-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ec00-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ec00-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ec00-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ec00-108">DESCRIPTION</span></span>
<span data-ttu-id="1ec00-109">O cmdlet **set-AzApplicationGatewayFirewallPolicy** atualiza uma política de firewall do Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1ec00-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="1ec00-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ec00-110">EXAMPLES</span></span>

### <span data-ttu-id="1ec00-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ec00-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="1ec00-112">Esse comando atualiza a política de firewall do gateway do aplicativo com configurações na variável $AppGwFirewallPolicy e armazena o gateway atualizado na variável $UpdatedAppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="1ec00-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="1ec00-113">OS</span><span class="sxs-lookup"><span data-stu-id="1ec00-113">PARAMETERS</span></span>

### <span data-ttu-id="1ec00-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ec00-114">-AsJob</span></span>
<span data-ttu-id="1ec00-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1ec00-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ec00-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="1ec00-116">-CustomRule</span></span>
<span data-ttu-id="1ec00-117">A lista de CustomRules</span><span class="sxs-lookup"><span data-stu-id="1ec00-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="1ec00-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec00-118">-DefaultProfile</span></span>
<span data-ttu-id="1ec00-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec00-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ec00-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ec00-120">-InputObject</span></span>
<span data-ttu-id="1ec00-121">O applicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1ec00-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="1ec00-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="1ec00-122">-ManagedRule</span></span>
<span data-ttu-id="1ec00-123">ManagedRules da política de firewall</span><span class="sxs-lookup"><span data-stu-id="1ec00-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="1ec00-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ec00-124">-Name</span></span>
<span data-ttu-id="1ec00-125">O nome da política de firewall.</span><span class="sxs-lookup"><span data-stu-id="1ec00-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="1ec00-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="1ec00-126">-PolicySetting</span></span>
<span data-ttu-id="1ec00-127">Policysettings da política de firewall</span><span class="sxs-lookup"><span data-stu-id="1ec00-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="1ec00-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec00-128">-ResourceGroupName</span></span>
<span data-ttu-id="1ec00-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ec00-129">The resource group name.</span></span>

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

### <span data-ttu-id="1ec00-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ec00-130">-ResourceId</span></span>
<span data-ttu-id="1ec00-131">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec00-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1ec00-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ec00-132">-Confirm</span></span>
<span data-ttu-id="1ec00-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec00-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec00-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec00-134">-WhatIf</span></span>
<span data-ttu-id="1ec00-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ec00-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ec00-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ec00-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec00-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec00-137">CommonParameters</span></span>
<span data-ttu-id="1ec00-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec00-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec00-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ec00-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec00-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ec00-140">INPUTS</span></span>

### <span data-ttu-id="1ec00-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1ec00-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="1ec00-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ec00-142">OUTPUTS</span></span>

### <span data-ttu-id="1ec00-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1ec00-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="1ec00-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ec00-144">NOTES</span></span>

## <span data-ttu-id="1ec00-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ec00-145">RELATED LINKS</span></span>
