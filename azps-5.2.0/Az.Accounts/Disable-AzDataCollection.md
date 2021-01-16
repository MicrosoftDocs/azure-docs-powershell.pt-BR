---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258251"
---
# <span data-ttu-id="57f82-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="57f82-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="57f82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57f82-102">SYNOPSIS</span></span>
<span data-ttu-id="57f82-103">Opta pela coleta de dados para melhorar os cmdlets do PowerShell do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="57f82-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="57f82-104">Os dados são coletados por padrão, a menos que você explicitamente opte por sair.</span><span class="sxs-lookup"><span data-stu-id="57f82-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="57f82-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57f82-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57f82-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57f82-106">DESCRIPTION</span></span>

<span data-ttu-id="57f82-107">O `Disable-AzDataCollection` cmdlet é usado para recusar a coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="57f82-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="57f82-108">O PowerShell do Azure coleta automaticamente dados de telemetria por padrão.</span><span class="sxs-lookup"><span data-stu-id="57f82-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="57f82-109">Para desabilitar a coleta de dados, você deve explicitamente recusar. A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="57f82-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="57f82-110">O Microsoft Azure PowerShell não coleta nenhum dado particular ou pessoal.</span><span class="sxs-lookup"><span data-stu-id="57f82-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="57f82-111">Se você tiver recusado anteriormente, execute o `Enable-AzDataCollection` cmdlet para habilitar novamente a coleta de dados do usuário atual no computador atual.</span><span class="sxs-lookup"><span data-stu-id="57f82-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="57f82-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57f82-112">EXAMPLES</span></span>

### <span data-ttu-id="57f82-113">Exemplo 1: desabilitando a coleta de dados para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="57f82-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="57f82-114">O exemplo a seguir mostra como desabilitar a coleta de dados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="57f82-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="57f82-115">OS</span><span class="sxs-lookup"><span data-stu-id="57f82-115">PARAMETERS</span></span>

### <span data-ttu-id="57f82-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f82-116">-DefaultProfile</span></span>

<span data-ttu-id="57f82-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57f82-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f82-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="57f82-118">-Confirm</span></span>

<span data-ttu-id="57f82-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57f82-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f82-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f82-120">-WhatIf</span></span>

<span data-ttu-id="57f82-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57f82-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57f82-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57f82-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57f82-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f82-123">CommonParameters</span></span>

<span data-ttu-id="57f82-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f82-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f82-125">Para obter mais informações, consulte [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="57f82-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="57f82-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57f82-126">INPUTS</span></span>

### <span data-ttu-id="57f82-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="57f82-127">None</span></span>

## <span data-ttu-id="57f82-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57f82-128">OUTPUTS</span></span>

### <span data-ttu-id="57f82-129">System. void</span><span class="sxs-lookup"><span data-stu-id="57f82-129">System.Void</span></span>

## <span data-ttu-id="57f82-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57f82-130">NOTES</span></span>

## <span data-ttu-id="57f82-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57f82-131">RELATED LINKS</span></span>

[<span data-ttu-id="57f82-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="57f82-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
