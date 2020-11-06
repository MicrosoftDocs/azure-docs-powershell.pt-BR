---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 3d4530090bc1386a34056b315c79a826be5d771f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430619"
---
# <span data-ttu-id="6ca68-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="6ca68-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="6ca68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ca68-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca68-103">Remove uma malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6ca68-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ca68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ca68-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca68-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ca68-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca68-106">O cmdlet **Remove-AzureRmSiteRecoveryFabric** remove uma malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6ca68-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="6ca68-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ca68-107">EXAMPLES</span></span>

## <span data-ttu-id="6ca68-108">OS</span><span class="sxs-lookup"><span data-stu-id="6ca68-108">PARAMETERS</span></span>

### <span data-ttu-id="6ca68-109">-Fabric</span><span class="sxs-lookup"><span data-stu-id="6ca68-109">-Fabric</span></span>
<span data-ttu-id="6ca68-110">Especifica o objeto da malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6ca68-110">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca68-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6ca68-111">-Force</span></span>
<span data-ttu-id="6ca68-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6ca68-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6ca68-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6ca68-113">-Confirm</span></span>
<span data-ttu-id="6ca68-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca68-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca68-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca68-115">-WhatIf</span></span>
<span data-ttu-id="6ca68-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ca68-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6ca68-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ca68-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca68-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca68-118">-DefaultProfile</span></span>
<span data-ttu-id="6ca68-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca68-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ca68-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca68-120">CommonParameters</span></span>
<span data-ttu-id="6ca68-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca68-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca68-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca68-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca68-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ca68-123">INPUTS</span></span>

### <span data-ttu-id="6ca68-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6ca68-124">ASRFabric</span></span>
<span data-ttu-id="6ca68-125">O parâmetro ' Fabric ' aceita o valor do tipo ' ASRFabric ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="6ca68-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="6ca68-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ca68-126">OUTPUTS</span></span>

### <span data-ttu-id="6ca68-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6ca68-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6ca68-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ca68-128">NOTES</span></span>

## <span data-ttu-id="6ca68-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ca68-129">RELATED LINKS</span></span>

[<span data-ttu-id="6ca68-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="6ca68-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="6ca68-131">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="6ca68-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
