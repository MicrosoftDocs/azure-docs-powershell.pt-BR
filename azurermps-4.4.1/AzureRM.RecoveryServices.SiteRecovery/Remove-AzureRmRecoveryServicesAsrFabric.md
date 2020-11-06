---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 3f380110359668af5c1b506e1736d3ecc9f39b3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429157"
---
# <span data-ttu-id="fcddc-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="fcddc-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="fcddc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcddc-102">SYNOPSIS</span></span>
<span data-ttu-id="fcddc-103">Exclui a malha de recuperação de site do Azure especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fcddc-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcddc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcddc-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcddc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcddc-105">DESCRIPTION</span></span>
<span data-ttu-id="fcddc-106">O cmdlet **Remove-AzureRmRecoveryServicesAsrFabric** remove a estrutura de recuperação de site do Azure especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="fcddc-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="fcddc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcddc-107">EXAMPLES</span></span>

### <span data-ttu-id="fcddc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fcddc-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="fcddc-109">Inicia a exclusão da malha especificada e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="fcddc-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fcddc-110">OS</span><span class="sxs-lookup"><span data-stu-id="fcddc-110">PARAMETERS</span></span>

### <span data-ttu-id="fcddc-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fcddc-111">-Force</span></span>
<span data-ttu-id="fcddc-112">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="fcddc-112">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcddc-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcddc-113">-InputObject</span></span>
<span data-ttu-id="fcddc-114">O objeto de entrada para o cmdlet: o objeto de malha ASR correspondente à malha a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="fcddc-114">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcddc-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fcddc-115">-Confirm</span></span>
<span data-ttu-id="fcddc-116">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="fcddc-116">Specify if confirmation is required.</span></span> <span data-ttu-id="fcddc-117">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="fcddc-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcddc-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcddc-118">-WhatIf</span></span>
<span data-ttu-id="fcddc-119">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcddc-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcddc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcddc-120">CommonParameters</span></span>
<span data-ttu-id="fcddc-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcddc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcddc-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcddc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcddc-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcddc-123">INPUTS</span></span>

### <span data-ttu-id="fcddc-124">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="fcddc-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="fcddc-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcddc-125">OUTPUTS</span></span>

### <span data-ttu-id="fcddc-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fcddc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fcddc-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcddc-127">NOTES</span></span>

## <span data-ttu-id="fcddc-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcddc-128">RELATED LINKS</span></span>

[<span data-ttu-id="fcddc-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="fcddc-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="fcddc-130">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="fcddc-130">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
