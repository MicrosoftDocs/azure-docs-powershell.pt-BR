---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: b87963b45010299dcb80c4b1859af8614f845526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427662"
---
# <span data-ttu-id="07d78-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07d78-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="07d78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07d78-102">SYNOPSIS</span></span>
<span data-ttu-id="07d78-103">Obtém um domínio personalizado CDN.</span><span class="sxs-lookup"><span data-stu-id="07d78-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07d78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07d78-104">SYNTAX</span></span>

### <span data-ttu-id="07d78-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="07d78-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07d78-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07d78-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07d78-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07d78-107">DESCRIPTION</span></span>
<span data-ttu-id="07d78-108">O cmdlet **Get-AzureRmCdnCustomDomain** Obtém um domínio personalizado de CDN (rede de distribuição de conteúdo) do Azure e suas configurações relacionadas.</span><span class="sxs-lookup"><span data-stu-id="07d78-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="07d78-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07d78-109">EXAMPLES</span></span>

## <span data-ttu-id="07d78-110">OS</span><span class="sxs-lookup"><span data-stu-id="07d78-110">PARAMETERS</span></span>

### <span data-ttu-id="07d78-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="07d78-111">-CdnEndpoint</span></span>
<span data-ttu-id="07d78-112">Especifica o objeto de ponto de extremidade CDN do qual o domínio personalizado é membro.</span><span class="sxs-lookup"><span data-stu-id="07d78-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="07d78-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="07d78-113">-CustomDomainName</span></span>
<span data-ttu-id="07d78-114">Especifica o nome do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="07d78-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="07d78-115">O nome do domínio personalizado é diferente do nome do host do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="07d78-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d78-116">-DefaultProfile</span></span>
<span data-ttu-id="07d78-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="07d78-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07d78-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="07d78-118">-EndpointName</span></span>
<span data-ttu-id="07d78-119">Especifica o nome do ponto de extremidade ao qual pertence o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="07d78-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="07d78-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="07d78-120">-ProfileName</span></span>
<span data-ttu-id="07d78-121">Especifica o nome do perfil ao qual pertence o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="07d78-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="07d78-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d78-122">-ResourceGroupName</span></span>
<span data-ttu-id="07d78-123">Especifica o nome do grupo de recursos ao qual pertence o domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="07d78-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="07d78-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d78-124">CommonParameters</span></span>
<span data-ttu-id="07d78-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d78-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d78-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d78-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d78-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07d78-127">INPUTS</span></span>

### <span data-ttu-id="07d78-128">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="07d78-128">PSEndpoint</span></span>
<span data-ttu-id="07d78-129">O parâmetro ' CdnEndpoint ' aceita o valor do tipo ' PSEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="07d78-129">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="07d78-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07d78-130">OUTPUTS</span></span>

###  
<span data-ttu-id="07d78-131">Esse cmdlet retorna um objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="07d78-131">This cmdlet returns a custom domain object.</span></span>

## <span data-ttu-id="07d78-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07d78-132">NOTES</span></span>

## <span data-ttu-id="07d78-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07d78-133">RELATED LINKS</span></span>

[<span data-ttu-id="07d78-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07d78-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="07d78-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07d78-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


