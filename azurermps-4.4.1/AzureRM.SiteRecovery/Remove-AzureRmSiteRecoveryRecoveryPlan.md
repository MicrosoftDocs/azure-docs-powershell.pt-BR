---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 5657701475e81b302d761193cd542ee38ea9c16e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430616"
---
# <span data-ttu-id="ccfcd-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ccfcd-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="ccfcd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccfcd-102">SYNOPSIS</span></span>
<span data-ttu-id="ccfcd-103">Remove um plano de recuperação de site da recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccfcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccfcd-104">SYNTAX</span></span>

### <span data-ttu-id="ccfcd-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="ccfcd-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccfcd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ccfcd-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccfcd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ccfcd-107">DESCRIPTION</span></span>
<span data-ttu-id="ccfcd-108">O cmdlet **Remove-AzureRmSiteRecoveryRecoveryPlan** remove um plano de recuperação de site do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="ccfcd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccfcd-109">EXAMPLES</span></span>

### <span data-ttu-id="ccfcd-110">Exemplo 1: remover um plano de recuperação</span><span class="sxs-lookup"><span data-stu-id="ccfcd-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="ccfcd-111">O primeiro comando usa o cmdlet Get-AzureRmSiteRecoveryRecoveryPlan para obter o plano de recuperação do site e, em seguida, armazena-o na variável $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="ccfcd-112">O segundo comando Remove o plano de recuperação em $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="ccfcd-113">OS</span><span class="sxs-lookup"><span data-stu-id="ccfcd-113">PARAMETERS</span></span>

### <span data-ttu-id="ccfcd-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccfcd-114">-Name</span></span>
<span data-ttu-id="ccfcd-115">Especifica o nome do plano de recuperação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-115">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ccfcd-116">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ccfcd-116">-RecoveryPlan</span></span>
<span data-ttu-id="ccfcd-117">Especifica o plano de recuperação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-117">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccfcd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccfcd-118">-DefaultProfile</span></span>
<span data-ttu-id="ccfcd-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccfcd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccfcd-120">CommonParameters</span></span>
<span data-ttu-id="ccfcd-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccfcd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccfcd-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccfcd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccfcd-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ccfcd-123">INPUTS</span></span>

### <span data-ttu-id="ccfcd-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ccfcd-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="ccfcd-125">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ccfcd-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="ccfcd-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ccfcd-126">OUTPUTS</span></span>

## <span data-ttu-id="ccfcd-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ccfcd-127">NOTES</span></span>

## <span data-ttu-id="ccfcd-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccfcd-128">RELATED LINKS</span></span>

[<span data-ttu-id="ccfcd-129">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ccfcd-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="ccfcd-130">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ccfcd-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="ccfcd-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ccfcd-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


