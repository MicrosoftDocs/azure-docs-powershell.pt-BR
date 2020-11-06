---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 6cc420ccb2ba2c7e555956d711fe0e30d02ef62f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429253"
---
# <span data-ttu-id="d2033-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d2033-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="d2033-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2033-102">SYNOPSIS</span></span>
<span data-ttu-id="d2033-103">Cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="d2033-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2033-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2033-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2033-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2033-105">DESCRIPTION</span></span>
<span data-ttu-id="d2033-106">O cmdlet New-AzureRmRouteFilter cria um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2033-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="d2033-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2033-107">EXAMPLES</span></span>

### <span data-ttu-id="d2033-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2033-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="d2033-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="d2033-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d2033-110">OS</span><span class="sxs-lookup"><span data-stu-id="d2033-110">PARAMETERS</span></span>

### <span data-ttu-id="d2033-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d2033-111">-Force</span></span>
<span data-ttu-id="d2033-112">Indica que esse cmdlet cria uma tabela de rota mesmo que um filtro de rota com o mesmo nome já exista.</span><span class="sxs-lookup"><span data-stu-id="d2033-112">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="d2033-113">-Local</span><span class="sxs-lookup"><span data-stu-id="d2033-113">-Location</span></span>
<span data-ttu-id="d2033-114">Especifica a região do Azure na qual esse cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="d2033-114">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="d2033-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2033-115">-Name</span></span>
<span data-ttu-id="d2033-116">Especifica um nome para o filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="d2033-116">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="d2033-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2033-117">-ResourceGroupName</span></span>
<span data-ttu-id="d2033-118">Especifica o nome do grupo de recursos em que esse cmdlet cria um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="d2033-118">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="d2033-119">-Regra</span><span class="sxs-lookup"><span data-stu-id="d2033-119">-Rule</span></span>
<span data-ttu-id="d2033-120">Especifica uma matriz de objetos de regra de filtro de rota para associar ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="d2033-120">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="d2033-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="d2033-121">-Tag</span></span>
<span data-ttu-id="d2033-122">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d2033-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d2033-123">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d2033-123">For example:</span></span>

<span data-ttu-id="d2033-124">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d2033-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d2033-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2033-125">-Confirm</span></span>
<span data-ttu-id="d2033-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2033-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2033-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2033-127">-WhatIf</span></span>
<span data-ttu-id="d2033-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2033-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2033-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2033-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2033-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2033-130">-DefaultProfile</span></span>
<span data-ttu-id="d2033-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2033-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2033-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2033-132">CommonParameters</span></span>
<span data-ttu-id="d2033-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2033-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2033-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2033-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2033-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2033-135">INPUTS</span></span>

## <span data-ttu-id="d2033-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2033-136">OUTPUTS</span></span>

### <span data-ttu-id="d2033-137">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d2033-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d2033-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2033-138">NOTES</span></span>
<span data-ttu-id="d2033-139">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="d2033-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d2033-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2033-140">RELATED LINKS</span></span>

[<span data-ttu-id="d2033-141">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d2033-141">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="d2033-142">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2033-142">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="d2033-143">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d2033-143">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="d2033-144">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d2033-144">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
