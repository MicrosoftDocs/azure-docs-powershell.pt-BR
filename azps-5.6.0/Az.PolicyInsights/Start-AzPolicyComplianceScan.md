---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: db51cfdf499fcf3d6c81f47d977978a6ff4bf8cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890104"
---
# <span data-ttu-id="00de8-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="00de8-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="00de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00de8-102">SYNOPSIS</span></span>
<span data-ttu-id="00de8-103">Dispara uma avaliação de conformidade de política para todos os recursos em uma assinatura ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="00de8-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="00de8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="00de8-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00de8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="00de8-105">DESCRIPTION</span></span>
<span data-ttu-id="00de8-106">O cmdlet **Start-AzPolicyComplianceScan** inicia uma avaliação de conformidade de política para uma assinatura ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="00de8-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="00de8-107">Todos os recursos nesse escopo terão seu estado de conformidade avaliado em relação a todas as políticas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="00de8-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="00de8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00de8-108">EXAMPLES</span></span>

### <span data-ttu-id="00de8-109">Exemplo 1: Iniciar uma verificação de conformidade no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="00de8-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="00de8-110">Este comando inicia uma avaliação de conformidade de política para a assinatura ativa.</span><span class="sxs-lookup"><span data-stu-id="00de8-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="00de8-111">Exemplo 2: Iniciar uma verificação de conformidade no escopo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="00de8-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="00de8-112">Este comando inicia uma avaliação de conformidade de política para o grupo de recursos "myRG" na assinatura ativa.</span><span class="sxs-lookup"><span data-stu-id="00de8-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="00de8-113">Exemplo 3: iniciar uma verificação de conformidade e aguardar que ela seja concluída em segundo plano</span><span class="sxs-lookup"><span data-stu-id="00de8-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="00de8-114">Este comando inicia uma avaliação de conformidade de política para a assinatura ativa.</span><span class="sxs-lookup"><span data-stu-id="00de8-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="00de8-115">Ele aguardará a conclusão da verificação.</span><span class="sxs-lookup"><span data-stu-id="00de8-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="00de8-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="00de8-116">PARAMETERS</span></span>

### <span data-ttu-id="00de8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00de8-117">-AsJob</span></span>
<span data-ttu-id="00de8-118">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="00de8-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="00de8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00de8-119">-DefaultProfile</span></span>
<span data-ttu-id="00de8-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00de8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00de8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00de8-121">-PassThru</span></span>
<span data-ttu-id="00de8-122">Retornar True se o comando for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="00de8-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="00de8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00de8-123">-ResourceGroupName</span></span>
<span data-ttu-id="00de8-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="00de8-124">Resource group name.</span></span>

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

### <span data-ttu-id="00de8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00de8-125">-Confirm</span></span>
<span data-ttu-id="00de8-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00de8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00de8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00de8-127">-WhatIf</span></span>
<span data-ttu-id="00de8-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00de8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00de8-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00de8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00de8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00de8-130">CommonParameters</span></span>
<span data-ttu-id="00de8-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00de8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00de8-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00de8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00de8-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00de8-133">INPUTS</span></span>

### <span data-ttu-id="00de8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="00de8-134">System.String</span></span>

## <span data-ttu-id="00de8-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="00de8-135">OUTPUTS</span></span>

### <span data-ttu-id="00de8-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00de8-136">System.Boolean</span></span>

## <span data-ttu-id="00de8-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="00de8-137">NOTES</span></span>

## <span data-ttu-id="00de8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00de8-138">RELATED LINKS</span></span>
