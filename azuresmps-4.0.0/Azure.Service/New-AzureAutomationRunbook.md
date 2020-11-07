---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0B496085-670D-45F7-B989-D4541A3811FF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37d95c570cc1c12bc40704ec2a2d89fcbec7cf48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945934"
---
# <span data-ttu-id="a5079-101">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a5079-101">New-AzureAutomationRunbook</span></span>

## <span data-ttu-id="a5079-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5079-102">SYNOPSIS</span></span>

<span data-ttu-id="a5079-103">Cria um runbook.</span><span class="sxs-lookup"><span data-stu-id="a5079-103">Creates a runbook.</span></span>

## <span data-ttu-id="a5079-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5079-104">SYNTAX</span></span>

### <span data-ttu-id="a5079-105">ByRunbookName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a5079-105">ByRunbookName (Default)</span></span>
```
New-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a5079-106">ByPath</span><span class="sxs-lookup"><span data-stu-id="a5079-106">ByPath</span></span>
```
New-AzureAutomationRunbook -Path <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a5079-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5079-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a5079-108">O cmdlet **New-AzureAutomationRunbook** cria um novo runbook de automação do Microsoft Azure vazio.</span><span class="sxs-lookup"><span data-stu-id="a5079-108">The **New-AzureAutomationRunbook** cmdlet creates a new, empty Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="a5079-109">Especifique um nome para criar um novo runbook.</span><span class="sxs-lookup"><span data-stu-id="a5079-109">Specify a name to create a new runbook.</span></span>

<span data-ttu-id="a5079-110">Você também pode especificar o caminho para um arquivo de script do Windows PowerShell (. ps1) para importar um runbook.</span><span class="sxs-lookup"><span data-stu-id="a5079-110">You can also specify the path to a Windows PowerShell script (.ps1 ) file to import a runbook.</span></span>
<span data-ttu-id="a5079-111">O script a ser importado deve conter uma única definição de fluxo de trabalho do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5079-111">The script to import must contain a single Windows PowerShell Workflow definition.</span></span>
<span data-ttu-id="a5079-112">O nome do fluxo de trabalho do Windows PowerShell se torna o nome do runbook.</span><span class="sxs-lookup"><span data-stu-id="a5079-112">The name of this Windows PowerShell Workflow becomes the name of the runbook.</span></span>

## <span data-ttu-id="a5079-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5079-113">EXAMPLES</span></span>

### <span data-ttu-id="a5079-114">Exemplo 1: criar um runbook</span><span class="sxs-lookup"><span data-stu-id="a5079-114">Example 1: Create a runbook</span></span>
```
PS C:\> New-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02"
```

<span data-ttu-id="a5079-115">Esse comando cria um novo runbook chamado Runbook02 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a5079-115">This command creates a new runbook named Runbook02 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a5079-116">OS</span><span class="sxs-lookup"><span data-stu-id="a5079-116">PARAMETERS</span></span>

### <span data-ttu-id="a5079-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a5079-117">-AutomationAccountName</span></span>
<span data-ttu-id="a5079-118">Especifica o nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="a5079-118">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="a5079-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a5079-119">-Description</span></span>
<span data-ttu-id="a5079-120">Especifica uma descrição para o runbook.</span><span class="sxs-lookup"><span data-stu-id="a5079-120">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5079-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5079-121">-Name</span></span>
<span data-ttu-id="a5079-122">Especifica o nome do runbook.</span><span class="sxs-lookup"><span data-stu-id="a5079-122">Specifies the name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5079-123">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a5079-123">-Path</span></span>
<span data-ttu-id="a5079-124">Especifica o caminho.</span><span class="sxs-lookup"><span data-stu-id="a5079-124">Specifies the path.</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5079-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a5079-125">-Profile</span></span>
<span data-ttu-id="a5079-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a5079-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a5079-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a5079-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a5079-128">-Marcas</span><span class="sxs-lookup"><span data-stu-id="a5079-128">-Tags</span></span>
<span data-ttu-id="a5079-129">Especifica as marcas do runbook.</span><span class="sxs-lookup"><span data-stu-id="a5079-129">Specifies tags for the runbook.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5079-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5079-130">CommonParameters</span></span>
<span data-ttu-id="a5079-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5079-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5079-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5079-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5079-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5079-133">INPUTS</span></span>

## <span data-ttu-id="a5079-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5079-134">OUTPUTS</span></span>

### <span data-ttu-id="a5079-135">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="a5079-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="a5079-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5079-136">NOTES</span></span>

## <span data-ttu-id="a5079-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5079-137">RELATED LINKS</span></span>

[<span data-ttu-id="a5079-138">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a5079-138">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="a5079-139">Publicar-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a5079-139">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="a5079-140">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a5079-140">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="a5079-141">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a5079-141">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="a5079-142">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a5079-142">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


