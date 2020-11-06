---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 703b686f11d7d55cc77bcfde929f9a9f261070f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601406"
---
# <span data-ttu-id="208d3-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="208d3-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="208d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="208d3-102">SYNOPSIS</span></span>
<span data-ttu-id="208d3-103">Cria um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="208d3-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="208d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="208d3-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="208d3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="208d3-105">DESCRIPTION</span></span>
<span data-ttu-id="208d3-106">O cmdlet **New-AzCdnProfile** cria um perfil da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="208d3-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="208d3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="208d3-107">EXAMPLES</span></span>

## <span data-ttu-id="208d3-108">OS</span><span class="sxs-lookup"><span data-stu-id="208d3-108">PARAMETERS</span></span>

### <span data-ttu-id="208d3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="208d3-109">-DefaultProfile</span></span>
<span data-ttu-id="208d3-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="208d3-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="208d3-111">-Local</span><span class="sxs-lookup"><span data-stu-id="208d3-111">-Location</span></span>
<span data-ttu-id="208d3-112">Especifica o local do recurso do perfil.</span><span class="sxs-lookup"><span data-stu-id="208d3-112">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="208d3-113">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="208d3-113">-ProfileName</span></span>
<span data-ttu-id="208d3-114">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="208d3-114">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="208d3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="208d3-115">-ResourceGroupName</span></span>
<span data-ttu-id="208d3-116">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="208d3-116">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="208d3-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="208d3-117">-Sku</span></span>
<span data-ttu-id="208d3-118">Especifica a SKU do perfil.</span><span class="sxs-lookup"><span data-stu-id="208d3-118">Specifies the SKU of the profile.</span></span>

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

### <span data-ttu-id="208d3-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="208d3-119">-Tag</span></span>
<span data-ttu-id="208d3-120">As marcas a serem associadas ao perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="208d3-120">The tags to associate with the Azure CDN profile.</span></span>

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

### <span data-ttu-id="208d3-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="208d3-121">-Confirm</span></span>
<span data-ttu-id="208d3-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="208d3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="208d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="208d3-123">-WhatIf</span></span>
<span data-ttu-id="208d3-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="208d3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="208d3-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="208d3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="208d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208d3-126">CommonParameters</span></span>
<span data-ttu-id="208d3-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="208d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208d3-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="208d3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208d3-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="208d3-129">INPUTS</span></span>

### <span data-ttu-id="208d3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="208d3-130">System.String</span></span>

## <span data-ttu-id="208d3-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="208d3-131">OUTPUTS</span></span>

### <span data-ttu-id="208d3-132">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="208d3-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="208d3-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="208d3-133">NOTES</span></span>

## <span data-ttu-id="208d3-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="208d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="208d3-135">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="208d3-135">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="208d3-136">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="208d3-136">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="208d3-137">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="208d3-137">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


