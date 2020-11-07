---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c76c2ebf40f360820ec3eef719b33142daacdbac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773463"
---
# <span data-ttu-id="0ab21-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0ab21-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="0ab21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ab21-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab21-103">Exclui o mapeamento de classificação de armazenamento ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="0ab21-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="0ab21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ab21-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ab21-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ab21-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab21-106">O cmdlet **Remove-AzRecoveryServicesAsrStorageClassificationMapping** exclui o mapeamento de classificação de armazenamento do Azure site Recovery especificado.</span><span class="sxs-lookup"><span data-stu-id="0ab21-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="0ab21-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ab21-107">EXAMPLES</span></span>

### <span data-ttu-id="0ab21-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0ab21-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="0ab21-109">Inicia a exclusão do mapeamento de classificação de armazenamento especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="0ab21-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0ab21-110">OS</span><span class="sxs-lookup"><span data-stu-id="0ab21-110">PARAMETERS</span></span>

### <span data-ttu-id="0ab21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab21-111">-DefaultProfile</span></span>
<span data-ttu-id="0ab21-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab21-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0ab21-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ab21-113">-InputObject</span></span>
<span data-ttu-id="0ab21-114">O objeto de entrada para o cmdlet: o objeto de mapeamento de classificação de armazenamento ASR correspondente ao mapeamento de classificação de armazenamento ASR a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="0ab21-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="0ab21-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0ab21-115">-Confirm</span></span>
<span data-ttu-id="0ab21-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ab21-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ab21-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ab21-117">-WhatIf</span></span>
<span data-ttu-id="0ab21-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0ab21-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ab21-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0ab21-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ab21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab21-120">CommonParameters</span></span>
<span data-ttu-id="0ab21-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab21-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab21-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab21-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ab21-123">INPUTS</span></span>

### <span data-ttu-id="0ab21-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0ab21-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="0ab21-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ab21-125">OUTPUTS</span></span>

### <span data-ttu-id="0ab21-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0ab21-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0ab21-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ab21-127">NOTES</span></span>

## <span data-ttu-id="0ab21-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ab21-128">RELATED LINKS</span></span>

[<span data-ttu-id="0ab21-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0ab21-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="0ab21-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0ab21-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
