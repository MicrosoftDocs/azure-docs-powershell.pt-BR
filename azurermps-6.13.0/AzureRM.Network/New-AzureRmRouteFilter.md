---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: a28fe30424b5b1d29c3b671e5cec266fc75d9dbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433204"
---
# <span data-ttu-id="8251f-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8251f-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="8251f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8251f-102">SYNOPSIS</span></span>
<span data-ttu-id="8251f-103">Cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="8251f-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8251f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8251f-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8251f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8251f-105">DESCRIPTION</span></span>
<span data-ttu-id="8251f-106">O cmdlet New-AzureRmRouteFilter cria um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="8251f-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="8251f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8251f-107">EXAMPLES</span></span>

### <span data-ttu-id="8251f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8251f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="8251f-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="8251f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="8251f-110">OS</span><span class="sxs-lookup"><span data-stu-id="8251f-110">PARAMETERS</span></span>

### <span data-ttu-id="8251f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8251f-111">-AsJob</span></span>
<span data-ttu-id="8251f-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8251f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8251f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8251f-113">-DefaultProfile</span></span>
<span data-ttu-id="8251f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8251f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8251f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8251f-115">-Force</span></span>
<span data-ttu-id="8251f-116">Indica que esse cmdlet cria uma tabela de rota mesmo que um filtro de rota com o mesmo nome já exista.</span><span class="sxs-lookup"><span data-stu-id="8251f-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="8251f-117">-Local</span><span class="sxs-lookup"><span data-stu-id="8251f-117">-Location</span></span>
<span data-ttu-id="8251f-118">Especifica a região do Azure na qual esse cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="8251f-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="8251f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8251f-119">-Name</span></span>
<span data-ttu-id="8251f-120">Especifica um nome para o filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="8251f-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="8251f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8251f-121">-ResourceGroupName</span></span>
<span data-ttu-id="8251f-122">Especifica o nome do grupo de recursos em que esse cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="8251f-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="8251f-123">-Regra</span><span class="sxs-lookup"><span data-stu-id="8251f-123">-Rule</span></span>
<span data-ttu-id="8251f-124">Especifica uma matriz de objetos de regra de filtro de rota para associar ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="8251f-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8251f-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="8251f-125">-Tag</span></span>
<span data-ttu-id="8251f-126">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8251f-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8251f-127">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8251f-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8251f-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8251f-128">-Confirm</span></span>
<span data-ttu-id="8251f-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8251f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8251f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8251f-130">-WhatIf</span></span>
<span data-ttu-id="8251f-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8251f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8251f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8251f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8251f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8251f-133">CommonParameters</span></span>
<span data-ttu-id="8251f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8251f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8251f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8251f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8251f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8251f-136">INPUTS</span></span>

### <span data-ttu-id="8251f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8251f-137">System.String</span></span>

### <span data-ttu-id="8251f-138">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8251f-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8251f-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8251f-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8251f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8251f-140">OUTPUTS</span></span>

### <span data-ttu-id="8251f-141">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8251f-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8251f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8251f-142">NOTES</span></span>
<span data-ttu-id="8251f-143">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="8251f-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8251f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8251f-144">RELATED LINKS</span></span>

[<span data-ttu-id="8251f-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8251f-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="8251f-146">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8251f-146">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="8251f-147">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8251f-147">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="8251f-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8251f-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
