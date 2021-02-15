---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112690"
---
# <span data-ttu-id="92290-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="92290-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="92290-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92290-102">SYNOPSIS</span></span>
<span data-ttu-id="92290-103">Exclui o Contêiner de Proteção especificado de sua Malha.</span><span class="sxs-lookup"><span data-stu-id="92290-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="92290-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92290-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92290-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="92290-105">DESCRIPTION</span></span>
<span data-ttu-id="92290-106">O Remove-AzRecoveryServicesAsrProtectionContainer cmdlet exclui o Contêiner de Proteção de Recuperação de Site do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="92290-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="92290-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="92290-107">EXAMPLES</span></span>

### <span data-ttu-id="92290-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="92290-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="92290-109">Inicia a exclusão do contêiner de proteção especificado e retorna o trabalho ASR usado para controlar a operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="92290-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="92290-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92290-110">PARAMETERS</span></span>

### <span data-ttu-id="92290-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92290-111">-DefaultProfile</span></span>
<span data-ttu-id="92290-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92290-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92290-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92290-113">-InputObject</span></span>
<span data-ttu-id="92290-114">Especifica o contêiner de proteção a ser removido.</span><span class="sxs-lookup"><span data-stu-id="92290-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="92290-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="92290-115">-Confirm</span></span>
<span data-ttu-id="92290-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92290-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92290-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92290-117">-WhatIf</span></span>
<span data-ttu-id="92290-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="92290-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92290-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92290-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92290-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92290-120">CommonParameters</span></span>
<span data-ttu-id="92290-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92290-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92290-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92290-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92290-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="92290-123">INPUTS</span></span>

### <span data-ttu-id="92290-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="92290-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="92290-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="92290-125">OUTPUTS</span></span>

### <span data-ttu-id="92290-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="92290-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="92290-127">Notas</span><span class="sxs-lookup"><span data-stu-id="92290-127">NOTES</span></span>

## <span data-ttu-id="92290-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92290-128">RELATED LINKS</span></span>
