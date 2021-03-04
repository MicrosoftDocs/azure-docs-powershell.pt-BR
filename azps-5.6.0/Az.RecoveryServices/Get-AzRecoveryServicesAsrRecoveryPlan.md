---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: d3470c3984026232fc90d336e22668868311aa9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886863"
---
# <span data-ttu-id="b61d0-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b61d0-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="b61d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b61d0-102">SYNOPSIS</span></span>
<span data-ttu-id="b61d0-103">Obtém um plano de recuperação ou todos os planos de recuperação no cofre dos Serviços de Recuperação</span><span class="sxs-lookup"><span data-stu-id="b61d0-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="b61d0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b61d0-104">SYNTAX</span></span>

### <span data-ttu-id="b61d0-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b61d0-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b61d0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b61d0-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b61d0-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b61d0-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b61d0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b61d0-108">DESCRIPTION</span></span>
<span data-ttu-id="b61d0-109">O cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan** obtém os detalhes do plano de recuperação especificado ou de todos os planos de recuperação no cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="b61d0-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="b61d0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b61d0-110">EXAMPLES</span></span>

### <span data-ttu-id="b61d0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b61d0-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="b61d0-112">Obtém o plano de recuperação com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="b61d0-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="b61d0-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b61d0-113">PARAMETERS</span></span>

### <span data-ttu-id="b61d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61d0-114">-DefaultProfile</span></span>
<span data-ttu-id="b61d0-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b61d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b61d0-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b61d0-116">-FriendlyName</span></span>
<span data-ttu-id="b61d0-117">Especifica o nome amigável do plano de recuperação a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="b61d0-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61d0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b61d0-118">-Name</span></span>
<span data-ttu-id="b61d0-119">Especifica o nome do plano de recuperação a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="b61d0-119">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61d0-120">-Path</span><span class="sxs-lookup"><span data-stu-id="b61d0-120">-Path</span></span>
<span data-ttu-id="b61d0-121">Especifica o caminho do arquivo para o qual esse cmdlet salva a definição json do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b61d0-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="b61d0-122">A definição json pode ser editada para modificar o plano de recuperação e usada para atualizar o plano de recuperação por meio do cmdlet Update-AzRecoveryServicesASRRecoveryPlan de recuperação</span><span class="sxs-lookup"><span data-stu-id="b61d0-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61d0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61d0-123">CommonParameters</span></span>
<span data-ttu-id="b61d0-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b61d0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61d0-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b61d0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61d0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b61d0-126">INPUTS</span></span>

### <span data-ttu-id="b61d0-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b61d0-127">None</span></span>

## <span data-ttu-id="b61d0-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b61d0-128">OUTPUTS</span></span>

### <span data-ttu-id="b61d0-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b61d0-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="b61d0-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="b61d0-130">NOTES</span></span>

## <span data-ttu-id="b61d0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b61d0-131">RELATED LINKS</span></span>

[<span data-ttu-id="b61d0-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b61d0-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b61d0-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b61d0-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="b61d0-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b61d0-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
