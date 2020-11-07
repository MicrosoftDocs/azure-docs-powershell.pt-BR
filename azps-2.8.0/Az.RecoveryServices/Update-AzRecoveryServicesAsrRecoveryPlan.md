---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 33410022800111097610116732f6f137dfac41bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773422"
---
# <span data-ttu-id="e7fbe-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e7fbe-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="e7fbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fbe-103">Atualiza o conteúdo de um plano do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e7fbe-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="e7fbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7fbe-104">SYNTAX</span></span>

### <span data-ttu-id="e7fbe-105">ByRPObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="e7fbe-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7fbe-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="e7fbe-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7fbe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7fbe-107">DESCRIPTION</span></span>
<span data-ttu-id="e7fbe-108">O cmdlet **Update-AzRecoveryServicesAsrRecoveryPlan** atualiza o conteúdo de um plano de recuperação usando o conteúdo do objeto de plano de recuperação ASR ou o arquivo JSON de definição do plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="e7fbe-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="e7fbe-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7fbe-109">EXAMPLES</span></span>

### <span data-ttu-id="e7fbe-110">Exemplo 1: atualizar um plano de recuperação</span><span class="sxs-lookup"><span data-stu-id="e7fbe-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="e7fbe-111">Inicie a operação de atualização de um plano de recuperação usando o conteúdo do objeto de plano de recuperação ASR especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="e7fbe-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e7fbe-112">OS</span><span class="sxs-lookup"><span data-stu-id="e7fbe-112">PARAMETERS</span></span>

### <span data-ttu-id="e7fbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7fbe-113">-DefaultProfile</span></span>
<span data-ttu-id="e7fbe-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7fbe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e7fbe-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7fbe-115">-InputObject</span></span>
<span data-ttu-id="e7fbe-116">Objeto de entrada para o cmdlet: especifica um objeto de plano de recuperação ASR, o conteúdo do qual é usado para atualizar o plano de recuperação referenciado pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="e7fbe-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7fbe-117">-Caminho</span><span class="sxs-lookup"><span data-stu-id="e7fbe-117">-Path</span></span>
<span data-ttu-id="e7fbe-118">Especifica o caminho do arquivo JSON de definição do plano de recuperação usado para atualizar o plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e7fbe-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7fbe-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7fbe-119">-Confirm</span></span>
<span data-ttu-id="e7fbe-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7fbe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7fbe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7fbe-121">-WhatIf</span></span>
<span data-ttu-id="e7fbe-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7fbe-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7fbe-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7fbe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7fbe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fbe-124">CommonParameters</span></span>
<span data-ttu-id="e7fbe-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7fbe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fbe-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7fbe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fbe-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7fbe-127">INPUTS</span></span>

### <span data-ttu-id="e7fbe-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e7fbe-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="e7fbe-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7fbe-129">OUTPUTS</span></span>

### <span data-ttu-id="e7fbe-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e7fbe-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e7fbe-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7fbe-131">NOTES</span></span>

## <span data-ttu-id="e7fbe-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7fbe-132">RELATED LINKS</span></span>

[<span data-ttu-id="e7fbe-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e7fbe-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e7fbe-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e7fbe-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e7fbe-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e7fbe-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
