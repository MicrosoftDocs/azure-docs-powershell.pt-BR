---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 6c17b3732cf5eab46f5826896dacafd3639aa788
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942844"
---
# <span data-ttu-id="9074c-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9074c-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="9074c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9074c-102">SYNOPSIS</span></span>
<span data-ttu-id="9074c-103">Cria um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="9074c-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="9074c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9074c-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9074c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9074c-105">DESCRIPTION</span></span>
<span data-ttu-id="9074c-106">O cmdlet **New-AzCdnProfile** cria um perfil da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="9074c-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="9074c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9074c-107">EXAMPLES</span></span>

## <span data-ttu-id="9074c-108">OS</span><span class="sxs-lookup"><span data-stu-id="9074c-108">PARAMETERS</span></span>

### <span data-ttu-id="9074c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9074c-109">-DefaultProfile</span></span>
<span data-ttu-id="9074c-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9074c-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9074c-111">-Local</span><span class="sxs-lookup"><span data-stu-id="9074c-111">-Location</span></span>
<span data-ttu-id="9074c-112">Especifica o local do recurso do perfil.</span><span class="sxs-lookup"><span data-stu-id="9074c-112">Specifies the resource location of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9074c-113">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9074c-113">-ProfileName</span></span>
<span data-ttu-id="9074c-114">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="9074c-114">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="9074c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9074c-115">-ResourceGroupName</span></span>
<span data-ttu-id="9074c-116">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="9074c-116">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="9074c-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="9074c-117">-Sku</span></span>
<span data-ttu-id="9074c-118">Especifica a SKU do perfil.</span><span class="sxs-lookup"><span data-stu-id="9074c-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn, Standard_Microsoft

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9074c-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="9074c-119">-Tag</span></span>
<span data-ttu-id="9074c-120">As marcas a serem associadas ao perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="9074c-120">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9074c-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9074c-121">-Confirm</span></span>
<span data-ttu-id="9074c-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9074c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9074c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9074c-123">-WhatIf</span></span>
<span data-ttu-id="9074c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9074c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9074c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9074c-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9074c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9074c-126">CommonParameters</span></span>
<span data-ttu-id="9074c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9074c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9074c-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9074c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9074c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9074c-129">INPUTS</span></span>

### <span data-ttu-id="9074c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9074c-130">System.String</span></span>

## <span data-ttu-id="9074c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9074c-131">OUTPUTS</span></span>

### <span data-ttu-id="9074c-132">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="9074c-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="9074c-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9074c-133">NOTES</span></span>

## <span data-ttu-id="9074c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9074c-134">RELATED LINKS</span></span>

[<span data-ttu-id="9074c-135">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9074c-135">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="9074c-136">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9074c-136">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="9074c-137">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9074c-137">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


