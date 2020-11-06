---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 3b01e089271cc131af5a4258c46836a87104ef62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602683"
---
# <span data-ttu-id="b62a7-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b62a7-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="b62a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b62a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b62a7-103">Remove uma política de replicação de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="b62a7-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b62a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b62a7-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b62a7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b62a7-105">DESCRIPTION</span></span>
<span data-ttu-id="b62a7-106">O cmdlet **Remove-AzureRMSiteRecoveryPolicy** remove uma política de replicação do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b62a7-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="b62a7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b62a7-107">EXAMPLES</span></span>

## <span data-ttu-id="b62a7-108">OS</span><span class="sxs-lookup"><span data-stu-id="b62a7-108">PARAMETERS</span></span>

### <span data-ttu-id="b62a7-109">-Política</span><span class="sxs-lookup"><span data-stu-id="b62a7-109">-Policy</span></span>
<span data-ttu-id="b62a7-110">Especifica o objeto da política de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="b62a7-110">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b62a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62a7-111">-DefaultProfile</span></span>
<span data-ttu-id="b62a7-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b62a7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b62a7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62a7-113">CommonParameters</span></span>
<span data-ttu-id="b62a7-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b62a7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62a7-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b62a7-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62a7-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b62a7-116">INPUTS</span></span>

### <span data-ttu-id="b62a7-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="b62a7-117">ASRPolicy</span></span>
<span data-ttu-id="b62a7-118">O parâmetro "política" aceita o valor do tipo "ASRPolicy" da pipeline</span><span class="sxs-lookup"><span data-stu-id="b62a7-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="b62a7-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b62a7-119">OUTPUTS</span></span>

## <span data-ttu-id="b62a7-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b62a7-120">NOTES</span></span>

## <span data-ttu-id="b62a7-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b62a7-121">RELATED LINKS</span></span>

[<span data-ttu-id="b62a7-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b62a7-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="b62a7-123">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b62a7-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
