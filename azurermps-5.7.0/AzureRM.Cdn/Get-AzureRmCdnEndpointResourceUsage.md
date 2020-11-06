---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 82daa7f202dce698a84d17292a199fbd8f85bca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440520"
---
# <span data-ttu-id="ec3a7-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="ec3a7-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="ec3a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec3a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec3a7-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="ec3a7-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec3a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec3a7-104">SYNTAX</span></span>

### <span data-ttu-id="ec3a7-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ec3a7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec3a7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec3a7-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec3a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec3a7-107">DESCRIPTION</span></span>
<span data-ttu-id="ec3a7-108">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="ec3a7-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ec3a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec3a7-109">EXAMPLES</span></span>

### <span data-ttu-id="ec3a7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec3a7-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ec3a7-111">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="ec3a7-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="ec3a7-112">OS</span><span class="sxs-lookup"><span data-stu-id="ec3a7-112">PARAMETERS</span></span>

### <span data-ttu-id="ec3a7-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec3a7-113">-CdnEndpoint</span></span>
<span data-ttu-id="ec3a7-114">O objeto de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="ec3a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec3a7-115">-DefaultProfile</span></span>
<span data-ttu-id="ec3a7-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ec3a7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec3a7-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ec3a7-117">-EndpointName</span></span>
<span data-ttu-id="ec3a7-118">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="ec3a7-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ec3a7-119">-ProfileName</span></span>
<span data-ttu-id="ec3a7-120">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="ec3a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec3a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="ec3a7-122">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="ec3a7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec3a7-123">CommonParameters</span></span>
<span data-ttu-id="ec3a7-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec3a7-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec3a7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec3a7-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec3a7-126">INPUTS</span></span>

### <span data-ttu-id="ec3a7-127">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec3a7-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="ec3a7-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec3a7-128">OUTPUTS</span></span>

### <span data-ttu-id="ec3a7-129">Microsoft. Azure. Commands. cdn. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="ec3a7-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="ec3a7-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec3a7-130">NOTES</span></span>

## <span data-ttu-id="ec3a7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec3a7-131">RELATED LINKS</span></span>
