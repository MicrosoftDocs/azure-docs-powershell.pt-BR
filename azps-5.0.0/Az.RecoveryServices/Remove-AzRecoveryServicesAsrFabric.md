---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 095759ca2753cac4f7155430a241e0554e910fd6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118046"
---
# <span data-ttu-id="52da9-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="52da9-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="52da9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52da9-102">SYNOPSIS</span></span>
<span data-ttu-id="52da9-103">Exclui a malha de recuperação de site do Azure especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="52da9-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="52da9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52da9-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52da9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52da9-105">DESCRIPTION</span></span>
<span data-ttu-id="52da9-106">O cmdlet **Remove-AzRecoveryServicesAsrFabric** remove a estrutura de recuperação de site do Azure especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="52da9-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="52da9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52da9-107">EXAMPLES</span></span>

### <span data-ttu-id="52da9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52da9-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="52da9-109">Inicia a exclusão da malha especificada e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="52da9-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="52da9-110">OS</span><span class="sxs-lookup"><span data-stu-id="52da9-110">PARAMETERS</span></span>

### <span data-ttu-id="52da9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52da9-111">-DefaultProfile</span></span>
<span data-ttu-id="52da9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52da9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="52da9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="52da9-113">-Force</span></span>
<span data-ttu-id="52da9-114">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="52da9-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="52da9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52da9-115">-InputObject</span></span>
<span data-ttu-id="52da9-116">O objeto de entrada para o cmdlet: o objeto de malha ASR correspondente à malha a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="52da9-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="52da9-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52da9-117">-Confirm</span></span>
<span data-ttu-id="52da9-118">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="52da9-118">Specify if confirmation is required.</span></span> <span data-ttu-id="52da9-119">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="52da9-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="52da9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52da9-120">-WhatIf</span></span>
<span data-ttu-id="52da9-121">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52da9-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="52da9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52da9-122">CommonParameters</span></span>
<span data-ttu-id="52da9-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52da9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52da9-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52da9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52da9-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52da9-125">INPUTS</span></span>

### <span data-ttu-id="52da9-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="52da9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="52da9-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52da9-127">OUTPUTS</span></span>

### <span data-ttu-id="52da9-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="52da9-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="52da9-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52da9-129">NOTES</span></span>

## <span data-ttu-id="52da9-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52da9-130">RELATED LINKS</span></span>

[<span data-ttu-id="52da9-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="52da9-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="52da9-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="52da9-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
