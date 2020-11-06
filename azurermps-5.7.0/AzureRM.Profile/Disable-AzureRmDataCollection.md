---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: 07b541636229d65a092dc9a3067d3a4cef89cac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439855"
---
# <span data-ttu-id="8cd02-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="8cd02-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="8cd02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8cd02-102">SYNOPSIS</span></span>
<span data-ttu-id="8cd02-103">Opta pela coleta de dados para melhorar os cmdlets do AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="8cd02-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="8cd02-104">Os dados não são coletados, a menos que você explicitamente opte por você.</span><span class="sxs-lookup"><span data-stu-id="8cd02-104">Data is not collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cd02-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cd02-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cd02-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8cd02-106">DESCRIPTION</span></span>
<span data-ttu-id="8cd02-107">Você pode melhorar a experiência de usar o Microsoft Cloud e o PowerShell do Azure, optando pela coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="8cd02-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="8cd02-108">O PowerShell do Azure não coleta dados sem o seu consentimento-você deve optar explicitamente por meio da execução de Enable-AzureRmDataCollection ou respondendo Sim quando o PowerShell do Azure solicitar a coleta de dados na primeira vez que você executar um cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cd02-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="8cd02-109">A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência de usar o PowerShell do Azure.</span><span class="sxs-lookup"><span data-stu-id="8cd02-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="8cd02-110">O Microsoft Azure PowerShell não coleta dados particulares nem qualquer informação que possa identificá-lo pessoalmente.</span><span class="sxs-lookup"><span data-stu-id="8cd02-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="8cd02-111">Execute o cmdlet Disable-AzureRMDataCollection para desabilitar a coleta de dados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="8cd02-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="8cd02-112">Isso impedirá que o usuário atual seja avisado sobre a coleta de dados na primeira vez que cmdlets são executados.</span><span class="sxs-lookup"><span data-stu-id="8cd02-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="8cd02-113">Para habilitar a coleta de dados para o usuário atual, execute o cmdlet Enable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="8cd02-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="8cd02-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8cd02-114">EXAMPLES</span></span>

### <span data-ttu-id="8cd02-115">Exemplo 1: desabilitando a coleta de dados para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="8cd02-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="8cd02-116">Este exemplo mostra como desabilitar a coleta de dados para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="8cd02-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="8cd02-117">OS</span><span class="sxs-lookup"><span data-stu-id="8cd02-117">PARAMETERS</span></span>

### <span data-ttu-id="8cd02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cd02-118">-DefaultProfile</span></span>
<span data-ttu-id="8cd02-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8cd02-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd02-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8cd02-120">-Confirm</span></span>
<span data-ttu-id="8cd02-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cd02-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd02-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cd02-122">-WhatIf</span></span>
<span data-ttu-id="8cd02-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8cd02-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cd02-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8cd02-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd02-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cd02-125">CommonParameters</span></span>
<span data-ttu-id="8cd02-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cd02-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cd02-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cd02-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cd02-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8cd02-128">INPUTS</span></span>

### <span data-ttu-id="8cd02-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8cd02-129">None</span></span>
<span data-ttu-id="8cd02-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8cd02-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8cd02-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8cd02-131">OUTPUTS</span></span>

### <span data-ttu-id="8cd02-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8cd02-132">None</span></span>

## <span data-ttu-id="8cd02-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8cd02-133">NOTES</span></span>

## <span data-ttu-id="8cd02-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8cd02-134">RELATED LINKS</span></span>

[<span data-ttu-id="8cd02-135">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="8cd02-135">Enable-AzureRmDataCollection</span></span>](./Enable-AzureRmDataCollection.md)

