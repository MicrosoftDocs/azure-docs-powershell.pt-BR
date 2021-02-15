---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118198"
---
# <span data-ttu-id="0c6eb-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="0c6eb-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="0c6eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="0c6eb-103">Aciona uma avaliação de conformidade de política para todos os recursos em uma assinatura ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="0c6eb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c6eb-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c6eb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c6eb-105">DESCRIPTION</span></span>
<span data-ttu-id="0c6eb-106">O cmdlet **Start-AzPolicyComplianceScan** inicia uma avaliação de conformidade de política para uma assinatura ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="0c6eb-107">Todos os recursos dentro desse escopo terão seu estado de conformidade avaliado em relação a todas as políticas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="0c6eb-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c6eb-108">EXAMPLES</span></span>

### <span data-ttu-id="0c6eb-109">Exemplo 1: Iniciar uma verificação de conformidade no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="0c6eb-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="0c6eb-110">Esse comando inicia uma avaliação de conformidade de política para a assinatura ativa.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="0c6eb-111">Exemplo 2: Iniciar uma verificação de conformidade no escopo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0c6eb-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="0c6eb-112">Esse comando inicia uma avaliação de conformidade de política para o grupo de recursos "myRG" na assinatura ativa.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="0c6eb-113">Exemplo 3: Iniciar uma verificação de conformidade e esperar até que ela seja concluída em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0c6eb-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="0c6eb-114">Esse comando inicia uma avaliação de conformidade de política para a assinatura ativa.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="0c6eb-115">Ele aguardará a conclusão da verificação.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="0c6eb-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c6eb-116">PARAMETERS</span></span>

### <span data-ttu-id="0c6eb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c6eb-117">-AsJob</span></span>
<span data-ttu-id="0c6eb-118">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="0c6eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c6eb-119">-DefaultProfile</span></span>
<span data-ttu-id="0c6eb-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c6eb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c6eb-121">-PassThru</span></span>
<span data-ttu-id="0c6eb-122">Retornar True se o comando for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="0c6eb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c6eb-123">-ResourceGroupName</span></span>
<span data-ttu-id="0c6eb-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-124">Resource group name.</span></span>

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

### <span data-ttu-id="0c6eb-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0c6eb-125">-Confirm</span></span>
<span data-ttu-id="0c6eb-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c6eb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c6eb-127">-WhatIf</span></span>
<span data-ttu-id="0c6eb-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c6eb-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c6eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c6eb-130">CommonParameters</span></span>
<span data-ttu-id="0c6eb-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c6eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c6eb-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c6eb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c6eb-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="0c6eb-133">INPUTS</span></span>

### <span data-ttu-id="0c6eb-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0c6eb-134">System.String</span></span>

## <span data-ttu-id="0c6eb-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="0c6eb-135">OUTPUTS</span></span>

### <span data-ttu-id="0c6eb-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c6eb-136">System.Boolean</span></span>

## <span data-ttu-id="0c6eb-137">Notas</span><span class="sxs-lookup"><span data-stu-id="0c6eb-137">NOTES</span></span>

## <span data-ttu-id="0c6eb-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c6eb-138">RELATED LINKS</span></span>
