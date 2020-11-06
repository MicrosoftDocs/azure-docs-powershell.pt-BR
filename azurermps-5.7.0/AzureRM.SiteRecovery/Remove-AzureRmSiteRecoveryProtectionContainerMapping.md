---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 27c90687b212c0ed41dcb080df1be5686a876725
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609904"
---
# <span data-ttu-id="5f1fc-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5f1fc-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="5f1fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f1fc-102">SYNOPSIS</span></span>
<span data-ttu-id="5f1fc-103">Remove um mapeamento de contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5f1fc-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f1fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f1fc-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f1fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f1fc-105">DESCRIPTION</span></span>
<span data-ttu-id="5f1fc-106">O cmdlet **Remove-AzureRmSiteRecoveryProtectionContainerMapping** remove um mapeamento de contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5f1fc-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="5f1fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f1fc-107">EXAMPLES</span></span>

## <span data-ttu-id="5f1fc-108">OS</span><span class="sxs-lookup"><span data-stu-id="5f1fc-108">PARAMETERS</span></span>

### <span data-ttu-id="5f1fc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f1fc-109">-DefaultProfile</span></span>
<span data-ttu-id="5f1fc-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f1fc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f1fc-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5f1fc-111">-Force</span></span>
<span data-ttu-id="5f1fc-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5f1fc-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f1fc-113">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5f1fc-113">-ProtectionContainerMapping</span></span>
<span data-ttu-id="5f1fc-114">Especifica o objeto de mapeamento de contêiner da proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5f1fc-114">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f1fc-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5f1fc-115">-Confirm</span></span>
<span data-ttu-id="5f1fc-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f1fc-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f1fc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f1fc-117">-WhatIf</span></span>
<span data-ttu-id="5f1fc-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5f1fc-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5f1fc-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5f1fc-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f1fc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f1fc-120">CommonParameters</span></span>
<span data-ttu-id="5f1fc-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f1fc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f1fc-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f1fc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f1fc-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f1fc-123">INPUTS</span></span>

### <span data-ttu-id="5f1fc-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5f1fc-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="5f1fc-125">O parâmetro ' ProtectionContainerMapping ' aceita o valor do tipo ' ASRProtectionContainerMapping ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="5f1fc-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="5f1fc-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f1fc-126">OUTPUTS</span></span>

### <span data-ttu-id="5f1fc-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5f1fc-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5f1fc-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f1fc-128">NOTES</span></span>

## <span data-ttu-id="5f1fc-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f1fc-129">RELATED LINKS</span></span>

[<span data-ttu-id="5f1fc-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5f1fc-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="5f1fc-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5f1fc-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
