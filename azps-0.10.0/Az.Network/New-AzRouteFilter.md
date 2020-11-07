---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 0b02c1bfbeee6fa3a628ea6ffacd04c15e96a440
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775363"
---
# <span data-ttu-id="71885-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="71885-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="71885-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71885-102">SYNOPSIS</span></span>
<span data-ttu-id="71885-103">Cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="71885-103">Creates a route filter.</span></span>

## <span data-ttu-id="71885-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71885-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71885-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71885-105">DESCRIPTION</span></span>
<span data-ttu-id="71885-106">O cmdlet New-AzRouteFilter cria um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="71885-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="71885-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71885-107">EXAMPLES</span></span>

### <span data-ttu-id="71885-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71885-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="71885-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="71885-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="71885-110">OS</span><span class="sxs-lookup"><span data-stu-id="71885-110">PARAMETERS</span></span>

### <span data-ttu-id="71885-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71885-111">-AsJob</span></span>
<span data-ttu-id="71885-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="71885-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71885-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71885-113">-DefaultProfile</span></span>
<span data-ttu-id="71885-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71885-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71885-115">-Force</span><span class="sxs-lookup"><span data-stu-id="71885-115">-Force</span></span>
<span data-ttu-id="71885-116">Indica que esse cmdlet cria uma tabela de rota mesmo que um filtro de rota com o mesmo nome já exista.</span><span class="sxs-lookup"><span data-stu-id="71885-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71885-117">-Local</span><span class="sxs-lookup"><span data-stu-id="71885-117">-Location</span></span>
<span data-ttu-id="71885-118">Especifica a região do Azure na qual esse cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="71885-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71885-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="71885-119">-Name</span></span>
<span data-ttu-id="71885-120">Especifica um nome para o filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="71885-120">Specifies a name for the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71885-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71885-121">-ResourceGroupName</span></span>
<span data-ttu-id="71885-122">Especifica o nome do grupo de recursos em que esse cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="71885-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71885-123">-Regra</span><span class="sxs-lookup"><span data-stu-id="71885-123">-Rule</span></span>
<span data-ttu-id="71885-124">Especifica uma matriz de objetos de regra de filtro de rota para associar ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="71885-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="71885-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="71885-125">-Tag</span></span>
<span data-ttu-id="71885-126">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="71885-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="71885-127">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="71885-127">For example:</span></span>

<span data-ttu-id="71885-128">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="71885-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71885-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71885-129">-Confirm</span></span>
<span data-ttu-id="71885-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71885-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71885-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71885-131">-WhatIf</span></span>
<span data-ttu-id="71885-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71885-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71885-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71885-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71885-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71885-134">CommonParameters</span></span>
<span data-ttu-id="71885-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71885-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71885-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71885-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71885-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71885-137">INPUTS</span></span>

## <span data-ttu-id="71885-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71885-138">OUTPUTS</span></span>

### <span data-ttu-id="71885-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="71885-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="71885-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71885-140">NOTES</span></span>
<span data-ttu-id="71885-141">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="71885-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="71885-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71885-142">RELATED LINKS</span></span>

[<span data-ttu-id="71885-143">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="71885-143">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="71885-144">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71885-144">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="71885-145">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="71885-145">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="71885-146">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="71885-146">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
