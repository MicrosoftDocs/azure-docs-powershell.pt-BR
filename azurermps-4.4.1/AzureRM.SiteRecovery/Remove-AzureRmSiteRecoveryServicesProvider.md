---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e7ee32974ef87b86d443d90b7dc628f9c9f1072f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429071"
---
# <span data-ttu-id="e809b-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e809b-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="e809b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e809b-102">SYNOPSIS</span></span>
<span data-ttu-id="e809b-103">Remove um provedor de serviços de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="e809b-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e809b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e809b-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e809b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e809b-105">DESCRIPTION</span></span>
<span data-ttu-id="e809b-106">O cmdlet **Remove-AzureRmSiteRecoveryServicesProvider** remove um provedor de serviços de recuperação de site do Azure do cofre.</span><span class="sxs-lookup"><span data-stu-id="e809b-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="e809b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e809b-107">EXAMPLES</span></span>

## <span data-ttu-id="e809b-108">OS</span><span class="sxs-lookup"><span data-stu-id="e809b-108">PARAMETERS</span></span>

### <span data-ttu-id="e809b-109">-Force</span><span class="sxs-lookup"><span data-stu-id="e809b-109">-Force</span></span>
<span data-ttu-id="e809b-110">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e809b-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e809b-111">-Servicesprovider</span><span class="sxs-lookup"><span data-stu-id="e809b-111">-ServicesProvider</span></span>
<span data-ttu-id="e809b-112">Especifica o objeto provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="e809b-112">Specifies the Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e809b-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e809b-113">-Confirm</span></span>
<span data-ttu-id="e809b-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e809b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e809b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e809b-115">-WhatIf</span></span>
<span data-ttu-id="e809b-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e809b-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e809b-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e809b-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e809b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e809b-118">-DefaultProfile</span></span>
<span data-ttu-id="e809b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e809b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e809b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e809b-120">CommonParameters</span></span>
<span data-ttu-id="e809b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e809b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e809b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e809b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e809b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e809b-123">INPUTS</span></span>

### <span data-ttu-id="e809b-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e809b-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="e809b-125">O parâmetro ' Servicesprovider ' aceita o valor do tipo ' ASRRecoveryServicesProvider ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="e809b-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="e809b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e809b-126">OUTPUTS</span></span>

### <span data-ttu-id="e809b-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRJob, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e809b-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e809b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e809b-128">NOTES</span></span>

## <span data-ttu-id="e809b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e809b-129">RELATED LINKS</span></span>

[<span data-ttu-id="e809b-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e809b-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="e809b-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e809b-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
