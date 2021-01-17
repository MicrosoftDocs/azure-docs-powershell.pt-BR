---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428784"
---
# <span data-ttu-id="72fd9-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="72fd9-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="72fd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="72fd9-103">Exclui o contêiner de proteção especificado da malha.</span><span class="sxs-lookup"><span data-stu-id="72fd9-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="72fd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72fd9-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72fd9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72fd9-105">DESCRIPTION</span></span>
<span data-ttu-id="72fd9-106">O cmdlet Remove-AzRecoveryServicesAsrProtectionContainer exclui o contêiner de proteção do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="72fd9-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="72fd9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72fd9-107">EXAMPLES</span></span>

### <span data-ttu-id="72fd9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72fd9-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="72fd9-109">Inicia a exclusão do contêiner de proteção especificado e retorna o trabalho ASR usado para acompanhar a operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="72fd9-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="72fd9-110">OS</span><span class="sxs-lookup"><span data-stu-id="72fd9-110">PARAMETERS</span></span>

### <span data-ttu-id="72fd9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72fd9-111">-DefaultProfile</span></span>
<span data-ttu-id="72fd9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="72fd9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72fd9-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72fd9-113">-InputObject</span></span>
<span data-ttu-id="72fd9-114">Especifica o contêiner de proteção a ser removido.</span><span class="sxs-lookup"><span data-stu-id="72fd9-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="72fd9-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="72fd9-115">-Confirm</span></span>
<span data-ttu-id="72fd9-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72fd9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72fd9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72fd9-117">-WhatIf</span></span>
<span data-ttu-id="72fd9-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="72fd9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72fd9-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72fd9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72fd9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fd9-120">CommonParameters</span></span>
<span data-ttu-id="72fd9-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72fd9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fd9-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72fd9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fd9-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72fd9-123">INPUTS</span></span>

### <span data-ttu-id="72fd9-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="72fd9-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="72fd9-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72fd9-125">OUTPUTS</span></span>

### <span data-ttu-id="72fd9-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="72fd9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="72fd9-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72fd9-127">NOTES</span></span>

## <span data-ttu-id="72fd9-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72fd9-128">RELATED LINKS</span></span>
