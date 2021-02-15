---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 8be04cd9e483e990d73130866779710bbed879bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117383"
---
# <span data-ttu-id="a1495-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a1495-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="a1495-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1495-102">SYNOPSIS</span></span>
<span data-ttu-id="a1495-103">Cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="a1495-103">Creates a route filter.</span></span>

## <span data-ttu-id="a1495-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1495-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1495-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1495-105">DESCRIPTION</span></span>
<span data-ttu-id="a1495-106">O New-AzRouteFilter cmdlet cria um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1495-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="a1495-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1495-107">EXAMPLES</span></span>

### <span data-ttu-id="a1495-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1495-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="a1495-109">O comando cria um novo filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="a1495-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="a1495-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1495-110">PARAMETERS</span></span>

### <span data-ttu-id="a1495-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1495-111">-AsJob</span></span>
<span data-ttu-id="a1495-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a1495-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1495-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1495-113">-DefaultProfile</span></span>
<span data-ttu-id="a1495-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a1495-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1495-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a1495-115">-Force</span></span>
<span data-ttu-id="a1495-116">Indica que esse cmdlet cria uma tabela de rota mesmo que já exista um filtro de rota com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="a1495-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="a1495-117">-Local</span><span class="sxs-lookup"><span data-stu-id="a1495-117">-Location</span></span>
<span data-ttu-id="a1495-118">Especifica a região do Azure na qual este cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="a1495-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="a1495-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1495-119">-Name</span></span>
<span data-ttu-id="a1495-120">Especifica um nome para o filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="a1495-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="a1495-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1495-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1495-122">Especifica o nome do grupo de recursos no qual este cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="a1495-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="a1495-123">-Regra</span><span class="sxs-lookup"><span data-stu-id="a1495-123">-Rule</span></span>
<span data-ttu-id="a1495-124">Especifica uma matriz de objetos de Regra de Filtro de Rota para associar ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="a1495-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="a1495-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1495-125">-Tag</span></span>
<span data-ttu-id="a1495-126">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a1495-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a1495-127">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a1495-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a1495-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a1495-128">-Confirm</span></span>
<span data-ttu-id="a1495-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1495-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1495-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1495-130">-WhatIf</span></span>
<span data-ttu-id="a1495-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a1495-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1495-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1495-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1495-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1495-133">CommonParameters</span></span>
<span data-ttu-id="a1495-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1495-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1495-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1495-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1495-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="a1495-136">INPUTS</span></span>

### <span data-ttu-id="a1495-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a1495-137">System.String</span></span>

### <span data-ttu-id="a1495-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span><span class="sxs-lookup"><span data-stu-id="a1495-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="a1495-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a1495-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a1495-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="a1495-140">OUTPUTS</span></span>

### <span data-ttu-id="a1495-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a1495-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="a1495-142">Notas</span><span class="sxs-lookup"><span data-stu-id="a1495-142">NOTES</span></span>
<span data-ttu-id="a1495-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="a1495-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a1495-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1495-144">RELATED LINKS</span></span>

[<span data-ttu-id="a1495-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a1495-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="a1495-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a1495-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="a1495-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a1495-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="a1495-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1495-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a1495-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1495-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a1495-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1495-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a1495-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1495-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a1495-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1495-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
