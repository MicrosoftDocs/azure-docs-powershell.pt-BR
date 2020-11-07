---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 58800beae60292029a7a9b3245f274355c887a5b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772312"
---
# <span data-ttu-id="dd032-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="dd032-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="dd032-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd032-102">SYNOPSIS</span></span>
<span data-ttu-id="dd032-103">Remove uma política de firewall do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dd032-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="dd032-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd032-104">SYNTAX</span></span>

### <span data-ttu-id="dd032-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="dd032-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd032-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dd032-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd032-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd032-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd032-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd032-108">DESCRIPTION</span></span>
<span data-ttu-id="dd032-109">O cmdlet **Remove-AzApplicationGatewayFirewallPolicy** remove uma política de firewall do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dd032-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="dd032-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd032-110">EXAMPLES</span></span>

### <span data-ttu-id="dd032-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd032-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dd032-112">Esse comando Remove a política de firewall do gateway do aplicativo chamada ApplicationGatewayFirewallPolicy01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="dd032-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="dd032-113">OS</span><span class="sxs-lookup"><span data-stu-id="dd032-113">PARAMETERS</span></span>

### <span data-ttu-id="dd032-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd032-114">-AsJob</span></span>
<span data-ttu-id="dd032-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dd032-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd032-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd032-116">-DefaultProfile</span></span>
<span data-ttu-id="dd032-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd032-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd032-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dd032-118">-Force</span></span>
<span data-ttu-id="dd032-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="dd032-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dd032-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd032-120">-InputObject</span></span>
<span data-ttu-id="dd032-121">O objeto de política de firewall</span><span class="sxs-lookup"><span data-stu-id="dd032-121">The firewall policy object</span></span>

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

### <span data-ttu-id="dd032-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd032-122">-Name</span></span>
<span data-ttu-id="dd032-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="dd032-123">The resource name.</span></span>

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

### <span data-ttu-id="dd032-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd032-124">-PassThru</span></span>
<span data-ttu-id="dd032-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="dd032-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dd032-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="dd032-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dd032-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd032-127">-ResourceGroupName</span></span>
<span data-ttu-id="dd032-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd032-128">The resource group name.</span></span>

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

### <span data-ttu-id="dd032-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd032-129">-ResourceId</span></span>
<span data-ttu-id="dd032-130">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd032-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="dd032-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd032-131">-Confirm</span></span>
<span data-ttu-id="dd032-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd032-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd032-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd032-133">-WhatIf</span></span>
<span data-ttu-id="dd032-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd032-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd032-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd032-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd032-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd032-136">CommonParameters</span></span>
<span data-ttu-id="dd032-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd032-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd032-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd032-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd032-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd032-139">INPUTS</span></span>

### <span data-ttu-id="dd032-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dd032-140">System.String</span></span>

## <span data-ttu-id="dd032-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd032-141">OUTPUTS</span></span>

### <span data-ttu-id="dd032-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd032-142">System.Boolean</span></span>

## <span data-ttu-id="dd032-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd032-143">NOTES</span></span>

## <span data-ttu-id="dd032-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd032-144">RELATED LINKS</span></span>