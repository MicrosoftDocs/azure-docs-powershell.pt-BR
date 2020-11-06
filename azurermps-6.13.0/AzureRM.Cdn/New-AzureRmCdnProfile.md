---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: c64f84c9f41dba29e54b14a69235bccd764ea750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609412"
---
# <span data-ttu-id="18fd9-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="18fd9-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="18fd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="18fd9-103">Cria um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="18fd9-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18fd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18fd9-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18fd9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18fd9-105">DESCRIPTION</span></span>
<span data-ttu-id="18fd9-106">O cmdlet **New-AzureRmCdnProfile** cria um perfil da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="18fd9-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="18fd9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18fd9-107">EXAMPLES</span></span>

## <span data-ttu-id="18fd9-108">OS</span><span class="sxs-lookup"><span data-stu-id="18fd9-108">PARAMETERS</span></span>

### <span data-ttu-id="18fd9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fd9-109">-DefaultProfile</span></span>
<span data-ttu-id="18fd9-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="18fd9-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18fd9-111">-Local</span><span class="sxs-lookup"><span data-stu-id="18fd9-111">-Location</span></span>
<span data-ttu-id="18fd9-112">Especifica o local do recurso do perfil.</span><span class="sxs-lookup"><span data-stu-id="18fd9-112">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="18fd9-113">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="18fd9-113">-ProfileName</span></span>
<span data-ttu-id="18fd9-114">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="18fd9-114">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="18fd9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18fd9-115">-ResourceGroupName</span></span>
<span data-ttu-id="18fd9-116">Especifica o nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="18fd9-116">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="18fd9-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="18fd9-117">-Sku</span></span>
<span data-ttu-id="18fd9-118">Especifica a SKU do perfil.</span><span class="sxs-lookup"><span data-stu-id="18fd9-118">Specifies the SKU of the profile.</span></span>

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

### <span data-ttu-id="18fd9-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="18fd9-119">-Tag</span></span>
<span data-ttu-id="18fd9-120">As marcas a serem associadas ao perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="18fd9-120">The tags to associate with the Azure CDN profile.</span></span>

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

### <span data-ttu-id="18fd9-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18fd9-121">-Confirm</span></span>
<span data-ttu-id="18fd9-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18fd9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18fd9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18fd9-123">-WhatIf</span></span>
<span data-ttu-id="18fd9-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18fd9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18fd9-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18fd9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18fd9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fd9-126">CommonParameters</span></span>
<span data-ttu-id="18fd9-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18fd9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fd9-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18fd9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fd9-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18fd9-129">INPUTS</span></span>

### <span data-ttu-id="18fd9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="18fd9-130">System.String</span></span>

## <span data-ttu-id="18fd9-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18fd9-131">OUTPUTS</span></span>

### <span data-ttu-id="18fd9-132">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="18fd9-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="18fd9-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18fd9-133">NOTES</span></span>

## <span data-ttu-id="18fd9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18fd9-134">RELATED LINKS</span></span>

[<span data-ttu-id="18fd9-135">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="18fd9-135">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="18fd9-136">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="18fd9-136">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="18fd9-137">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="18fd9-137">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


