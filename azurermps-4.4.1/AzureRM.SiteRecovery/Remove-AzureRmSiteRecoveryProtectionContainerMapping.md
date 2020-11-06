---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: a0de6cc5594b019275cb14785cbae3b969d44301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602682"
---
# <span data-ttu-id="6a2ef-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6a2ef-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="6a2ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a2ef-102">SYNOPSIS</span></span>
<span data-ttu-id="6a2ef-103">Remove um mapeamento de contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6a2ef-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a2ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a2ef-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a2ef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a2ef-105">DESCRIPTION</span></span>
<span data-ttu-id="6a2ef-106">O cmdlet **Remove-AzureRmSiteRecoveryProtectionContainerMapping** remove um mapeamento de contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6a2ef-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="6a2ef-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a2ef-107">EXAMPLES</span></span>

## <span data-ttu-id="6a2ef-108">OS</span><span class="sxs-lookup"><span data-stu-id="6a2ef-108">PARAMETERS</span></span>

### <span data-ttu-id="6a2ef-109">-Force</span><span class="sxs-lookup"><span data-stu-id="6a2ef-109">-Force</span></span>
<span data-ttu-id="6a2ef-110">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6a2ef-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ef-111">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6a2ef-111">-ProtectionContainerMapping</span></span>
<span data-ttu-id="6a2ef-112">Especifica o objeto de mapeamento de contêiner da proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6a2ef-112">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ef-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6a2ef-113">-Confirm</span></span>
<span data-ttu-id="6a2ef-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a2ef-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ef-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a2ef-115">-WhatIf</span></span>
<span data-ttu-id="6a2ef-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6a2ef-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6a2ef-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a2ef-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a2ef-118">-DefaultProfile</span></span>
<span data-ttu-id="6a2ef-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a2ef-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a2ef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a2ef-120">CommonParameters</span></span>
<span data-ttu-id="6a2ef-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a2ef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a2ef-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a2ef-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a2ef-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a2ef-123">INPUTS</span></span>

### <span data-ttu-id="6a2ef-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6a2ef-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="6a2ef-125">O parâmetro ' ProtectionContainerMapping ' aceita o valor do tipo ' ASRProtectionContainerMapping ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6a2ef-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="6a2ef-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a2ef-126">OUTPUTS</span></span>

### <span data-ttu-id="6a2ef-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6a2ef-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6a2ef-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a2ef-128">NOTES</span></span>

## <span data-ttu-id="6a2ef-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a2ef-129">RELATED LINKS</span></span>

[<span data-ttu-id="6a2ef-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6a2ef-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="6a2ef-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="6a2ef-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
