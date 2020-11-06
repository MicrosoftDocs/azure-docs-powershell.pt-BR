---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 2d9f087b87d99003b559fc363265fdb4b996c3f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429073"
---
# <span data-ttu-id="62213-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="62213-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="62213-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62213-102">SYNOPSIS</span></span>
<span data-ttu-id="62213-103">Obtém um plano de recuperação na recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="62213-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62213-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62213-104">SYNTAX</span></span>

### <span data-ttu-id="62213-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="62213-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62213-106">ByName</span><span class="sxs-lookup"><span data-stu-id="62213-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62213-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="62213-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62213-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62213-108">DESCRIPTION</span></span>
<span data-ttu-id="62213-109">O cmdlet **Get-AzureRmSiteRecoveryRecoveryPlan** Obtém um plano de recuperação no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="62213-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="62213-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62213-110">EXAMPLES</span></span>

## <span data-ttu-id="62213-111">OS</span><span class="sxs-lookup"><span data-stu-id="62213-111">PARAMETERS</span></span>

### <span data-ttu-id="62213-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="62213-112">-FriendlyName</span></span>
<span data-ttu-id="62213-113">Especifica o nome amigável do plano de recuperação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="62213-113">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="62213-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="62213-114">-Name</span></span>
<span data-ttu-id="62213-115">Especifica o nome do plano de recuperação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="62213-115">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="62213-116">-Caminho</span><span class="sxs-lookup"><span data-stu-id="62213-116">-Path</span></span>
<span data-ttu-id="62213-117">Especifica o caminho de arquivo para o qual esse cmdlet salva o plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="62213-117">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62213-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62213-118">-DefaultProfile</span></span>
<span data-ttu-id="62213-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62213-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62213-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62213-120">CommonParameters</span></span>
<span data-ttu-id="62213-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62213-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62213-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62213-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62213-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62213-123">INPUTS</span></span>

## <span data-ttu-id="62213-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62213-124">OUTPUTS</span></span>

### <span data-ttu-id="62213-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPlan]</span><span class="sxs-lookup"><span data-stu-id="62213-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="62213-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62213-126">NOTES</span></span>

## <span data-ttu-id="62213-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62213-127">RELATED LINKS</span></span>

[<span data-ttu-id="62213-128">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="62213-128">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="62213-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="62213-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="62213-130">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="62213-130">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
