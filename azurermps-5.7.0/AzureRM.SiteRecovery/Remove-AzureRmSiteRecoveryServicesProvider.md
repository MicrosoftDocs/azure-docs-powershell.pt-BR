---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 88b6b83f24edb06871fd87f61fec1732893b0f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426600"
---
# <span data-ttu-id="173f2-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="173f2-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="173f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="173f2-102">SYNOPSIS</span></span>
<span data-ttu-id="173f2-103">Remove um provedor de serviços de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="173f2-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="173f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="173f2-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="173f2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="173f2-105">DESCRIPTION</span></span>
<span data-ttu-id="173f2-106">O cmdlet **Remove-AzureRmSiteRecoveryServicesProvider** remove um provedor de serviços de recuperação de site do Azure do cofre.</span><span class="sxs-lookup"><span data-stu-id="173f2-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="173f2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="173f2-107">EXAMPLES</span></span>

## <span data-ttu-id="173f2-108">OS</span><span class="sxs-lookup"><span data-stu-id="173f2-108">PARAMETERS</span></span>

### <span data-ttu-id="173f2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="173f2-109">-DefaultProfile</span></span>
<span data-ttu-id="173f2-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="173f2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="173f2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="173f2-111">-Force</span></span>
<span data-ttu-id="173f2-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="173f2-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="173f2-113">-Servicesprovider</span><span class="sxs-lookup"><span data-stu-id="173f2-113">-ServicesProvider</span></span>
<span data-ttu-id="173f2-114">Especifica o objeto provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="173f2-114">Specifies the Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="173f2-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="173f2-115">-Confirm</span></span>
<span data-ttu-id="173f2-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="173f2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="173f2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="173f2-117">-WhatIf</span></span>
<span data-ttu-id="173f2-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="173f2-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="173f2-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="173f2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="173f2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="173f2-120">CommonParameters</span></span>
<span data-ttu-id="173f2-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="173f2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="173f2-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="173f2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="173f2-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="173f2-123">INPUTS</span></span>

### <span data-ttu-id="173f2-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="173f2-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="173f2-125">O parâmetro ' Servicesprovider ' aceita o valor do tipo ' ASRRecoveryServicesProvider ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="173f2-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="173f2-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="173f2-126">OUTPUTS</span></span>

### <span data-ttu-id="173f2-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRJob, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="173f2-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="173f2-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="173f2-128">NOTES</span></span>

## <span data-ttu-id="173f2-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="173f2-129">RELATED LINKS</span></span>

[<span data-ttu-id="173f2-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="173f2-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="173f2-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="173f2-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
