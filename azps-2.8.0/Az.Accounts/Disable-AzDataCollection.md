---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: e78a361bfb332bc2a8bcb226fae946a3abc0a05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598271"
---
# <span data-ttu-id="f02fc-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f02fc-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="f02fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f02fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f02fc-103">Opta pela coleta de dados para melhorar os cmdlets do AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="f02fc-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="f02fc-104">Os dados não são coletados, a menos que você explicitamente opte por você.</span><span class="sxs-lookup"><span data-stu-id="f02fc-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="f02fc-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f02fc-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f02fc-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f02fc-106">DESCRIPTION</span></span>
<span data-ttu-id="f02fc-107">Você pode melhorar a experiência de usar o Microsoft Cloud e o PowerShell do Azure, optando pela coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="f02fc-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="f02fc-108">O PowerShell do Azure não coleta dados sem o seu consentimento-você deve optar explicitamente por meio da execução de Enable-AzDataCollection ou respondendo Sim quando o PowerShell do Azure solicitar a coleta de dados na primeira vez que você executar um cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f02fc-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="f02fc-109">A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência de usar o PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="f02fc-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="f02fc-110">O Microsoft Azure PowerShell não coleta dados particulares nem qualquer informação que possa identificá-lo pessoalmente.</span><span class="sxs-lookup"><span data-stu-id="f02fc-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="f02fc-111">Execute o cmdlet Disable-AzDataCollection para desabilitar a coleta de dados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f02fc-111">Run the Disable-AzDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="f02fc-112">Isso impedirá que o usuário atual seja avisado sobre a coleta de dados na primeira vez que cmdlets são executados.</span><span class="sxs-lookup"><span data-stu-id="f02fc-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="f02fc-113">Para habilitar a coleta de dados para o usuário atual, execute o cmdlet Enable-AzDataCollection.</span><span class="sxs-lookup"><span data-stu-id="f02fc-113">To enable data collection for the current user, run the Enable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="f02fc-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f02fc-114">EXAMPLES</span></span>

### <span data-ttu-id="f02fc-115">Exemplo 1: desabilitando a coleta de dados para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="f02fc-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzDataCollection
```

<span data-ttu-id="f02fc-116">Este exemplo mostra como desabilitar a coleta de dados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f02fc-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="f02fc-117">OS</span><span class="sxs-lookup"><span data-stu-id="f02fc-117">PARAMETERS</span></span>

### <span data-ttu-id="f02fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f02fc-118">-DefaultProfile</span></span>
<span data-ttu-id="f02fc-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f02fc-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f02fc-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f02fc-120">-Confirm</span></span>
<span data-ttu-id="f02fc-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f02fc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f02fc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f02fc-122">-WhatIf</span></span>
<span data-ttu-id="f02fc-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f02fc-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f02fc-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f02fc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f02fc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02fc-125">CommonParameters</span></span>
<span data-ttu-id="f02fc-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f02fc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f02fc-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f02fc-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02fc-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f02fc-128">INPUTS</span></span>

### <span data-ttu-id="f02fc-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f02fc-129">None</span></span>

## <span data-ttu-id="f02fc-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f02fc-130">OUTPUTS</span></span>

### <span data-ttu-id="f02fc-131">System. void</span><span class="sxs-lookup"><span data-stu-id="f02fc-131">System.Void</span></span>

## <span data-ttu-id="f02fc-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f02fc-132">NOTES</span></span>

## <span data-ttu-id="f02fc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f02fc-133">RELATED LINKS</span></span>

[<span data-ttu-id="f02fc-134">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f02fc-134">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)

