---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 6813bf30da73f09f285151d6d309eb89b32acbb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600412"
---
# <span data-ttu-id="db29c-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="db29c-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="db29c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db29c-102">SYNOPSIS</span></span>
<span data-ttu-id="db29c-103">Cria uma política de firewall do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="db29c-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="db29c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db29c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db29c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db29c-105">DESCRIPTION</span></span>
<span data-ttu-id="db29c-106">O cmdlet **New-AzApplicationGatewayFirewallPolicy** cria uma política de firewall do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="db29c-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="db29c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db29c-107">EXAMPLES</span></span>

### <span data-ttu-id="db29c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db29c-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzureRmApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="db29c-109">Esse comando cria uma nova política de firewall do aplicativo gateway do Azure chamada "wafResource1" no grupo de recursos "Rg1" no local "oesteus" com as regras personalizadas definidas na variável $customRule</span><span class="sxs-lookup"><span data-stu-id="db29c-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="db29c-110">OS</span><span class="sxs-lookup"><span data-stu-id="db29c-110">PARAMETERS</span></span>

### <span data-ttu-id="db29c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db29c-111">-AsJob</span></span>
<span data-ttu-id="db29c-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="db29c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db29c-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="db29c-113">-CustomRule</span></span>
<span data-ttu-id="db29c-114">A lista de CustomRules</span><span class="sxs-lookup"><span data-stu-id="db29c-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="db29c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db29c-115">-DefaultProfile</span></span>
<span data-ttu-id="db29c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db29c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db29c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="db29c-117">-Force</span></span>
<span data-ttu-id="db29c-118">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="db29c-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="db29c-119">-Local</span><span class="sxs-lookup"><span data-stu-id="db29c-119">-Location</span></span>
<span data-ttu-id="db29c-120">ponto.</span><span class="sxs-lookup"><span data-stu-id="db29c-120">location.</span></span>

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

### <span data-ttu-id="db29c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="db29c-121">-Name</span></span>
<span data-ttu-id="db29c-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="db29c-122">The resource name.</span></span>

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

### <span data-ttu-id="db29c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db29c-123">-ResourceGroupName</span></span>
<span data-ttu-id="db29c-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="db29c-124">The resource group name.</span></span>

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

### <span data-ttu-id="db29c-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="db29c-125">-Tag</span></span>
<span data-ttu-id="db29c-126">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="db29c-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="db29c-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db29c-127">-Confirm</span></span>
<span data-ttu-id="db29c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db29c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db29c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db29c-129">-WhatIf</span></span>
<span data-ttu-id="db29c-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db29c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db29c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db29c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db29c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db29c-132">CommonParameters</span></span>
<span data-ttu-id="db29c-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db29c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db29c-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db29c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db29c-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db29c-135">INPUTS</span></span>

### <span data-ttu-id="db29c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="db29c-136">System.String</span></span>

### <span data-ttu-id="db29c-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="db29c-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="db29c-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="db29c-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="db29c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db29c-139">OUTPUTS</span></span>

### <span data-ttu-id="db29c-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="db29c-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="db29c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db29c-141">NOTES</span></span>

## <span data-ttu-id="db29c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db29c-142">RELATED LINKS</span></span>
