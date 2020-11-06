---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: d93dadc062f2cc12ed363039d69266daf365920e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427655"
---
# <span data-ttu-id="ed1ac-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="ed1ac-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="ed1ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed1ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1ac-103">Obtém a URL de logon único de um perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="ed1ac-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed1ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed1ac-104">SYNTAX</span></span>

### <span data-ttu-id="ed1ac-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ed1ac-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed1ac-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed1ac-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed1ac-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed1ac-107">DESCRIPTION</span></span>
<span data-ttu-id="ed1ac-108">O cmdlet **Get-AzureRmCdnProfileSsoUrl** Obtém a URL de logon único do perfil da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed1ac-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="ed1ac-109">Esta URL permite que os usuários conntectm um portal complementar e usem recursos adicionais da CDN.</span><span class="sxs-lookup"><span data-stu-id="ed1ac-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="ed1ac-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed1ac-110">EXAMPLES</span></span>

## <span data-ttu-id="ed1ac-111">OS</span><span class="sxs-lookup"><span data-stu-id="ed1ac-111">PARAMETERS</span></span>

### <span data-ttu-id="ed1ac-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ed1ac-112">-CdnProfile</span></span>
<span data-ttu-id="ed1ac-113">Especifica o perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="ed1ac-113">Specifies the CDN profile.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed1ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1ac-114">-DefaultProfile</span></span>
<span data-ttu-id="ed1ac-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ed1ac-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed1ac-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ed1ac-116">-ProfileName</span></span>
<span data-ttu-id="ed1ac-117">Especifica o nome do perfil CDN.</span><span class="sxs-lookup"><span data-stu-id="ed1ac-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="ed1ac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed1ac-118">-ResourceGroupName</span></span>
<span data-ttu-id="ed1ac-119">Especifica o nome do nome do grupo de recursos ao qual o perfil pertence.</span><span class="sxs-lookup"><span data-stu-id="ed1ac-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="ed1ac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1ac-120">CommonParameters</span></span>
<span data-ttu-id="ed1ac-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed1ac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1ac-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed1ac-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1ac-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed1ac-123">INPUTS</span></span>

### <span data-ttu-id="ed1ac-124">PSProfile</span><span class="sxs-lookup"><span data-stu-id="ed1ac-124">PSProfile</span></span>
<span data-ttu-id="ed1ac-125">O parâmetro ' CdnProfile ' aceita o valor do tipo ' PSProfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ed1ac-125">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="ed1ac-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed1ac-126">OUTPUTS</span></span>

###  
<span data-ttu-id="ed1ac-127">Esse cmdlet retorna uma URL.</span><span class="sxs-lookup"><span data-stu-id="ed1ac-127">This cmdlet returns a URL.</span></span>

## <span data-ttu-id="ed1ac-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed1ac-128">NOTES</span></span>

## <span data-ttu-id="ed1ac-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed1ac-129">RELATED LINKS</span></span>

[<span data-ttu-id="ed1ac-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ed1ac-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


