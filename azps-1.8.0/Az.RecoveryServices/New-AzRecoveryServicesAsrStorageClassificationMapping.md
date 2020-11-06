---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 152bd9cce3622f0ef0f04049b96791dc08627308
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599663"
---
# <span data-ttu-id="67a7f-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="67a7f-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="67a7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67a7f-102">SYNOPSIS</span></span>
<span data-ttu-id="67a7f-103">Cria um mapeamento de classificação de armazenamento ASR no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="67a7f-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="67a7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67a7f-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67a7f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67a7f-105">DESCRIPTION</span></span>
<span data-ttu-id="67a7f-106">O cmdlet **New-AzRecoveryServicesAsrStorageClassificationMapping** cria um mapeamento de classificação de armazenamento do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="67a7f-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="67a7f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67a7f-107">EXAMPLES</span></span>

### <span data-ttu-id="67a7f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67a7f-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="67a7f-109">Inicia a operação de criação do mapeamento de classificação de armazenamento com os parâmetros especificados e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="67a7f-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="67a7f-110">OS</span><span class="sxs-lookup"><span data-stu-id="67a7f-110">PARAMETERS</span></span>

### <span data-ttu-id="67a7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a7f-111">-DefaultProfile</span></span>
<span data-ttu-id="67a7f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67a7f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="67a7f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="67a7f-113">-Name</span></span>
<span data-ttu-id="67a7f-114">Especifica um nome para o mapeamento de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="67a7f-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="67a7f-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="67a7f-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="67a7f-116">Especifica o objeto de classificação de armazenamento ASR primário para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="67a7f-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="67a7f-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="67a7f-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="67a7f-118">Especifica o objeto de classificação de armazenamento ASR de recuperação para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="67a7f-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="67a7f-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="67a7f-119">-Confirm</span></span>
<span data-ttu-id="67a7f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67a7f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67a7f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a7f-121">-WhatIf</span></span>
<span data-ttu-id="67a7f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67a7f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67a7f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67a7f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67a7f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a7f-124">CommonParameters</span></span>
<span data-ttu-id="67a7f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a7f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a7f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a7f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a7f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67a7f-127">INPUTS</span></span>

### <span data-ttu-id="67a7f-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="67a7f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="67a7f-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67a7f-129">OUTPUTS</span></span>

### <span data-ttu-id="67a7f-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="67a7f-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="67a7f-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67a7f-131">NOTES</span></span>

## <span data-ttu-id="67a7f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67a7f-132">RELATED LINKS</span></span>

[<span data-ttu-id="67a7f-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="67a7f-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="67a7f-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="67a7f-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
