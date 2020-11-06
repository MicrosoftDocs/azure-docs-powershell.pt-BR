---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d6c93a6ca54a67c13fcba54a11d9f30c61377e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609903"
---
# <span data-ttu-id="96fca-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96fca-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="96fca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96fca-102">SYNOPSIS</span></span>
<span data-ttu-id="96fca-103">Remove um plano de recuperação de site da recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="96fca-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96fca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96fca-104">SYNTAX</span></span>

### <span data-ttu-id="96fca-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="96fca-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96fca-106">ByName</span><span class="sxs-lookup"><span data-stu-id="96fca-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96fca-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96fca-107">DESCRIPTION</span></span>
<span data-ttu-id="96fca-108">O cmdlet **Remove-AzureRmSiteRecoveryRecoveryPlan** remove um plano de recuperação de site do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="96fca-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="96fca-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96fca-109">EXAMPLES</span></span>

### <span data-ttu-id="96fca-110">Exemplo 1: remover um plano de recuperação</span><span class="sxs-lookup"><span data-stu-id="96fca-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="96fca-111">O primeiro comando usa o cmdlet Get-AzureRmSiteRecoveryRecoveryPlan para obter o plano de recuperação do site e, em seguida, armazena-o na variável $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="96fca-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="96fca-112">O segundo comando Remove o plano de recuperação em $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="96fca-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="96fca-113">OS</span><span class="sxs-lookup"><span data-stu-id="96fca-113">PARAMETERS</span></span>

### <span data-ttu-id="96fca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96fca-114">-DefaultProfile</span></span>
<span data-ttu-id="96fca-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96fca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96fca-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="96fca-116">-Name</span></span>
<span data-ttu-id="96fca-117">Especifica o nome do plano de recuperação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="96fca-117">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

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

### <span data-ttu-id="96fca-118">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96fca-118">-RecoveryPlan</span></span>
<span data-ttu-id="96fca-119">Especifica o plano de recuperação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="96fca-119">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96fca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96fca-120">CommonParameters</span></span>
<span data-ttu-id="96fca-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96fca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96fca-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96fca-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96fca-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96fca-123">INPUTS</span></span>

### <span data-ttu-id="96fca-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96fca-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="96fca-125">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="96fca-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="96fca-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96fca-126">OUTPUTS</span></span>

## <span data-ttu-id="96fca-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96fca-127">NOTES</span></span>

## <span data-ttu-id="96fca-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96fca-128">RELATED LINKS</span></span>

[<span data-ttu-id="96fca-129">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96fca-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="96fca-130">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96fca-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="96fca-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="96fca-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


