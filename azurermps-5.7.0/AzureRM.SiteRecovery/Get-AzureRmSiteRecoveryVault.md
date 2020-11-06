---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: f3988d28633ba879ebf78c57e235f4f07d6deced
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609914"
---
# <span data-ttu-id="77631-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="77631-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="77631-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77631-102">SYNOPSIS</span></span>
<span data-ttu-id="77631-103">Obtém cofres de recuperação de site da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="77631-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77631-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77631-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77631-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77631-105">DESCRIPTION</span></span>
<span data-ttu-id="77631-106">O cmdlet **Get-AzureRmSiteRecoveryVault** Obtém uma lista de cofres do Azure site Recovery ou um cofre de recuperação de site específico da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="77631-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="77631-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77631-107">EXAMPLES</span></span>

## <span data-ttu-id="77631-108">OS</span><span class="sxs-lookup"><span data-stu-id="77631-108">PARAMETERS</span></span>

### <span data-ttu-id="77631-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77631-109">-DefaultProfile</span></span>
<span data-ttu-id="77631-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77631-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77631-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="77631-111">-Name</span></span>
<span data-ttu-id="77631-112">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="77631-112">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="77631-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77631-113">-ResourceGroupName</span></span>
<span data-ttu-id="77631-114">Especifica o nome do grupo de recursos do Azure do qual obter o objeto de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="77631-114">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

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

### <span data-ttu-id="77631-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77631-115">CommonParameters</span></span>
<span data-ttu-id="77631-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77631-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77631-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77631-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77631-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77631-118">INPUTS</span></span>

### <span data-ttu-id="77631-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="77631-119">None</span></span>
<span data-ttu-id="77631-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="77631-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77631-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77631-121">OUTPUTS</span></span>

### <span data-ttu-id="77631-122">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="77631-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="77631-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77631-123">NOTES</span></span>

## <span data-ttu-id="77631-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77631-124">RELATED LINKS</span></span>

[<span data-ttu-id="77631-125">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="77631-125">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="77631-126">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="77631-126">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
