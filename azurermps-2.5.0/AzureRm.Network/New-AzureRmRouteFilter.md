---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 981ef70f711cf418a92d8fb0caaae22c114f96b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786293"
---
# <span data-ttu-id="3f732-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3f732-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="3f732-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f732-102">SYNOPSIS</span></span>
<span data-ttu-id="3f732-103">Cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="3f732-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f732-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f732-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f732-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f732-105">DESCRIPTION</span></span>
<span data-ttu-id="3f732-106">O cmdlet New-AzureRmRouteFilter cria um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="3f732-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="3f732-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f732-107">EXAMPLES</span></span>

### <span data-ttu-id="3f732-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f732-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="3f732-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="3f732-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3f732-110">OS</span><span class="sxs-lookup"><span data-stu-id="3f732-110">PARAMETERS</span></span>

### <span data-ttu-id="3f732-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f732-111">-AsJob</span></span>
<span data-ttu-id="3f732-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3f732-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f732-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f732-113">-DefaultProfile</span></span>
<span data-ttu-id="3f732-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f732-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f732-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3f732-115">-Force</span></span>
<span data-ttu-id="3f732-116">Indica que esse cmdlet cria uma tabela de rota mesmo que um filtro de rota com o mesmo nome já exista.</span><span class="sxs-lookup"><span data-stu-id="3f732-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="3f732-117">-Local</span><span class="sxs-lookup"><span data-stu-id="3f732-117">-Location</span></span>
<span data-ttu-id="3f732-118">Especifica a região do Azure na qual esse cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="3f732-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="3f732-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f732-119">-Name</span></span>
<span data-ttu-id="3f732-120">Especifica um nome para o filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="3f732-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="3f732-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f732-121">-ResourceGroupName</span></span>
<span data-ttu-id="3f732-122">Especifica o nome do grupo de recursos em que esse cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="3f732-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="3f732-123">-Regra</span><span class="sxs-lookup"><span data-stu-id="3f732-123">-Rule</span></span>
<span data-ttu-id="3f732-124">Especifica uma matriz de objetos de regra de filtro de rota para associar ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="3f732-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="3f732-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="3f732-125">-Tag</span></span>
<span data-ttu-id="3f732-126">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3f732-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3f732-127">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="3f732-127">For example:</span></span>

<span data-ttu-id="3f732-128">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3f732-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3f732-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3f732-129">-Confirm</span></span>
<span data-ttu-id="3f732-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f732-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f732-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f732-131">-WhatIf</span></span>
<span data-ttu-id="3f732-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3f732-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f732-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f732-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f732-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f732-134">CommonParameters</span></span>
<span data-ttu-id="3f732-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f732-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f732-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f732-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f732-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f732-137">INPUTS</span></span>

## <span data-ttu-id="3f732-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f732-138">OUTPUTS</span></span>

### <span data-ttu-id="3f732-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3f732-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="3f732-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f732-140">NOTES</span></span>
<span data-ttu-id="3f732-141">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="3f732-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3f732-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f732-142">RELATED LINKS</span></span>

[<span data-ttu-id="3f732-143">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3f732-143">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="3f732-144">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f732-144">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="3f732-145">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3f732-145">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="3f732-146">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3f732-146">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
