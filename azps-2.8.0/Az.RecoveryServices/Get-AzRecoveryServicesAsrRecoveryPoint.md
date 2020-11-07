---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: b381f611d47306c9327d1b276aa3773c34c7b3e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773031"
---
# <span data-ttu-id="46cef-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="46cef-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="46cef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46cef-102">SYNOPSIS</span></span>
<span data-ttu-id="46cef-103">Obtém os pontos de recuperação disponíveis para um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="46cef-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="46cef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46cef-104">SYNTAX</span></span>

### <span data-ttu-id="46cef-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="46cef-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46cef-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="46cef-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46cef-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46cef-107">DESCRIPTION</span></span>
<span data-ttu-id="46cef-108">O cmdlet **Get-AzRecoveryServicesAsrRecoveryPoint** Obtém a lista de pontos de recuperação disponíveis para um item protegido de replicação.</span><span class="sxs-lookup"><span data-stu-id="46cef-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="46cef-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46cef-109">EXAMPLES</span></span>

### <span data-ttu-id="46cef-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46cef-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="46cef-111">Obtém pontos de recuperação para o item protegido de replicação ASR especificado.</span><span class="sxs-lookup"><span data-stu-id="46cef-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="46cef-112">OS</span><span class="sxs-lookup"><span data-stu-id="46cef-112">PARAMETERS</span></span>

### <span data-ttu-id="46cef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46cef-113">-DefaultProfile</span></span>
<span data-ttu-id="46cef-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46cef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="46cef-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="46cef-115">-Name</span></span>
<span data-ttu-id="46cef-116">Especifica o nome do ponto de recuperação a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="46cef-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="46cef-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="46cef-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="46cef-118">Especifica o objeto de item protegido da replicação do Azure site Recovery para o qual obter a lista de pontos de recuperação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="46cef-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="46cef-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46cef-119">CommonParameters</span></span>
<span data-ttu-id="46cef-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46cef-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46cef-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46cef-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46cef-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46cef-122">INPUTS</span></span>

### <span data-ttu-id="46cef-123">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="46cef-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="46cef-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46cef-124">OUTPUTS</span></span>

### <span data-ttu-id="46cef-125">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="46cef-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="46cef-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46cef-126">NOTES</span></span>

## <span data-ttu-id="46cef-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46cef-127">RELATED LINKS</span></span>

[<span data-ttu-id="46cef-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46cef-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="46cef-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46cef-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="46cef-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46cef-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="46cef-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46cef-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="46cef-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="46cef-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
