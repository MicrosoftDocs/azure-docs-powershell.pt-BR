---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114971"
---
# <span data-ttu-id="fb208-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="fb208-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="fb208-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb208-102">SYNOPSIS</span></span>
<span data-ttu-id="fb208-103">Obtém os pontos de recuperação disponíveis para um item protegido por replicação.</span><span class="sxs-lookup"><span data-stu-id="fb208-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="fb208-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb208-104">SYNTAX</span></span>

### <span data-ttu-id="fb208-105">ByObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fb208-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb208-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="fb208-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb208-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb208-107">DESCRIPTION</span></span>
<span data-ttu-id="fb208-108">O cmdlet **Get-AzRecoveryServicesAsrRecoveryPoint** obtém a lista de pontos de recuperação disponíveis para um item protegido por replicação.</span><span class="sxs-lookup"><span data-stu-id="fb208-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="fb208-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fb208-109">EXAMPLES</span></span>

### <span data-ttu-id="fb208-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb208-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="fb208-111">Obtém pontos de recuperação para o item protegido de replicação ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="fb208-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="fb208-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb208-112">PARAMETERS</span></span>

### <span data-ttu-id="fb208-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb208-113">-DefaultProfile</span></span>
<span data-ttu-id="fb208-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb208-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fb208-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb208-115">-Name</span></span>
<span data-ttu-id="fb208-116">Especifica o nome do ponto de recuperação a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="fb208-116">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb208-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb208-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fb208-118">Especifica o objeto Item Protegido de Replicação de Recuperação de Site do Azure para obter a lista de pontos de recuperação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fb208-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb208-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb208-119">CommonParameters</span></span>
<span data-ttu-id="fb208-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb208-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb208-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb208-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb208-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="fb208-122">INPUTS</span></span>

### <span data-ttu-id="fb208-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb208-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="fb208-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="fb208-124">OUTPUTS</span></span>

### <span data-ttu-id="fb208-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="fb208-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="fb208-126">Notas</span><span class="sxs-lookup"><span data-stu-id="fb208-126">NOTES</span></span>

## <span data-ttu-id="fb208-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb208-127">RELATED LINKS</span></span>

[<span data-ttu-id="fb208-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb208-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="fb208-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb208-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="fb208-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb208-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="fb208-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb208-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="fb208-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb208-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
