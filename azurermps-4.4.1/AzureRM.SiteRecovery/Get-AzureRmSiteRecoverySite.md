---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: e41b491611ebc5dda1da56ac26827c5fa547dd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429072"
---
# <span data-ttu-id="cff07-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="cff07-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="cff07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cff07-102">SYNOPSIS</span></span>
<span data-ttu-id="cff07-103">Obtém os sites do Hyper-V do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="cff07-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cff07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cff07-104">SYNTAX</span></span>

### <span data-ttu-id="cff07-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="cff07-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cff07-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cff07-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cff07-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="cff07-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cff07-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cff07-108">DESCRIPTION</span></span>
<span data-ttu-id="cff07-109">O cmdlet **Get-AzureRmSiteRecoverySite** Obtém os sites do Hyper-V no cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cff07-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="cff07-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cff07-110">EXAMPLES</span></span>

## <span data-ttu-id="cff07-111">OS</span><span class="sxs-lookup"><span data-stu-id="cff07-111">PARAMETERS</span></span>

### <span data-ttu-id="cff07-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cff07-112">-FriendlyName</span></span>
<span data-ttu-id="cff07-113">Especifica o nome amigável do site.</span><span class="sxs-lookup"><span data-stu-id="cff07-113">Specifies the friendly name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff07-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="cff07-114">-Name</span></span>
<span data-ttu-id="cff07-115">Especifica o nome do site.</span><span class="sxs-lookup"><span data-stu-id="cff07-115">Specifies the name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff07-116">-DefaultProfile</span></span>
<span data-ttu-id="cff07-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cff07-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cff07-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff07-118">CommonParameters</span></span>
<span data-ttu-id="cff07-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cff07-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff07-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff07-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff07-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cff07-121">INPUTS</span></span>

## <span data-ttu-id="cff07-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cff07-122">OUTPUTS</span></span>

### <span data-ttu-id="cff07-123">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="cff07-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="cff07-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cff07-124">NOTES</span></span>

## <span data-ttu-id="cff07-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cff07-125">RELATED LINKS</span></span>

[<span data-ttu-id="cff07-126">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="cff07-126">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="cff07-127">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="cff07-127">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
