---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117363"
---
# <span data-ttu-id="1f156-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1f156-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="1f156-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f156-102">SYNOPSIS</span></span>
<span data-ttu-id="1f156-103">Remove uma política de firewall do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1f156-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="1f156-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f156-104">SYNTAX</span></span>

### <span data-ttu-id="1f156-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="1f156-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f156-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1f156-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f156-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f156-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f156-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f156-108">DESCRIPTION</span></span>
<span data-ttu-id="1f156-109">O cmdlet **Remove-AzApplicationGatewayFirewallPolicy** remove uma política de firewall do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1f156-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="1f156-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f156-110">EXAMPLES</span></span>

### <span data-ttu-id="1f156-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f156-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1f156-112">Esse comando remove a política de firewall do gateway de aplicativo chamada ApplicationGatewayFirewallPolicy01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="1f156-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="1f156-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f156-113">PARAMETERS</span></span>

### <span data-ttu-id="1f156-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f156-114">-AsJob</span></span>
<span data-ttu-id="1f156-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1f156-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f156-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f156-116">-DefaultProfile</span></span>
<span data-ttu-id="1f156-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f156-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f156-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1f156-118">-Force</span></span>
<span data-ttu-id="1f156-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="1f156-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1f156-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f156-120">-InputObject</span></span>
<span data-ttu-id="1f156-121">O objeto de política de firewall</span><span class="sxs-lookup"><span data-stu-id="1f156-121">The firewall policy object</span></span>

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

### <span data-ttu-id="1f156-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f156-122">-Name</span></span>
<span data-ttu-id="1f156-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1f156-123">The resource name.</span></span>

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

### <span data-ttu-id="1f156-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f156-124">-PassThru</span></span>
<span data-ttu-id="1f156-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="1f156-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f156-126">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="1f156-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f156-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f156-127">-ResourceGroupName</span></span>
<span data-ttu-id="1f156-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f156-128">The resource group name.</span></span>

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

### <span data-ttu-id="1f156-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f156-129">-ResourceId</span></span>
<span data-ttu-id="1f156-130">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="1f156-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1f156-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1f156-131">-Confirm</span></span>
<span data-ttu-id="1f156-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f156-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f156-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f156-133">-WhatIf</span></span>
<span data-ttu-id="1f156-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1f156-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f156-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f156-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f156-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f156-136">CommonParameters</span></span>
<span data-ttu-id="1f156-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f156-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f156-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f156-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f156-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="1f156-139">INPUTS</span></span>

### <span data-ttu-id="1f156-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1f156-140">System.String</span></span>

## <span data-ttu-id="1f156-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="1f156-141">OUTPUTS</span></span>

### <span data-ttu-id="1f156-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f156-142">System.Boolean</span></span>

## <span data-ttu-id="1f156-143">Notas</span><span class="sxs-lookup"><span data-stu-id="1f156-143">NOTES</span></span>

## <span data-ttu-id="1f156-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f156-144">RELATED LINKS</span></span>
