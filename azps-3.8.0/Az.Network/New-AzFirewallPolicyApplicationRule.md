---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 1b9fd10e11cb283f880979e7e4a5d703521c9a87
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777217"
---
# <span data-ttu-id="6f2ba-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="6f2ba-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="6f2ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f2ba-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2ba-103">Criar uma nova regra de aplicativo da política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="6f2ba-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="6f2ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f2ba-104">SYNTAX</span></span>

### <span data-ttu-id="6f2ba-105">TargetFqdn (padrão)</span><span class="sxs-lookup"><span data-stu-id="6f2ba-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f2ba-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="6f2ba-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f2ba-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f2ba-107">DESCRIPTION</span></span>
<span data-ttu-id="6f2ba-108">O cmdlet **New-AzFirewallPolicyApplicationRule** cria uma regra de aplicativo para uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2ba-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="6f2ba-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f2ba-109">EXAMPLES</span></span>

### <span data-ttu-id="6f2ba-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f2ba-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="6f2ba-111">Este exemplo cria uma regra de aplicativo com o endereço de origem, o protocolo e os FQDNs de destino.</span><span class="sxs-lookup"><span data-stu-id="6f2ba-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

## <span data-ttu-id="6f2ba-112">OS</span><span class="sxs-lookup"><span data-stu-id="6f2ba-112">PARAMETERS</span></span>

### <span data-ttu-id="6f2ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f2ba-113">-DefaultProfile</span></span>
<span data-ttu-id="6f2ba-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2ba-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6f2ba-115">-Description</span></span>
<span data-ttu-id="6f2ba-116">A descrição da regra</span><span class="sxs-lookup"><span data-stu-id="6f2ba-116">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2ba-117">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="6f2ba-117">-FqdnTag</span></span>
<span data-ttu-id="6f2ba-118">As marcas de FQDN da regra</span><span class="sxs-lookup"><span data-stu-id="6f2ba-118">The FQDN Tags of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2ba-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f2ba-119">-Name</span></span>
<span data-ttu-id="6f2ba-120">O nome da regra do aplicativo</span><span class="sxs-lookup"><span data-stu-id="6f2ba-120">The name of the Application Rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2ba-121">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="6f2ba-121">-Protocol</span></span>
<span data-ttu-id="6f2ba-122">Os protocolos da regra</span><span class="sxs-lookup"><span data-stu-id="6f2ba-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2ba-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="6f2ba-123">-SourceAddress</span></span>
<span data-ttu-id="6f2ba-124">Os endereços de origem da regra</span><span class="sxs-lookup"><span data-stu-id="6f2ba-124">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2ba-125">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="6f2ba-125">-TargetFqdn</span></span>
<span data-ttu-id="6f2ba-126">Os FQDNs de destino da regra</span><span class="sxs-lookup"><span data-stu-id="6f2ba-126">The target FQDNs of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2ba-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6f2ba-127">-Confirm</span></span>
<span data-ttu-id="6f2ba-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f2ba-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2ba-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f2ba-129">-WhatIf</span></span>
<span data-ttu-id="6f2ba-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6f2ba-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f2ba-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6f2ba-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2ba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2ba-132">CommonParameters</span></span>
<span data-ttu-id="6f2ba-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f2ba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2ba-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f2ba-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2ba-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f2ba-135">INPUTS</span></span>

### <span data-ttu-id="6f2ba-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6f2ba-136">None</span></span>

## <span data-ttu-id="6f2ba-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f2ba-137">OUTPUTS</span></span>

### <span data-ttu-id="6f2ba-138">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="6f2ba-138">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="6f2ba-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f2ba-139">NOTES</span></span>

## <span data-ttu-id="6f2ba-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f2ba-140">RELATED LINKS</span></span>
