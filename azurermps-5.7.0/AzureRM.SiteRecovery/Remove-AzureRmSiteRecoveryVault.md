---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 70d0876be32b80d314dfb7a464d0626b7c534fea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426597"
---
# <span data-ttu-id="845a0-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="845a0-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="845a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="845a0-102">SYNOPSIS</span></span>
<span data-ttu-id="845a0-103">Remove um cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="845a0-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="845a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="845a0-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="845a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="845a0-105">DESCRIPTION</span></span>
<span data-ttu-id="845a0-106">O cmdlet **Remove-AzureRmSiteRecoveryVault** exclui um cofre do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="845a0-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="845a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="845a0-107">EXAMPLES</span></span>

## <span data-ttu-id="845a0-108">OS</span><span class="sxs-lookup"><span data-stu-id="845a0-108">PARAMETERS</span></span>

### <span data-ttu-id="845a0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="845a0-109">-DefaultProfile</span></span>
<span data-ttu-id="845a0-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="845a0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="845a0-111">-Cofre</span><span class="sxs-lookup"><span data-stu-id="845a0-111">-Vault</span></span>
<span data-ttu-id="845a0-112">Especifica o objeto do cofre de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="845a0-112">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="845a0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="845a0-113">CommonParameters</span></span>
<span data-ttu-id="845a0-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="845a0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="845a0-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="845a0-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="845a0-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="845a0-116">INPUTS</span></span>

### <span data-ttu-id="845a0-117">ASRVault</span><span class="sxs-lookup"><span data-stu-id="845a0-117">ASRVault</span></span>
<span data-ttu-id="845a0-118">O parâmetro ' cofre ' aceita o valor do tipo ' ASRVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="845a0-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="845a0-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="845a0-119">OUTPUTS</span></span>

## <span data-ttu-id="845a0-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="845a0-120">NOTES</span></span>

## <span data-ttu-id="845a0-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="845a0-121">RELATED LINKS</span></span>

[<span data-ttu-id="845a0-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="845a0-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="845a0-123">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="845a0-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
