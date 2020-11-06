---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: f09ca4bb6c033b954542d6c734b27bf5f2236d87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426603"
---
# <span data-ttu-id="cfe89-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="cfe89-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="cfe89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfe89-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe89-103">Remove uma política de replicação de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="cfe89-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfe89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfe89-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfe89-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfe89-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe89-106">O cmdlet **Remove-AzureRMSiteRecoveryPolicy** remove uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cfe89-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="cfe89-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfe89-107">EXAMPLES</span></span>

## <span data-ttu-id="cfe89-108">OS</span><span class="sxs-lookup"><span data-stu-id="cfe89-108">PARAMETERS</span></span>

### <span data-ttu-id="cfe89-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe89-109">-DefaultProfile</span></span>
<span data-ttu-id="cfe89-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe89-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfe89-111">-Política</span><span class="sxs-lookup"><span data-stu-id="cfe89-111">-Policy</span></span>
<span data-ttu-id="cfe89-112">Especifica o objeto da política de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="cfe89-112">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe89-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe89-113">CommonParameters</span></span>
<span data-ttu-id="cfe89-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe89-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe89-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe89-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe89-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfe89-116">INPUTS</span></span>

### <span data-ttu-id="cfe89-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="cfe89-117">ASRPolicy</span></span>
<span data-ttu-id="cfe89-118">O parâmetro "política" aceita o valor do tipo "ASRPolicy" da pipeline</span><span class="sxs-lookup"><span data-stu-id="cfe89-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="cfe89-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfe89-119">OUTPUTS</span></span>

## <span data-ttu-id="cfe89-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfe89-120">NOTES</span></span>

## <span data-ttu-id="cfe89-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfe89-121">RELATED LINKS</span></span>

[<span data-ttu-id="cfe89-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="cfe89-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="cfe89-123">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="cfe89-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
