---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 37e0096dd6f279c13909f1b542e603faebfd1e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609558"
---
# <span data-ttu-id="02078-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="02078-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="02078-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02078-102">SYNOPSIS</span></span>
<span data-ttu-id="02078-103">Obtém cofres de recuperação de site da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="02078-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02078-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02078-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02078-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02078-105">DESCRIPTION</span></span>
<span data-ttu-id="02078-106">O cmdlet **Get-AzureRmSiteRecoveryVault** Obtém uma lista de cofres do Azure site Recovery ou um cofre de recuperação de site específico da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="02078-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="02078-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02078-107">EXAMPLES</span></span>

## <span data-ttu-id="02078-108">OS</span><span class="sxs-lookup"><span data-stu-id="02078-108">PARAMETERS</span></span>

### <span data-ttu-id="02078-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="02078-109">-Name</span></span>
<span data-ttu-id="02078-110">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="02078-110">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02078-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02078-111">-ResourceGroupName</span></span>
<span data-ttu-id="02078-112">Especifica o nome do grupo de recursos do Azure do qual obter o objeto de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="02078-112">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02078-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02078-113">-DefaultProfile</span></span>
<span data-ttu-id="02078-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02078-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02078-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02078-115">CommonParameters</span></span>
<span data-ttu-id="02078-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02078-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02078-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02078-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02078-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02078-118">INPUTS</span></span>

## <span data-ttu-id="02078-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02078-119">OUTPUTS</span></span>

### <span data-ttu-id="02078-120">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="02078-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="02078-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02078-121">NOTES</span></span>

## <span data-ttu-id="02078-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02078-122">RELATED LINKS</span></span>

[<span data-ttu-id="02078-123">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="02078-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="02078-124">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="02078-124">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
