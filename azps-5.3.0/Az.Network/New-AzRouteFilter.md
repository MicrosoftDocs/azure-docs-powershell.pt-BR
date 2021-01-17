---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 8be04cd9e483e990d73130866779710bbed879bb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427543"
---
# <span data-ttu-id="15234-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="15234-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="15234-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15234-102">SYNOPSIS</span></span>
<span data-ttu-id="15234-103">Cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="15234-103">Creates a route filter.</span></span>

## <span data-ttu-id="15234-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15234-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15234-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15234-105">DESCRIPTION</span></span>
<span data-ttu-id="15234-106">O cmdlet New-AzRouteFilter cria um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="15234-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="15234-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15234-107">EXAMPLES</span></span>

### <span data-ttu-id="15234-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="15234-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="15234-109">O comando cria um novo filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="15234-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="15234-110">OS</span><span class="sxs-lookup"><span data-stu-id="15234-110">PARAMETERS</span></span>

### <span data-ttu-id="15234-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15234-111">-AsJob</span></span>
<span data-ttu-id="15234-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="15234-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15234-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15234-113">-DefaultProfile</span></span>
<span data-ttu-id="15234-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15234-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15234-115">-Force</span><span class="sxs-lookup"><span data-stu-id="15234-115">-Force</span></span>
<span data-ttu-id="15234-116">Indica que esse cmdlet cria uma tabela de rota mesmo que um filtro de rota com o mesmo nome já exista.</span><span class="sxs-lookup"><span data-stu-id="15234-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="15234-117">-Local</span><span class="sxs-lookup"><span data-stu-id="15234-117">-Location</span></span>
<span data-ttu-id="15234-118">Especifica a região do Azure na qual esse cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="15234-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="15234-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="15234-119">-Name</span></span>
<span data-ttu-id="15234-120">Especifica um nome para o filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="15234-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="15234-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15234-121">-ResourceGroupName</span></span>
<span data-ttu-id="15234-122">Especifica o nome do grupo de recursos em que esse cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="15234-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="15234-123">-Regra</span><span class="sxs-lookup"><span data-stu-id="15234-123">-Rule</span></span>
<span data-ttu-id="15234-124">Especifica uma matriz de objetos de regra de filtro de rota para associar ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="15234-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15234-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="15234-125">-Tag</span></span>
<span data-ttu-id="15234-126">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="15234-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="15234-127">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="15234-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="15234-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="15234-128">-Confirm</span></span>
<span data-ttu-id="15234-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15234-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15234-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15234-130">-WhatIf</span></span>
<span data-ttu-id="15234-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15234-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15234-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15234-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15234-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15234-133">CommonParameters</span></span>
<span data-ttu-id="15234-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15234-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15234-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15234-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15234-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15234-136">INPUTS</span></span>

### <span data-ttu-id="15234-137">System. String</span><span class="sxs-lookup"><span data-stu-id="15234-137">System.String</span></span>

### <span data-ttu-id="15234-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule []</span><span class="sxs-lookup"><span data-stu-id="15234-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="15234-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="15234-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="15234-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15234-140">OUTPUTS</span></span>

### <span data-ttu-id="15234-141">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="15234-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="15234-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15234-142">NOTES</span></span>
<span data-ttu-id="15234-143">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="15234-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="15234-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15234-144">RELATED LINKS</span></span>

[<span data-ttu-id="15234-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="15234-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="15234-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="15234-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="15234-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="15234-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="15234-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15234-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="15234-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15234-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="15234-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15234-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="15234-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15234-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="15234-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15234-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
