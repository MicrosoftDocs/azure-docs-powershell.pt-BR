---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 9a262bd5680a9d5cd89d5ec32e3a57edbdaf60f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889178"
---
# <span data-ttu-id="f420a-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f420a-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="f420a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f420a-102">SYNOPSIS</span></span>
<span data-ttu-id="f420a-103">Cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="f420a-103">Creates a route filter.</span></span>

## <span data-ttu-id="f420a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f420a-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f420a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f420a-105">DESCRIPTION</span></span>
<span data-ttu-id="f420a-106">O New-AzRouteFilter cmdlet cria um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="f420a-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="f420a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f420a-107">EXAMPLES</span></span>

### <span data-ttu-id="f420a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f420a-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="f420a-109">O comando cria um novo filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="f420a-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="f420a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f420a-110">PARAMETERS</span></span>

### <span data-ttu-id="f420a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f420a-111">-AsJob</span></span>
<span data-ttu-id="f420a-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f420a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f420a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f420a-113">-DefaultProfile</span></span>
<span data-ttu-id="f420a-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f420a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f420a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f420a-115">-Force</span></span>
<span data-ttu-id="f420a-116">Indica que esse cmdlet cria uma tabela de rota mesmo que um filtro de rota que já tenha o mesmo nome já exista.</span><span class="sxs-lookup"><span data-stu-id="f420a-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="f420a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="f420a-117">-Location</span></span>
<span data-ttu-id="f420a-118">Especifica a região do Azure na qual este cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="f420a-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="f420a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f420a-119">-Name</span></span>
<span data-ttu-id="f420a-120">Especifica um nome para o filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="f420a-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="f420a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f420a-121">-ResourceGroupName</span></span>
<span data-ttu-id="f420a-122">Especifica o nome do grupo de recursos no qual esse cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="f420a-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="f420a-123">-Rule</span><span class="sxs-lookup"><span data-stu-id="f420a-123">-Rule</span></span>
<span data-ttu-id="f420a-124">Especifica uma matriz de objetos Route Filter Rule para associar ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="f420a-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="f420a-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f420a-125">-Tag</span></span>
<span data-ttu-id="f420a-126">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f420a-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f420a-127">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f420a-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f420a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f420a-128">-Confirm</span></span>
<span data-ttu-id="f420a-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f420a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f420a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f420a-130">-WhatIf</span></span>
<span data-ttu-id="f420a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f420a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f420a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f420a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f420a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f420a-133">CommonParameters</span></span>
<span data-ttu-id="f420a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f420a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f420a-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f420a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f420a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f420a-136">INPUTS</span></span>

### <span data-ttu-id="f420a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f420a-137">System.String</span></span>

### <span data-ttu-id="f420a-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span><span class="sxs-lookup"><span data-stu-id="f420a-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="f420a-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f420a-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f420a-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f420a-140">OUTPUTS</span></span>

### <span data-ttu-id="f420a-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f420a-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f420a-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="f420a-142">NOTES</span></span>
<span data-ttu-id="f420a-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="f420a-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f420a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f420a-144">RELATED LINKS</span></span>

[<span data-ttu-id="f420a-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f420a-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="f420a-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f420a-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="f420a-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f420a-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="f420a-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f420a-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f420a-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f420a-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f420a-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f420a-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f420a-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f420a-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f420a-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f420a-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
