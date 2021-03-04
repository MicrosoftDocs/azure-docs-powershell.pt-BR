---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: b19808ff7b5576c93bc81414d665e23086e524d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885528"
---
# <span data-ttu-id="02103-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="02103-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="02103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02103-102">SYNOPSIS</span></span>
<span data-ttu-id="02103-103">Exclui o mapeamento de classificação de armazenamento ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="02103-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="02103-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="02103-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02103-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="02103-105">DESCRIPTION</span></span>
<span data-ttu-id="02103-106">O cmdlet **Remove-AzRecoveryServicesAsrStorageClassificationMapping** exclui o mapeamento de classificação de armazenamento de Recuperação de Site especificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="02103-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="02103-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02103-107">EXAMPLES</span></span>

### <span data-ttu-id="02103-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02103-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="02103-109">Inicia a exclusão do mapeamento de classificação de armazenamento especificado e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="02103-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="02103-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="02103-110">PARAMETERS</span></span>

### <span data-ttu-id="02103-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02103-111">-DefaultProfile</span></span>
<span data-ttu-id="02103-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02103-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="02103-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02103-113">-InputObject</span></span>
<span data-ttu-id="02103-114">O objeto de entrada para o cmdlet: o objeto de mapeamento de classificação de armazenamento ASR correspondente ao mapeamento de classificação de armazenamento ASR a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="02103-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02103-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02103-115">-Confirm</span></span>
<span data-ttu-id="02103-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02103-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02103-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02103-117">-WhatIf</span></span>
<span data-ttu-id="02103-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02103-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02103-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02103-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02103-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02103-120">CommonParameters</span></span>
<span data-ttu-id="02103-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02103-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02103-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02103-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02103-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02103-123">INPUTS</span></span>

### <span data-ttu-id="02103-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="02103-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="02103-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="02103-125">OUTPUTS</span></span>

### <span data-ttu-id="02103-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="02103-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="02103-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="02103-127">NOTES</span></span>

## <span data-ttu-id="02103-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02103-128">RELATED LINKS</span></span>

[<span data-ttu-id="02103-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="02103-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="02103-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="02103-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
