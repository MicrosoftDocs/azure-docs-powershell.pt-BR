---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 0e69e48d29c96163acbb82ffe691de6affe8d131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432656"
---
# <span data-ttu-id="9049f-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9049f-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="9049f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9049f-102">SYNOPSIS</span></span>
<span data-ttu-id="9049f-103">Cria um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="9049f-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9049f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9049f-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9049f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9049f-105">DESCRIPTION</span></span>
<span data-ttu-id="9049f-106">O cmdlet **New-AzureRmCdnProfile** cria um perfil da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="9049f-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="9049f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9049f-107">EXAMPLES</span></span>

## <span data-ttu-id="9049f-108">OS</span><span class="sxs-lookup"><span data-stu-id="9049f-108">PARAMETERS</span></span>

### <span data-ttu-id="9049f-109">-Local</span><span class="sxs-lookup"><span data-stu-id="9049f-109">-Location</span></span>
<span data-ttu-id="9049f-110">Especifica o local do recurso do perfil.</span><span class="sxs-lookup"><span data-stu-id="9049f-110">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="9049f-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9049f-111">-ProfileName</span></span>
<span data-ttu-id="9049f-112">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="9049f-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="9049f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9049f-113">-ResourceGroupName</span></span>
<span data-ttu-id="9049f-114">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="9049f-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="9049f-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="9049f-115">-Sku</span></span>
<span data-ttu-id="9049f-116">Especifica a SKU do perfil.</span><span class="sxs-lookup"><span data-stu-id="9049f-116">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9049f-117">-Marcas</span><span class="sxs-lookup"><span data-stu-id="9049f-117">-Tags</span></span>
<span data-ttu-id="9049f-118">Sepcifies uma tabela de hash de marcas que estão associadas a esse perfil.</span><span class="sxs-lookup"><span data-stu-id="9049f-118">Sepcifies a hash table of tags that are associated with this profile.</span></span>

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

### <span data-ttu-id="9049f-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9049f-119">-Confirm</span></span>
<span data-ttu-id="9049f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9049f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9049f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9049f-121">-WhatIf</span></span>
<span data-ttu-id="9049f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9049f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9049f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9049f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9049f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9049f-124">-DefaultProfile</span></span>
<span data-ttu-id="9049f-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9049f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9049f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9049f-126">CommonParameters</span></span>
<span data-ttu-id="9049f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9049f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9049f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9049f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9049f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9049f-129">INPUTS</span></span>

## <span data-ttu-id="9049f-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9049f-130">OUTPUTS</span></span>

### <span data-ttu-id="9049f-131">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="9049f-131">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="9049f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9049f-132">NOTES</span></span>

## <span data-ttu-id="9049f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9049f-133">RELATED LINKS</span></span>

[<span data-ttu-id="9049f-134">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9049f-134">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="9049f-135">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9049f-135">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="9049f-136">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9049f-136">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


