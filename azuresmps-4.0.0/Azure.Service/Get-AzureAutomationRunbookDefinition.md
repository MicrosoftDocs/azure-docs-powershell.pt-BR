---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 66740917-E8BB-44ED-9CBB-9825BD1840E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b049d770dbcee8b7cea56dbadbf7d4071c344cc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946362"
---
# <span data-ttu-id="223be-101">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="223be-101">Get-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="223be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="223be-102">SYNOPSIS</span></span>

<span data-ttu-id="223be-103">Obtém uma definição de runbook.</span><span class="sxs-lookup"><span data-stu-id="223be-103">Gets a runbook definition.</span></span>

## <span data-ttu-id="223be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="223be-104">SYNTAX</span></span>

```
Get-AzureAutomationRunbookDefinition -Name <String> [-Slot <String>] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="223be-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="223be-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="223be-106">O cmdlet **Get-AzureAutomationRunbookDefinition** Obtém a definição de rascunho, a definição publicada ou ambas as definições de um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="223be-106">The **Get-AzureAutomationRunbookDefinition** cmdlet gets the draft definition, the published definition, or both definitions of an Azure Automation runbook.</span></span>
<span data-ttu-id="223be-107">Por padrão, a versão publicada é retornada.</span><span class="sxs-lookup"><span data-stu-id="223be-107">By default, the published version is returned.</span></span>

## <span data-ttu-id="223be-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="223be-108">EXAMPLES</span></span>

### <span data-ttu-id="223be-109">Exemplo 1: obter uma definição de runbook</span><span class="sxs-lookup"><span data-stu-id="223be-109">Example 1: Get a runbook definition</span></span>
```
PS C:\> Get-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "RunbookDef01" -Slot "Published"
```

<span data-ttu-id="223be-110">Esse comando obtém a definição do runbook publicado do runbook chamado RunbookDef01 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="223be-110">This command gets the published runbook definition of the runbook named RunbookDef01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="223be-111">OS</span><span class="sxs-lookup"><span data-stu-id="223be-111">PARAMETERS</span></span>

### <span data-ttu-id="223be-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="223be-112">-AutomationAccountName</span></span>
<span data-ttu-id="223be-113">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="223be-113">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="223be-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="223be-114">-Name</span></span>
<span data-ttu-id="223be-115">Especifica o nome de um runbook.</span><span class="sxs-lookup"><span data-stu-id="223be-115">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="223be-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="223be-116">-Profile</span></span>
<span data-ttu-id="223be-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="223be-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="223be-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="223be-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="223be-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="223be-119">-Slot</span></span>
<span data-ttu-id="223be-120">Especifica o slot.</span><span class="sxs-lookup"><span data-stu-id="223be-120">Specifies the slot.</span></span>
<span data-ttu-id="223be-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="223be-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="223be-122">Provisório</span><span class="sxs-lookup"><span data-stu-id="223be-122">Draft</span></span>
- <span data-ttu-id="223be-123">Publish</span><span class="sxs-lookup"><span data-stu-id="223be-123">Published</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="223be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="223be-124">CommonParameters</span></span>
<span data-ttu-id="223be-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="223be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="223be-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="223be-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="223be-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="223be-127">INPUTS</span></span>

## <span data-ttu-id="223be-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="223be-128">OUTPUTS</span></span>

## <span data-ttu-id="223be-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="223be-129">NOTES</span></span>

## <span data-ttu-id="223be-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="223be-130">RELATED LINKS</span></span>

[<span data-ttu-id="223be-131">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="223be-131">Set-AzureAutomationRunbookDefinition</span></span>](./Set-AzureAutomationRunbookDefinition.md)


