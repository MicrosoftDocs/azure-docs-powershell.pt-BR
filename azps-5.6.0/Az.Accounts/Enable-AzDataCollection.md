---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: ce2c4060d6471cc65c6b343e86c1e15b74ca5414
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891528"
---
# <span data-ttu-id="81d5b-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="81d5b-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="81d5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="81d5b-103">Permite que o Azure PowerShell colete dados para melhorar a experiência do usuário com os cmdlets do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="81d5b-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="81d5b-104">A execução desse cmdlet opta pela coleta de dados para o usuário atual no computador atual.</span><span class="sxs-lookup"><span data-stu-id="81d5b-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="81d5b-105">Os dados são coletados por padrão, a menos que você opte explicitamente.</span><span class="sxs-lookup"><span data-stu-id="81d5b-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="81d5b-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="81d5b-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81d5b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="81d5b-107">DESCRIPTION</span></span>

<span data-ttu-id="81d5b-108">O `Enable-AzDataCollection` cmdlet é usado para optar pela coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="81d5b-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="81d5b-109">O Azure PowerShell coleta automaticamente dados de telemetria por padrão.</span><span class="sxs-lookup"><span data-stu-id="81d5b-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="81d5b-110">A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="81d5b-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="81d5b-111">O Microsoft Azure PowerShell não coleta dados pessoais ou particulares.</span><span class="sxs-lookup"><span data-stu-id="81d5b-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="81d5b-112">Para desabilitar a coleta de dados, você deve optar explicitamente pela execução `Disable-AzDataCollection` de .</span><span class="sxs-lookup"><span data-stu-id="81d5b-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="81d5b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81d5b-113">EXAMPLES</span></span>

### <span data-ttu-id="81d5b-114">Exemplo 1: Habilitando a coleta de dados para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="81d5b-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="81d5b-115">O exemplo a seguir mostra como habilitar a coleta de dados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="81d5b-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="81d5b-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="81d5b-116">PARAMETERS</span></span>

### <span data-ttu-id="81d5b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d5b-117">-DefaultProfile</span></span>

<span data-ttu-id="81d5b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81d5b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81d5b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81d5b-119">-Confirm</span></span>

<span data-ttu-id="81d5b-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81d5b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d5b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d5b-121">-WhatIf</span></span>

<span data-ttu-id="81d5b-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81d5b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81d5b-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81d5b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d5b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d5b-124">CommonParameters</span></span>
<span data-ttu-id="81d5b-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d5b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d5b-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81d5b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d5b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81d5b-127">INPUTS</span></span>

### <span data-ttu-id="81d5b-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="81d5b-128">None</span></span>

## <span data-ttu-id="81d5b-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="81d5b-129">OUTPUTS</span></span>

### <span data-ttu-id="81d5b-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="81d5b-130">System.Void</span></span>

## <span data-ttu-id="81d5b-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="81d5b-131">NOTES</span></span>

## <span data-ttu-id="81d5b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81d5b-132">RELATED LINKS</span></span>

[<span data-ttu-id="81d5b-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="81d5b-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
