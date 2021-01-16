---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258246"
---
# <span data-ttu-id="ee4c2-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ee4c2-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="ee4c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4c2-103">Permite que o Azure PowerShell colete dados para melhorar a experiência do usuário com os cmdlets do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ee4c2-104">Executar esse cmdlet é ativado para a coleta de dados do usuário atual no computador atual.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="ee4c2-105">Os dados são coletados por padrão, a menos que você explicitamente opte por sair.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="ee4c2-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee4c2-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee4c2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee4c2-107">DESCRIPTION</span></span>

<span data-ttu-id="ee4c2-108">O `Enable-AzDataCollection` cmdlet é usado para aceitar a coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="ee4c2-109">O PowerShell do Azure coleta automaticamente dados de telemetria por padrão.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="ee4c2-110">A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência do PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="ee4c2-111">O Microsoft Azure PowerShell não coleta nenhum dado particular ou pessoal.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="ee4c2-112">Para desabilitar a coleta de dados, você deve explicitamente optar por executar `Disable-AzDataCollection` .</span><span class="sxs-lookup"><span data-stu-id="ee4c2-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="ee4c2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee4c2-113">EXAMPLES</span></span>

### <span data-ttu-id="ee4c2-114">Exemplo 1: Habilitando a coleta de dados para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="ee4c2-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="ee4c2-115">O exemplo a seguir mostra como habilitar a coleta de dados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="ee4c2-116">OS</span><span class="sxs-lookup"><span data-stu-id="ee4c2-116">PARAMETERS</span></span>

### <span data-ttu-id="ee4c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee4c2-117">-DefaultProfile</span></span>

<span data-ttu-id="ee4c2-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee4c2-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ee4c2-119">-Confirm</span></span>

<span data-ttu-id="ee4c2-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee4c2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee4c2-121">-WhatIf</span></span>

<span data-ttu-id="ee4c2-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee4c2-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee4c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4c2-124">CommonParameters</span></span>

<span data-ttu-id="ee4c2-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee4c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4c2-126">Para obter mais informações, consulte [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="ee4c2-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="ee4c2-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee4c2-127">INPUTS</span></span>

### <span data-ttu-id="ee4c2-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ee4c2-128">None</span></span>

## <span data-ttu-id="ee4c2-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee4c2-129">OUTPUTS</span></span>

### <span data-ttu-id="ee4c2-130">System. void</span><span class="sxs-lookup"><span data-stu-id="ee4c2-130">System.Void</span></span>

## <span data-ttu-id="ee4c2-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee4c2-131">NOTES</span></span>

## <span data-ttu-id="ee4c2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee4c2-132">RELATED LINKS</span></span>

[<span data-ttu-id="ee4c2-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ee4c2-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
