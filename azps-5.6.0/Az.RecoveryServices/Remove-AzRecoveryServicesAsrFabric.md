---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: ed06852e2ce0342502d01bd7f5ae17c0c3b8f4e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885547"
---
# <span data-ttu-id="c89ed-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c89ed-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="c89ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c89ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c89ed-103">Exclui o Azure Site Recovery Fabric especificado do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="c89ed-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="c89ed-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c89ed-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c89ed-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c89ed-105">DESCRIPTION</span></span>
<span data-ttu-id="c89ed-106">O cmdlet **Remove-AzRecoveryServicesAsrFabric** remove o tecido especificado de Recuperação de Site do Azure do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c89ed-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="c89ed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c89ed-107">EXAMPLES</span></span>

### <span data-ttu-id="c89ed-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c89ed-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="c89ed-109">Inicia a exclusão de malha especificada e retorna o trabalho ASR usado para rastrear a operação.</span><span class="sxs-lookup"><span data-stu-id="c89ed-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c89ed-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c89ed-110">PARAMETERS</span></span>

### <span data-ttu-id="c89ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c89ed-111">-DefaultProfile</span></span>
<span data-ttu-id="c89ed-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c89ed-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c89ed-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c89ed-113">-Force</span></span>
<span data-ttu-id="c89ed-114">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="c89ed-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c89ed-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c89ed-115">-InputObject</span></span>
<span data-ttu-id="c89ed-116">O objeto de entrada para o cmdlet: o objeto de malha ASR correspondente ao tecido a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c89ed-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c89ed-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c89ed-117">-Confirm</span></span>
<span data-ttu-id="c89ed-118">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="c89ed-118">Specify if confirmation is required.</span></span> <span data-ttu-id="c89ed-119">De definir o valor do parâmetro confirme como $false para ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="c89ed-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="c89ed-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c89ed-120">-WhatIf</span></span>
<span data-ttu-id="c89ed-121">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c89ed-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="c89ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c89ed-122">CommonParameters</span></span>
<span data-ttu-id="c89ed-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c89ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c89ed-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c89ed-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c89ed-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c89ed-125">INPUTS</span></span>

### <span data-ttu-id="c89ed-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c89ed-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c89ed-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c89ed-127">OUTPUTS</span></span>

### <span data-ttu-id="c89ed-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c89ed-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c89ed-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="c89ed-129">NOTES</span></span>

## <span data-ttu-id="c89ed-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c89ed-130">RELATED LINKS</span></span>

[<span data-ttu-id="c89ed-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c89ed-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="c89ed-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c89ed-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
