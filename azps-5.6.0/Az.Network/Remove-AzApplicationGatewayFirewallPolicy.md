---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 2d7bdd9a1669859f0bcd650577ed3169a0aeea2e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890601"
---
# <span data-ttu-id="009c9-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="009c9-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="009c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="009c9-102">SYNOPSIS</span></span>
<span data-ttu-id="009c9-103">Remove uma política de firewall de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="009c9-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="009c9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="009c9-104">SYNTAX</span></span>

### <span data-ttu-id="009c9-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="009c9-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="009c9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="009c9-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="009c9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="009c9-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="009c9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="009c9-108">DESCRIPTION</span></span>
<span data-ttu-id="009c9-109">O cmdlet **Remove-AzApplicationGatewayFirewallPolicy** remove uma política de firewall de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="009c9-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="009c9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="009c9-110">EXAMPLES</span></span>

### <span data-ttu-id="009c9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="009c9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="009c9-112">Este comando remove a política de firewall do gateway de aplicativo chamada ApplicationGatewayFirewallPolicy01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="009c9-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="009c9-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="009c9-113">PARAMETERS</span></span>

### <span data-ttu-id="009c9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="009c9-114">-AsJob</span></span>
<span data-ttu-id="009c9-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="009c9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="009c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="009c9-116">-DefaultProfile</span></span>
<span data-ttu-id="009c9-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="009c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="009c9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="009c9-118">-Force</span></span>
<span data-ttu-id="009c9-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="009c9-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="009c9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="009c9-120">-InputObject</span></span>
<span data-ttu-id="009c9-121">O objeto de política de firewall</span><span class="sxs-lookup"><span data-stu-id="009c9-121">The firewall policy object</span></span>

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

### <span data-ttu-id="009c9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="009c9-122">-Name</span></span>
<span data-ttu-id="009c9-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="009c9-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="009c9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="009c9-124">-PassThru</span></span>
<span data-ttu-id="009c9-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="009c9-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="009c9-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="009c9-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="009c9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="009c9-127">-ResourceGroupName</span></span>
<span data-ttu-id="009c9-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="009c9-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="009c9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="009c9-129">-ResourceId</span></span>
<span data-ttu-id="009c9-130">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="009c9-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="009c9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="009c9-131">-Confirm</span></span>
<span data-ttu-id="009c9-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="009c9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="009c9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="009c9-133">-WhatIf</span></span>
<span data-ttu-id="009c9-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="009c9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="009c9-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="009c9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="009c9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="009c9-136">CommonParameters</span></span>
<span data-ttu-id="009c9-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="009c9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="009c9-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="009c9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="009c9-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="009c9-139">INPUTS</span></span>

### <span data-ttu-id="009c9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="009c9-140">System.String</span></span>

## <span data-ttu-id="009c9-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="009c9-141">OUTPUTS</span></span>

### <span data-ttu-id="009c9-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="009c9-142">System.Boolean</span></span>

## <span data-ttu-id="009c9-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="009c9-143">NOTES</span></span>

## <span data-ttu-id="009c9-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="009c9-144">RELATED LINKS</span></span>
