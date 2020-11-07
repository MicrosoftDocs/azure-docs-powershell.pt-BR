---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C583BECF-7FC2-4A1F-9788-5CB19E73956C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9464e811597ba0fe5bfe2d53643c7b788c9be71e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946070"
---
# <span data-ttu-id="4e956-101">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="4e956-101">Set-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="4e956-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e956-102">SYNOPSIS</span></span>

<span data-ttu-id="4e956-103">Atualiza a definição de rascunho de um runbook.</span><span class="sxs-lookup"><span data-stu-id="4e956-103">Updates the draft definition of a runbook.</span></span>

## <span data-ttu-id="4e956-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e956-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbookDefinition -Name <String> -Path <String> [-Overwrite] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4e956-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e956-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4e956-106">O cmdlet **set-AzureAutomationRunbookDefinition** atualiza a definição de rascunho de um runbook de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e956-106">The **Set-AzureAutomationRunbookDefinition** cmdlet updates the draft definition of a Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="4e956-107">Especifique um arquivo de script do Windows PowerShell (. ps1) que contenha um runbook que se torna o runbook de rascunho.</span><span class="sxs-lookup"><span data-stu-id="4e956-107">Specify a Windows PowerShell script (.ps1) file that contains a runbook that becomes the draft runbook.</span></span>

<span data-ttu-id="4e956-108">Se já existir uma definição de rascunho, use o parâmetro *overwrite* para forçar o cmdlet a substituir o rascunho existente.</span><span class="sxs-lookup"><span data-stu-id="4e956-108">If a draft definition already exists, use the *Overwrite* parameter to force the cmdlet to overwrite the existing draft.</span></span>

## <span data-ttu-id="4e956-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e956-109">EXAMPLES</span></span>

### <span data-ttu-id="4e956-110">Exemplo 1: substituir uma definição de rascunho existente de um runbook</span><span class="sxs-lookup"><span data-stu-id="4e956-110">Example 1: Overwrite an existing draft definition of a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "Runbk01" -Path ".\App01.ps1" -Overwrite
```

<span data-ttu-id="4e956-111">Esse comando substitui a definição de rascunho existente de um runbook.</span><span class="sxs-lookup"><span data-stu-id="4e956-111">This command overwrites the existing draft definition of a runbook.</span></span>

## <span data-ttu-id="4e956-112">OS</span><span class="sxs-lookup"><span data-stu-id="4e956-112">PARAMETERS</span></span>

### <span data-ttu-id="4e956-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4e956-113">-AutomationAccountName</span></span>
<span data-ttu-id="4e956-114">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="4e956-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="4e956-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e956-115">-Name</span></span>
<span data-ttu-id="4e956-116">Especifica um nome.</span><span class="sxs-lookup"><span data-stu-id="4e956-116">Specifies a name.</span></span>

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

### <span data-ttu-id="4e956-117">-Substituir</span><span class="sxs-lookup"><span data-stu-id="4e956-117">-Overwrite</span></span>
<span data-ttu-id="4e956-118">Indica se uma definição de rascunho existente deve ser substituída.</span><span class="sxs-lookup"><span data-stu-id="4e956-118">Indicates whether to overwrite an existing draft definition.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e956-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="4e956-119">-Path</span></span>
<span data-ttu-id="4e956-120">Especifica o caminho para um runbook.</span><span class="sxs-lookup"><span data-stu-id="4e956-120">Specifies the path to a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e956-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4e956-121">-Profile</span></span>
<span data-ttu-id="4e956-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4e956-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4e956-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4e956-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4e956-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e956-124">CommonParameters</span></span>
<span data-ttu-id="4e956-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e956-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e956-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e956-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e956-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e956-127">INPUTS</span></span>

## <span data-ttu-id="4e956-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e956-128">OUTPUTS</span></span>

### <span data-ttu-id="4e956-129">Microsoft. Azure. Commands. Automation. Model. RunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="4e956-129">Microsoft.Azure.Commands.Automation.Model.RunbookDefinition</span></span>

## <span data-ttu-id="4e956-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e956-130">NOTES</span></span>

## <span data-ttu-id="4e956-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e956-131">RELATED LINKS</span></span>

[<span data-ttu-id="4e956-132">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="4e956-132">Get-AzureAutomationRunbookDefinition</span></span>](./Get-AzureAutomationRunbookDefinition.md)


