---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 508465250489f2bcd0b031627258f11370fccfa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427640"
---
# <span data-ttu-id="cd486-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd486-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="cd486-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd486-102">SYNOPSIS</span></span>
<span data-ttu-id="cd486-103">Para o ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="cd486-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd486-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd486-104">SYNTAX</span></span>

### <span data-ttu-id="cd486-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cd486-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd486-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd486-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd486-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd486-107">DESCRIPTION</span></span>
<span data-ttu-id="cd486-108">O cmdlet **Stop-AzureRmCdnEndpoint** interrompe o ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="cd486-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="cd486-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd486-109">EXAMPLES</span></span>

## <span data-ttu-id="cd486-110">OS</span><span class="sxs-lookup"><span data-stu-id="cd486-110">PARAMETERS</span></span>

### <span data-ttu-id="cd486-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd486-111">-CdnEndpoint</span></span>
<span data-ttu-id="cd486-112">Especifica o objeto de ponto de extremidade para o qual este cmdlet é interrompido.</span><span class="sxs-lookup"><span data-stu-id="cd486-112">Specifies the endpoint object that this cmdlet stops.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd486-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd486-113">-DefaultProfile</span></span>
<span data-ttu-id="cd486-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cd486-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd486-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cd486-115">-EndpointName</span></span>
<span data-ttu-id="cd486-116">Especifica o nome do ponto de extremidade que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="cd486-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd486-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd486-117">-PassThru</span></span>
<span data-ttu-id="cd486-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="cd486-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd486-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="cd486-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd486-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cd486-120">-ProfileName</span></span>
<span data-ttu-id="cd486-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="cd486-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd486-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd486-122">-ResourceGroupName</span></span>
<span data-ttu-id="cd486-123">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="cd486-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd486-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cd486-124">-Confirm</span></span>
<span data-ttu-id="cd486-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd486-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd486-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd486-126">-WhatIf</span></span>
<span data-ttu-id="cd486-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd486-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd486-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd486-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd486-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd486-129">CommonParameters</span></span>
<span data-ttu-id="cd486-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd486-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd486-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd486-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd486-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd486-132">INPUTS</span></span>

### <span data-ttu-id="cd486-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd486-133">PSEndpoint</span></span>
<span data-ttu-id="cd486-134">O parâmetro ' CdnEndpoint ' aceita o valor do tipo ' PSEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cd486-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="cd486-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd486-135">OUTPUTS</span></span>

### <span data-ttu-id="cd486-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd486-136">System.Boolean</span></span>

## <span data-ttu-id="cd486-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd486-137">NOTES</span></span>

## <span data-ttu-id="cd486-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd486-138">RELATED LINKS</span></span>

[<span data-ttu-id="cd486-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd486-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cd486-140">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd486-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cd486-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd486-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cd486-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd486-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="cd486-143">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd486-143">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


