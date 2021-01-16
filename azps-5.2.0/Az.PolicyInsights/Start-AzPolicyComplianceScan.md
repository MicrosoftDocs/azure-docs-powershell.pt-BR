---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264408"
---
# <span data-ttu-id="390a2-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="390a2-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="390a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="390a2-102">SYNOPSIS</span></span>
<span data-ttu-id="390a2-103">Dispara uma avaliação de conformidade de política para todos os recursos de uma assinatura ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="390a2-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="390a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="390a2-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="390a2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="390a2-105">DESCRIPTION</span></span>
<span data-ttu-id="390a2-106">O cmdlet **Start-AzPolicyComplianceScan** inicia uma avaliação de conformidade de política para uma assinatura ou um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="390a2-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="390a2-107">Todos os recursos nesse escopo terão seu estado de conformidade avaliado em relação a todas as políticas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="390a2-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="390a2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="390a2-108">EXAMPLES</span></span>

### <span data-ttu-id="390a2-109">Exemplo 1: iniciar uma verificação de conformidade em escopo de assinatura</span><span class="sxs-lookup"><span data-stu-id="390a2-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="390a2-110">Esse comando inicia uma avaliação de conformidade de política para a assinatura ativa.</span><span class="sxs-lookup"><span data-stu-id="390a2-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="390a2-111">Exemplo 2: iniciar uma verificação de conformidade em escopo de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="390a2-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="390a2-112">Esse comando inicia uma avaliação de conformidade de política para o grupo de recursos "myRG" na assinatura ativa.</span><span class="sxs-lookup"><span data-stu-id="390a2-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="390a2-113">Exemplo 3: iniciar uma verificação de conformidade e esperar que ela seja concluída em segundo plano</span><span class="sxs-lookup"><span data-stu-id="390a2-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="390a2-114">Esse comando inicia uma avaliação de conformidade de política para a assinatura ativa.</span><span class="sxs-lookup"><span data-stu-id="390a2-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="390a2-115">Ele aguardará que a verificação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="390a2-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="390a2-116">OS</span><span class="sxs-lookup"><span data-stu-id="390a2-116">PARAMETERS</span></span>

### <span data-ttu-id="390a2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="390a2-117">-AsJob</span></span>
<span data-ttu-id="390a2-118">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="390a2-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="390a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="390a2-119">-DefaultProfile</span></span>
<span data-ttu-id="390a2-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="390a2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="390a2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="390a2-121">-PassThru</span></span>
<span data-ttu-id="390a2-122">Retorne true se o comando for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="390a2-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="390a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="390a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="390a2-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="390a2-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="390a2-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="390a2-125">-Confirm</span></span>
<span data-ttu-id="390a2-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="390a2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="390a2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="390a2-127">-WhatIf</span></span>
<span data-ttu-id="390a2-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="390a2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="390a2-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="390a2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="390a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="390a2-130">CommonParameters</span></span>
<span data-ttu-id="390a2-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="390a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="390a2-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="390a2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="390a2-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="390a2-133">INPUTS</span></span>

### <span data-ttu-id="390a2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="390a2-134">System.String</span></span>

## <span data-ttu-id="390a2-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="390a2-135">OUTPUTS</span></span>

### <span data-ttu-id="390a2-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="390a2-136">System.Boolean</span></span>

## <span data-ttu-id="390a2-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="390a2-137">NOTES</span></span>

## <span data-ttu-id="390a2-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="390a2-138">RELATED LINKS</span></span>
