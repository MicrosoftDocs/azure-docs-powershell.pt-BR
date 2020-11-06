---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 4a29a1d57d903edb0e19689750de2bad45b2c2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430685"
---
# <span data-ttu-id="e72a7-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="e72a7-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="e72a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e72a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e72a7-103">Permite que o Azure PowerShell colete dados para melhorar a experiência do usuário com cmdlets do AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="e72a7-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="e72a7-104">Executar esse cmdlet é ativado para a coleta de dados do usuário atual no computador atual.</span><span class="sxs-lookup"><span data-stu-id="e72a7-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="e72a7-105">Nenhum dado será coletado, a menos que você explicitamente opte por fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="e72a7-105">No data is collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e72a7-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e72a7-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e72a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e72a7-107">DESCRIPTION</span></span>
<span data-ttu-id="e72a7-108">Você pode melhorar a experiência de usar o Microsoft Cloud e o PowerShell do Azure, optando pela coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="e72a7-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="e72a7-109">O PowerShell do Azure não coleta dados sem o seu consentimento-você deve optar explicitamente por meio da execução de Enable-AzureRmDataCollection ou respondendo Sim quando o PowerShell do Azure solicitar a coleta de dados na primeira vez que você executar um cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e72a7-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="e72a7-110">A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência de usar o PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="e72a7-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="e72a7-111">O Microsoft Azure PowerShell não coleta dados particulares nem qualquer informação que possa identificá-lo pessoalmente.</span><span class="sxs-lookup"><span data-stu-id="e72a7-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="e72a7-112">Execute o cmdlet Enable-AzureRMDataCollection para habilitar a coleta de dados para o usuário atual no computador atual.</span><span class="sxs-lookup"><span data-stu-id="e72a7-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="e72a7-113">Isso impedirá que o usuário atual seja avisado sobre a coleta de dados na primeira vez que cmdlets são executados.</span><span class="sxs-lookup"><span data-stu-id="e72a7-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="e72a7-114">Para desabilitar a coleta de dados para o usuário atual, execute o cmdlet Disable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="e72a7-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="e72a7-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e72a7-115">EXAMPLES</span></span>

### <span data-ttu-id="e72a7-116">Exemplo 1: Habilitando a coleta de dados para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="e72a7-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="e72a7-117">Este exemplo mostra como habilitar a coleta de dados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="e72a7-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="e72a7-118">OS</span><span class="sxs-lookup"><span data-stu-id="e72a7-118">PARAMETERS</span></span>

### <span data-ttu-id="e72a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72a7-119">-DefaultProfile</span></span>
<span data-ttu-id="e72a7-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e72a7-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e72a7-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e72a7-121">-Confirm</span></span>
<span data-ttu-id="e72a7-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e72a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e72a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e72a7-123">-WhatIf</span></span>
<span data-ttu-id="e72a7-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e72a7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e72a7-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e72a7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e72a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72a7-126">CommonParameters</span></span>
<span data-ttu-id="e72a7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e72a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72a7-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e72a7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72a7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e72a7-129">INPUTS</span></span>

## <span data-ttu-id="e72a7-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e72a7-130">OUTPUTS</span></span>

### <span data-ttu-id="e72a7-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e72a7-131">None</span></span>

## <span data-ttu-id="e72a7-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e72a7-132">NOTES</span></span>

## <span data-ttu-id="e72a7-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e72a7-133">RELATED LINKS</span></span>

[<span data-ttu-id="e72a7-134">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="e72a7-134">Disable-AzureRmDataCollection</span></span>](./Disable-AzureRmDataCollection.md)

