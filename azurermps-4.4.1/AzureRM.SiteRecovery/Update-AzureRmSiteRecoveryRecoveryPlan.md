---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: d497938a8a68d3efc6cafd1640de8d0be738b113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610709"
---
# <span data-ttu-id="292ba-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="292ba-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="292ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="292ba-102">SYNOPSIS</span></span>
<span data-ttu-id="292ba-103">Atualiza um plano de recuperação na recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="292ba-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="292ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="292ba-104">SYNTAX</span></span>

### <span data-ttu-id="292ba-105">ByRPObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="292ba-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="292ba-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="292ba-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="292ba-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="292ba-107">DESCRIPTION</span></span>
<span data-ttu-id="292ba-108">O cmdlet **Update-AzureRmSiteRecoveryRecoveryPlan** atualiza um plano de recuperação no Azure site Recovery e, em seguida, o publica.</span><span class="sxs-lookup"><span data-stu-id="292ba-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="292ba-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="292ba-109">EXAMPLES</span></span>

### <span data-ttu-id="292ba-110">Exemplo 1: atualizar um plano de recuperação</span><span class="sxs-lookup"><span data-stu-id="292ba-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="292ba-111">Esse comando atualiza o plano de recuperação especificado e o publica.</span><span class="sxs-lookup"><span data-stu-id="292ba-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="292ba-112">OS</span><span class="sxs-lookup"><span data-stu-id="292ba-112">PARAMETERS</span></span>

### <span data-ttu-id="292ba-113">-Caminho</span><span class="sxs-lookup"><span data-stu-id="292ba-113">-Path</span></span>
<span data-ttu-id="292ba-114">Especifica o caminho do arquivo de plano de recuperação do plano de recuperação que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="292ba-114">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="292ba-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="292ba-115">-RecoveryPlan</span></span>
<span data-ttu-id="292ba-116">Especifica um plano de recuperação que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="292ba-116">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="292ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="292ba-117">-DefaultProfile</span></span>
<span data-ttu-id="292ba-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="292ba-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="292ba-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="292ba-119">CommonParameters</span></span>
<span data-ttu-id="292ba-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="292ba-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="292ba-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="292ba-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="292ba-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="292ba-122">INPUTS</span></span>

### <span data-ttu-id="292ba-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="292ba-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="292ba-124">O parâmetro ' RecoveryPlan ' aceita o valor do tipo ' ASRRecoveryPlan ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="292ba-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="292ba-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="292ba-125">OUTPUTS</span></span>

## <span data-ttu-id="292ba-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="292ba-126">NOTES</span></span>

## <span data-ttu-id="292ba-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="292ba-127">RELATED LINKS</span></span>

[<span data-ttu-id="292ba-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="292ba-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="292ba-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="292ba-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="292ba-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="292ba-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


