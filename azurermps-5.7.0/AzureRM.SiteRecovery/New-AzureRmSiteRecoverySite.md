---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 053cd7695768be44cf3cecc5964e037f12f0b84e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431591"
---
# <span data-ttu-id="9cdc5-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="9cdc5-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="9cdc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9cdc5-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdc5-103">Cria um site de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="9cdc5-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cdc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9cdc5-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cdc5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9cdc5-105">DESCRIPTION</span></span>
<span data-ttu-id="9cdc5-106">O cmdlet **New-AzureRmSiteRecoverySite** cria um site de recuperação do site do Azure no cofre atual.</span><span class="sxs-lookup"><span data-stu-id="9cdc5-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="9cdc5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9cdc5-107">EXAMPLES</span></span>

## <span data-ttu-id="9cdc5-108">OS</span><span class="sxs-lookup"><span data-stu-id="9cdc5-108">PARAMETERS</span></span>

### <span data-ttu-id="9cdc5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdc5-109">-DefaultProfile</span></span>
<span data-ttu-id="9cdc5-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9cdc5-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cdc5-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="9cdc5-111">-Name</span></span>
<span data-ttu-id="9cdc5-112">Especifica o nome do site.</span><span class="sxs-lookup"><span data-stu-id="9cdc5-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdc5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdc5-113">CommonParameters</span></span>
<span data-ttu-id="9cdc5-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cdc5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdc5-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cdc5-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdc5-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9cdc5-116">INPUTS</span></span>

### <span data-ttu-id="9cdc5-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9cdc5-117">None</span></span>
<span data-ttu-id="9cdc5-118">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9cdc5-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9cdc5-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9cdc5-119">OUTPUTS</span></span>

## <span data-ttu-id="9cdc5-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9cdc5-120">NOTES</span></span>

## <span data-ttu-id="9cdc5-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9cdc5-121">RELATED LINKS</span></span>

[<span data-ttu-id="9cdc5-122">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="9cdc5-122">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="9cdc5-123">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="9cdc5-123">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
