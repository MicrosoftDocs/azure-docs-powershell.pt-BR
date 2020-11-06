---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 0cabaee1c1d9dfc8a627160ac01adaca81fe65c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432425"
---
# <span data-ttu-id="2beff-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2beff-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="2beff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2beff-102">SYNOPSIS</span></span>
<span data-ttu-id="2beff-103">Atualiza o conteúdo de um plano do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2beff-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2beff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2beff-104">SYNTAX</span></span>

### <span data-ttu-id="2beff-105">ByRPObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="2beff-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2beff-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="2beff-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2beff-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2beff-107">DESCRIPTION</span></span>
<span data-ttu-id="2beff-108">O cmdlet **Update-AzureRmRecoveryServicesAsrRecoveryPlan** atualiza o conteúdo de um plano de recuperação usando o conteúdo do objeto de plano de recuperação ASR ou o arquivo JSON de definição do plano de recuperação ASR.</span><span class="sxs-lookup"><span data-stu-id="2beff-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="2beff-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2beff-109">EXAMPLES</span></span>

### <span data-ttu-id="2beff-110">Exemplo 1: atualizar um plano de recuperação</span><span class="sxs-lookup"><span data-stu-id="2beff-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="2beff-111">Inicie a operação de atualização de um plano de recuperação usando o conteúdo do objeto de plano de recuperação ASR especificado e retorna o trabalho ASR usado para acompanhar a operação.</span><span class="sxs-lookup"><span data-stu-id="2beff-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2beff-112">OS</span><span class="sxs-lookup"><span data-stu-id="2beff-112">PARAMETERS</span></span>

### <span data-ttu-id="2beff-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2beff-113">-Confirm</span></span>
<span data-ttu-id="2beff-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2beff-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2beff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2beff-115">-DefaultProfile</span></span>
<span data-ttu-id="2beff-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2beff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2beff-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2beff-117">-InputObject</span></span>
<span data-ttu-id="2beff-118">Objeto de entrada para o cmdlet: especifica um objeto de plano de recuperação ASR, o conteúdo do qual é usado para atualizar o plano de recuperação referenciado pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="2beff-118">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2beff-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="2beff-119">-Path</span></span>
<span data-ttu-id="2beff-120">Especifica o caminho do arquivo JSON de definição do plano de recuperação usado para atualizar o plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2beff-120">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2beff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2beff-121">-WhatIf</span></span>
<span data-ttu-id="2beff-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2beff-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2beff-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2beff-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2beff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2beff-124">CommonParameters</span></span>
<span data-ttu-id="2beff-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2beff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2beff-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2beff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2beff-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2beff-127">INPUTS</span></span>

### <span data-ttu-id="2beff-128">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2beff-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="2beff-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2beff-129">OUTPUTS</span></span>

### <span data-ttu-id="2beff-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="2beff-130">System.Object</span></span>

## <span data-ttu-id="2beff-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2beff-131">NOTES</span></span>

## <span data-ttu-id="2beff-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2beff-132">RELATED LINKS</span></span>

[<span data-ttu-id="2beff-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2beff-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2beff-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2beff-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2beff-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2beff-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)
