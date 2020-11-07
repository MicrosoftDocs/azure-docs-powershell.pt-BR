---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 8c4bc3598d18042d31e98b37d9fc2c09d45b74d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773039"
---
# <span data-ttu-id="a4401-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a4401-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="a4401-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4401-102">SYNOPSIS</span></span>
<span data-ttu-id="a4401-103">Obtém um plano de recuperação ou todos os planos de recuperação no cofre dos serviços de recuperação</span><span class="sxs-lookup"><span data-stu-id="a4401-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="a4401-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4401-104">SYNTAX</span></span>

### <span data-ttu-id="a4401-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="a4401-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4401-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a4401-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4401-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a4401-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4401-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4401-108">DESCRIPTION</span></span>
<span data-ttu-id="a4401-109">O cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan** Obtém os detalhes do plano de recuperação especificado ou todos os planos de recuperação no cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a4401-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="a4401-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4401-110">EXAMPLES</span></span>

### <span data-ttu-id="a4401-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4401-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="a4401-112">Obtém o plano de recuperação com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="a4401-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="a4401-113">OS</span><span class="sxs-lookup"><span data-stu-id="a4401-113">PARAMETERS</span></span>

### <span data-ttu-id="a4401-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4401-114">-DefaultProfile</span></span>
<span data-ttu-id="a4401-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4401-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a4401-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a4401-116">-FriendlyName</span></span>
<span data-ttu-id="a4401-117">Especifica o nome amigável do plano de recuperação a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="a4401-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="a4401-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4401-118">-Name</span></span>
<span data-ttu-id="a4401-119">Especifica o nome do plano de recuperação a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="a4401-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="a4401-120">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a4401-120">-Path</span></span>
<span data-ttu-id="a4401-121">Especifica o caminho de arquivo para o qual esse cmdlet salva a definição JSON do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="a4401-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="a4401-122">A definição JSON pode ser editada para modificar o plano de recuperação e usada para atualizar o plano de recuperação por meio do cmdlet Update-AzRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a4401-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="a4401-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4401-123">CommonParameters</span></span>
<span data-ttu-id="a4401-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4401-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4401-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4401-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4401-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4401-126">INPUTS</span></span>

### <span data-ttu-id="a4401-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a4401-127">None</span></span>

## <span data-ttu-id="a4401-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4401-128">OUTPUTS</span></span>

### <span data-ttu-id="a4401-129">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a4401-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="a4401-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4401-130">NOTES</span></span>

## <span data-ttu-id="a4401-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4401-131">RELATED LINKS</span></span>

[<span data-ttu-id="a4401-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a4401-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a4401-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a4401-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="a4401-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a4401-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)