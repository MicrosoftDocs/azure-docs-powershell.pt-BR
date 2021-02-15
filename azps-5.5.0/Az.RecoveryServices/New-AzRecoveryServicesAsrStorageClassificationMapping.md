---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118186"
---
# <span data-ttu-id="78932-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="78932-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="78932-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78932-102">SYNOPSIS</span></span>
<span data-ttu-id="78932-103">Cria um mapeamento de classificação de armazenamento ASR no cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="78932-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="78932-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78932-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78932-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="78932-105">DESCRIPTION</span></span>
<span data-ttu-id="78932-106">O cmdlet **New-AzRecoveryServicesAsrStorageClassificationMapping** cria um mapeamento de classificação de armazenamento do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="78932-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="78932-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="78932-107">EXAMPLES</span></span>

### <span data-ttu-id="78932-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78932-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="78932-109">Inicia a operação de criação de mapeamento de classificação de armazenamento com os parâmetros especificados e retorna o trabalho ASR usado para controlar a operação.</span><span class="sxs-lookup"><span data-stu-id="78932-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="78932-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78932-110">PARAMETERS</span></span>

### <span data-ttu-id="78932-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78932-111">-DefaultProfile</span></span>
<span data-ttu-id="78932-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78932-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="78932-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="78932-113">-Name</span></span>
<span data-ttu-id="78932-114">Especifica um nome para o mapeamento de classificação de armazenamento ASR.</span><span class="sxs-lookup"><span data-stu-id="78932-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="78932-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="78932-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="78932-116">Especifica o objeto de classificação de armazenamento ASR principal para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="78932-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="78932-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="78932-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="78932-118">Especifica o objeto de classificação de armazenamento ASR de recuperação para o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="78932-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="78932-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="78932-119">-Confirm</span></span>
<span data-ttu-id="78932-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78932-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78932-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78932-121">-WhatIf</span></span>
<span data-ttu-id="78932-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="78932-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78932-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78932-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78932-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78932-124">CommonParameters</span></span>
<span data-ttu-id="78932-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78932-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78932-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78932-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78932-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="78932-127">INPUTS</span></span>

### <span data-ttu-id="78932-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="78932-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="78932-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="78932-129">OUTPUTS</span></span>

### <span data-ttu-id="78932-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="78932-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="78932-131">Notas</span><span class="sxs-lookup"><span data-stu-id="78932-131">NOTES</span></span>

## <span data-ttu-id="78932-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78932-132">RELATED LINKS</span></span>

[<span data-ttu-id="78932-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="78932-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="78932-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="78932-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
