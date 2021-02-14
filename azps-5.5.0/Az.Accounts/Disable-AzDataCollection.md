---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115581"
---
# <span data-ttu-id="e744f-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="e744f-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="e744f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e744f-102">SYNOPSIS</span></span>
<span data-ttu-id="e744f-103">Opta por não coletar dados para melhorar os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e744f-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="e744f-104">Os dados são coletados por padrão, a menos que você a opte explicitamente.</span><span class="sxs-lookup"><span data-stu-id="e744f-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="e744f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e744f-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e744f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e744f-106">DESCRIPTION</span></span>

<span data-ttu-id="e744f-107">O `Disable-AzDataCollection` cmdlet é usado para não usar a coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="e744f-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="e744f-108">O Azure PowerShell coleta automaticamente dados de telemetria por padrão.</span><span class="sxs-lookup"><span data-stu-id="e744f-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="e744f-109">Para desabilitar a coleta de dados, você deve sair explicitamente. A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="e744f-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="e744f-110">O Microsoft Azure PowerShell não coleta dados pessoais ou particulares.</span><span class="sxs-lookup"><span data-stu-id="e744f-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="e744f-111">Se você tiver optado anteriormente, execute o cmdlet para habilitar a coleta de dados para o usuário `Enable-AzDataCollection` atual no computador atual.</span><span class="sxs-lookup"><span data-stu-id="e744f-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="e744f-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e744f-112">EXAMPLES</span></span>

### <span data-ttu-id="e744f-113">Exemplo 1: desabilitando a coleta de dados para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="e744f-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="e744f-114">O exemplo a seguir mostra como desabilitar a coleta de dados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="e744f-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="e744f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e744f-115">PARAMETERS</span></span>

### <span data-ttu-id="e744f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e744f-116">-DefaultProfile</span></span>

<span data-ttu-id="e744f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e744f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e744f-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e744f-118">-Confirm</span></span>

<span data-ttu-id="e744f-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e744f-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e744f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e744f-120">-WhatIf</span></span>

<span data-ttu-id="e744f-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e744f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e744f-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e744f-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e744f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e744f-123">CommonParameters</span></span>

<span data-ttu-id="e744f-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e744f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e744f-125">Para obter mais informações, [consulte about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="e744f-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="e744f-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="e744f-126">INPUTS</span></span>

### <span data-ttu-id="e744f-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e744f-127">None</span></span>

## <span data-ttu-id="e744f-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="e744f-128">OUTPUTS</span></span>

### <span data-ttu-id="e744f-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="e744f-129">System.Void</span></span>

## <span data-ttu-id="e744f-130">Notas</span><span class="sxs-lookup"><span data-stu-id="e744f-130">NOTES</span></span>

## <span data-ttu-id="e744f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e744f-131">RELATED LINKS</span></span>

[<span data-ttu-id="e744f-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="e744f-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
