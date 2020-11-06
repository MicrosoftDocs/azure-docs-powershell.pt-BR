---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: f052b11a11fa77047d424b7045b127a75043cc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603316"
---
# <span data-ttu-id="e2d6f-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e2d6f-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="e2d6f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d6f-103">Remove um site de recuperação do site do cofre atual.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2d6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2d6f-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2d6f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="e2d6f-106">O cmdlet **Remove-AzureRmSiteRecoverySite** exclui um site de recuperação de site do Azure do cofre atual.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="e2d6f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2d6f-107">EXAMPLES</span></span>

## <span data-ttu-id="e2d6f-108">OS</span><span class="sxs-lookup"><span data-stu-id="e2d6f-108">PARAMETERS</span></span>

### <span data-ttu-id="e2d6f-109">-Force</span><span class="sxs-lookup"><span data-stu-id="e2d6f-109">-Force</span></span>
<span data-ttu-id="e2d6f-110">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e2d6f-111">-Site</span><span class="sxs-lookup"><span data-stu-id="e2d6f-111">-Site</span></span>
<span data-ttu-id="e2d6f-112">Especifica o objeto de site de recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-112">Specifies the Site Recovery site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d6f-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2d6f-113">-Confirm</span></span>
<span data-ttu-id="e2d6f-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2d6f-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d6f-115">-WhatIf</span></span>
<span data-ttu-id="e2d6f-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e2d6f-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2d6f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d6f-118">-DefaultProfile</span></span>
<span data-ttu-id="e2d6f-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2d6f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d6f-120">CommonParameters</span></span>
<span data-ttu-id="e2d6f-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2d6f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d6f-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d6f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d6f-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2d6f-123">INPUTS</span></span>

### <span data-ttu-id="e2d6f-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="e2d6f-124">ASRSite</span></span>
<span data-ttu-id="e2d6f-125">O parâmetro ' site ' aceita o valor do tipo ' ASRSite ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="e2d6f-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="e2d6f-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2d6f-126">OUTPUTS</span></span>

## <span data-ttu-id="e2d6f-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2d6f-127">NOTES</span></span>

## <span data-ttu-id="e2d6f-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2d6f-128">RELATED LINKS</span></span>

[<span data-ttu-id="e2d6f-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e2d6f-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="e2d6f-130">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e2d6f-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
