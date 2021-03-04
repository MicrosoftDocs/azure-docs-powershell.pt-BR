---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: c1b5623e185c10471da674c21995917c169e5ffa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885543"
---
# <span data-ttu-id="c26ba-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c26ba-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="c26ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c26ba-102">SYNOPSIS</span></span>
<span data-ttu-id="c26ba-103">Exclui o Contêiner de Proteção especificado de seu Fabric.</span><span class="sxs-lookup"><span data-stu-id="c26ba-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="c26ba-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c26ba-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c26ba-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c26ba-105">DESCRIPTION</span></span>
<span data-ttu-id="c26ba-106">O Remove-AzRecoveryServicesAsrProtectionContainer cmdlet exclui o Contêiner de Proteção de Recuperação de Site especificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="c26ba-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="c26ba-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c26ba-107">EXAMPLES</span></span>

### <span data-ttu-id="c26ba-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c26ba-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="c26ba-109">Inicia a exclusão do contêiner de proteção especificado e retorna o trabalho ASR usado para rastrear a operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="c26ba-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="c26ba-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c26ba-110">PARAMETERS</span></span>

### <span data-ttu-id="c26ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26ba-111">-DefaultProfile</span></span>
<span data-ttu-id="c26ba-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c26ba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c26ba-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c26ba-113">-InputObject</span></span>
<span data-ttu-id="c26ba-114">Especifica o contêiner de proteção a ser removido .</span><span class="sxs-lookup"><span data-stu-id="c26ba-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="c26ba-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c26ba-115">-Confirm</span></span>
<span data-ttu-id="c26ba-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c26ba-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c26ba-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c26ba-117">-WhatIf</span></span>
<span data-ttu-id="c26ba-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c26ba-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c26ba-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c26ba-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c26ba-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26ba-120">CommonParameters</span></span>
<span data-ttu-id="c26ba-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c26ba-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26ba-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c26ba-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26ba-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c26ba-123">INPUTS</span></span>

### <span data-ttu-id="c26ba-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c26ba-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="c26ba-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c26ba-125">OUTPUTS</span></span>

### <span data-ttu-id="c26ba-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c26ba-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c26ba-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="c26ba-127">NOTES</span></span>

## <span data-ttu-id="c26ba-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c26ba-128">RELATED LINKS</span></span>
