---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 0cc4a1c58349157024f38bce6e5ee2d8bcaa3cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440305"
---
# <span data-ttu-id="ba43b-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ba43b-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="ba43b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba43b-102">SYNOPSIS</span></span>
<span data-ttu-id="ba43b-103">Exclui o contêiner de proteção especificado da malha.</span><span class="sxs-lookup"><span data-stu-id="ba43b-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba43b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba43b-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba43b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba43b-105">DESCRIPTION</span></span>
<span data-ttu-id="ba43b-106">O cmdlet Remove-AzureRmRecoveryServicesAsrProtectionContainer exclui o contêiner de proteção do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="ba43b-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="ba43b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba43b-107">EXAMPLES</span></span>

### <span data-ttu-id="ba43b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ba43b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="ba43b-109">Inicia a exclusão do contêiner de proteção especificado e retorna o trabalho ASR usado para acompanhar a operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="ba43b-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="ba43b-110">OS</span><span class="sxs-lookup"><span data-stu-id="ba43b-110">PARAMETERS</span></span>

### <span data-ttu-id="ba43b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba43b-111">-DefaultProfile</span></span>
<span data-ttu-id="ba43b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba43b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba43b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba43b-113">-InputObject</span></span>
<span data-ttu-id="ba43b-114">Especifica o contêiner de proteção a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ba43b-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba43b-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ba43b-115">-Confirm</span></span>
<span data-ttu-id="ba43b-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba43b-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba43b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba43b-117">-WhatIf</span></span>
<span data-ttu-id="ba43b-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ba43b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba43b-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba43b-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba43b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba43b-120">CommonParameters</span></span>
<span data-ttu-id="ba43b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba43b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba43b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba43b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba43b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba43b-123">INPUTS</span></span>

### <span data-ttu-id="ba43b-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ba43b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="ba43b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba43b-125">OUTPUTS</span></span>

### <span data-ttu-id="ba43b-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ba43b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ba43b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba43b-127">NOTES</span></span>

## <span data-ttu-id="ba43b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba43b-128">RELATED LINKS</span></span>