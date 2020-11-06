---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 4a710507321d2f4eb2a605846928f66c5bdb6a4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609918"
---
# <span data-ttu-id="791cb-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="791cb-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="791cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="791cb-102">SYNOPSIS</span></span>
<span data-ttu-id="791cb-103">Obtém os sites do Hyper-V do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="791cb-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="791cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="791cb-104">SYNTAX</span></span>

### <span data-ttu-id="791cb-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="791cb-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="791cb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="791cb-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="791cb-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="791cb-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="791cb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="791cb-108">DESCRIPTION</span></span>
<span data-ttu-id="791cb-109">O cmdlet **Get-AzureRmSiteRecoverySite** Obtém os sites do Hyper-V no cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="791cb-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="791cb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="791cb-110">EXAMPLES</span></span>

## <span data-ttu-id="791cb-111">OS</span><span class="sxs-lookup"><span data-stu-id="791cb-111">PARAMETERS</span></span>

### <span data-ttu-id="791cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="791cb-112">-DefaultProfile</span></span>
<span data-ttu-id="791cb-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="791cb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="791cb-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="791cb-114">-FriendlyName</span></span>
<span data-ttu-id="791cb-115">Especifica o nome amigável do site.</span><span class="sxs-lookup"><span data-stu-id="791cb-115">Specifies the friendly name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791cb-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="791cb-116">-Name</span></span>
<span data-ttu-id="791cb-117">Especifica o nome do site.</span><span class="sxs-lookup"><span data-stu-id="791cb-117">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791cb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791cb-118">CommonParameters</span></span>
<span data-ttu-id="791cb-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="791cb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791cb-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="791cb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791cb-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="791cb-121">INPUTS</span></span>

### <span data-ttu-id="791cb-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="791cb-122">None</span></span>
<span data-ttu-id="791cb-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="791cb-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="791cb-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="791cb-124">OUTPUTS</span></span>

### <span data-ttu-id="791cb-125">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="791cb-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="791cb-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="791cb-126">NOTES</span></span>

## <span data-ttu-id="791cb-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="791cb-127">RELATED LINKS</span></span>

[<span data-ttu-id="791cb-128">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="791cb-128">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="791cb-129">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="791cb-129">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
