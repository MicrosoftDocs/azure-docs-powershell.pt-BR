---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8ad9ca87687acfdeb526dc33cdcb5a6ec70c65bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885563"
---
# <span data-ttu-id="71d4d-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="71d4d-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="71d4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="71d4d-103">Cria um mapeamento de classificação de armazenamento ASR no cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="71d4d-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="71d4d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="71d4d-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71d4d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="71d4d-105">DESCRIPTION</span></span>
<span data-ttu-id="71d4d-106">O cmdlet **New-AzRecoveryServicesAsrStorageClassificationMapping** cria uma classificação de armazenamento que mapeia o cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="71d4d-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="71d4d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71d4d-107">EXAMPLES</span></span>

### <span data-ttu-id="71d4d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71d4d-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="71d4d-109">Inicia a operação de criação de mapeamento de classificação de armazenamento com os parâmetros especificados e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="71d4d-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="71d4d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="71d4d-110">PARAMETERS</span></span>

### <span data-ttu-id="71d4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d4d-111">-DefaultProfile</span></span>
<span data-ttu-id="71d4d-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71d4d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="71d4d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="71d4d-113">-Name</span></span>
<span data-ttu-id="71d4d-114">Especifica um nome para o mapeamento de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="71d4d-114">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d4d-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="71d4d-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="71d4d-116">Especifica o objeto de classificação de armazenamento ASR principal para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="71d4d-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71d4d-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="71d4d-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="71d4d-118">Especifica o objeto de classificação de armazenamento ASR de recuperação para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="71d4d-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d4d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71d4d-119">-Confirm</span></span>
<span data-ttu-id="71d4d-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71d4d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71d4d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71d4d-121">-WhatIf</span></span>
<span data-ttu-id="71d4d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71d4d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71d4d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71d4d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71d4d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d4d-124">CommonParameters</span></span>
<span data-ttu-id="71d4d-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71d4d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d4d-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71d4d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d4d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71d4d-127">INPUTS</span></span>

### <span data-ttu-id="71d4d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="71d4d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="71d4d-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="71d4d-129">OUTPUTS</span></span>

### <span data-ttu-id="71d4d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="71d4d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="71d4d-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="71d4d-131">NOTES</span></span>

## <span data-ttu-id="71d4d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71d4d-132">RELATED LINKS</span></span>

[<span data-ttu-id="71d4d-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="71d4d-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="71d4d-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="71d4d-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
