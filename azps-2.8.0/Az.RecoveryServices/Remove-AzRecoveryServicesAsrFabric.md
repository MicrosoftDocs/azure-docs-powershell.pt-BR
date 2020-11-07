---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 9a67729b384703ccc102b14d521d4422825bdb6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773480"
---
# <span data-ttu-id="29105-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="29105-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="29105-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29105-102">SYNOPSIS</span></span>
<span data-ttu-id="29105-103">Exclui a malha de recuperação de site do Azure especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="29105-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="29105-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29105-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29105-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29105-105">DESCRIPTION</span></span>
<span data-ttu-id="29105-106">O cmdlet **Remove-AzRecoveryServicesAsrFabric** remove a estrutura de recuperação de site do Azure especificada do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="29105-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="29105-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29105-107">EXAMPLES</span></span>

### <span data-ttu-id="29105-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29105-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="29105-109">Inicia a exclusão da malha especificada e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="29105-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="29105-110">OS</span><span class="sxs-lookup"><span data-stu-id="29105-110">PARAMETERS</span></span>

### <span data-ttu-id="29105-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29105-111">-DefaultProfile</span></span>
<span data-ttu-id="29105-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29105-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="29105-113">-Force</span><span class="sxs-lookup"><span data-stu-id="29105-113">-Force</span></span>
<span data-ttu-id="29105-114">Force o comando a ser executado sem fornecer um aviso adicional.</span><span class="sxs-lookup"><span data-stu-id="29105-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="29105-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29105-115">-InputObject</span></span>
<span data-ttu-id="29105-116">O objeto de entrada para o cmdlet: o objeto de malha ASR correspondente à malha a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="29105-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="29105-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29105-117">-Confirm</span></span>
<span data-ttu-id="29105-118">Especifique se a confirmação é necessária.</span><span class="sxs-lookup"><span data-stu-id="29105-118">Specify if confirmation is required.</span></span> <span data-ttu-id="29105-119">Defina o valor do parâmetro Confirm para $false a fim de ignorar a confirmação.</span><span class="sxs-lookup"><span data-stu-id="29105-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="29105-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29105-120">-WhatIf</span></span>
<span data-ttu-id="29105-121">Mostra o que aconteceria se o cmdlet fosse executado sem realmente executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29105-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="29105-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29105-122">CommonParameters</span></span>
<span data-ttu-id="29105-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29105-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29105-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29105-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29105-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29105-125">INPUTS</span></span>

### <span data-ttu-id="29105-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="29105-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="29105-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29105-127">OUTPUTS</span></span>

### <span data-ttu-id="29105-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="29105-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="29105-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29105-129">NOTES</span></span>

## <span data-ttu-id="29105-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29105-130">RELATED LINKS</span></span>

[<span data-ttu-id="29105-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="29105-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="29105-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="29105-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
