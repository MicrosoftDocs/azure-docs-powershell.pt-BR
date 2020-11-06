---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: 1a68b5ca391e6c09673f07f0469035e0f96c1562
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595805"
---
# <span data-ttu-id="aae7f-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="aae7f-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="aae7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aae7f-102">SYNOPSIS</span></span>
<span data-ttu-id="aae7f-103">Permite que o Azure PowerShell colete dados para melhorar a experiência do usuário com cmdlets do AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="aae7f-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="aae7f-104">Executar esse cmdlet é ativado para a coleta de dados do usuário atual no computador atual.</span><span class="sxs-lookup"><span data-stu-id="aae7f-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="aae7f-105">Nenhum dado será coletado, a menos que você explicitamente opte por fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="aae7f-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="aae7f-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aae7f-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aae7f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aae7f-107">DESCRIPTION</span></span>
<span data-ttu-id="aae7f-108">Você pode melhorar a experiência de usar o Microsoft Cloud e o PowerShell do Azure, optando pela coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="aae7f-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="aae7f-109">O PowerShell do Azure não coleta dados sem o seu consentimento-você deve optar explicitamente por meio da execução de Enable-AzDataCollection ou respondendo Sim quando o PowerShell do Azure solicitar a coleta de dados na primeira vez que você executar um cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aae7f-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="aae7f-110">A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência de usar o PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="aae7f-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="aae7f-111">O Microsoft Azure PowerShell não coleta dados particulares nem qualquer informação que possa identificá-lo pessoalmente.</span><span class="sxs-lookup"><span data-stu-id="aae7f-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="aae7f-112">Execute o cmdlet Enable-AzDataCollection para habilitar a coleta de dados para o usuário atual no computador atual.</span><span class="sxs-lookup"><span data-stu-id="aae7f-112">Run the Enable-AzDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="aae7f-113">Isso impedirá que o usuário atual seja avisado sobre a coleta de dados na primeira vez que cmdlets são executados.</span><span class="sxs-lookup"><span data-stu-id="aae7f-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="aae7f-114">Para desabilitar a coleta de dados para o usuário atual, execute o cmdlet Disable-AzDataCollection.</span><span class="sxs-lookup"><span data-stu-id="aae7f-114">To disable data collection for the current user, run the Disable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="aae7f-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aae7f-115">EXAMPLES</span></span>

### <span data-ttu-id="aae7f-116">Exemplo 1: Habilitando a coleta de dados para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="aae7f-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzDataCollection
```

<span data-ttu-id="aae7f-117">Este exemplo mostra como habilitar a coleta de dados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="aae7f-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="aae7f-118">OS</span><span class="sxs-lookup"><span data-stu-id="aae7f-118">PARAMETERS</span></span>

### <span data-ttu-id="aae7f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae7f-119">-DefaultProfile</span></span>
<span data-ttu-id="aae7f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aae7f-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aae7f-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aae7f-121">-Confirm</span></span>
<span data-ttu-id="aae7f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aae7f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aae7f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aae7f-123">-WhatIf</span></span>
<span data-ttu-id="aae7f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aae7f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aae7f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aae7f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aae7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae7f-126">CommonParameters</span></span>
<span data-ttu-id="aae7f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae7f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae7f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae7f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aae7f-129">INPUTS</span></span>

### <span data-ttu-id="aae7f-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="aae7f-130">None</span></span>

## <span data-ttu-id="aae7f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aae7f-131">OUTPUTS</span></span>

### <span data-ttu-id="aae7f-132">System. void</span><span class="sxs-lookup"><span data-stu-id="aae7f-132">System.Void</span></span>

## <span data-ttu-id="aae7f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aae7f-133">NOTES</span></span>

## <span data-ttu-id="aae7f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aae7f-134">RELATED LINKS</span></span>

[<span data-ttu-id="aae7f-135">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="aae7f-135">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)

