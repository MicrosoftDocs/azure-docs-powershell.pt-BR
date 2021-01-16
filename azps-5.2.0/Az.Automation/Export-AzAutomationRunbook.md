---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 03a57c35063a401aa5f730e11538532bdbbbc58c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259449"
---
# <span data-ttu-id="1194f-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1194f-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="1194f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1194f-102">SYNOPSIS</span></span>
<span data-ttu-id="1194f-103">Exporta um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="1194f-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="1194f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1194f-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1194f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1194f-105">DESCRIPTION</span></span>
<span data-ttu-id="1194f-106">O cmdlet **Export-AzAutomationRunbook** exporta um runbook de automação do Azure para um arquivo de script wps_2 (. ps1), para wps_2 ou wps_2 Runbooks de fluxo de trabalho, ou para um arquivo de runbook gráfico (. graphrunbook), para runbooks gráficos.</span><span class="sxs-lookup"><span data-stu-id="1194f-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="1194f-107">O nome do runbook se torna o nome do arquivo exportado.</span><span class="sxs-lookup"><span data-stu-id="1194f-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="1194f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1194f-108">EXAMPLES</span></span>

### <span data-ttu-id="1194f-109">Exemplo 1: exportar um runbook</span><span class="sxs-lookup"><span data-stu-id="1194f-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="1194f-110">Esse comando exporta a versão publicada de um runbook de automação para uma área de trabalho do usuário.</span><span class="sxs-lookup"><span data-stu-id="1194f-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="1194f-111">OS</span><span class="sxs-lookup"><span data-stu-id="1194f-111">PARAMETERS</span></span>

### <span data-ttu-id="1194f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1194f-112">-AutomationAccountName</span></span>
<span data-ttu-id="1194f-113">Especifica o nome da conta de automação na qual esse cmdlet exporta um runbook.</span><span class="sxs-lookup"><span data-stu-id="1194f-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1194f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1194f-114">-DefaultProfile</span></span>
<span data-ttu-id="1194f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1194f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1194f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1194f-116">-Force</span></span>
<span data-ttu-id="1194f-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="1194f-117">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1194f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1194f-118">-Name</span></span>
<span data-ttu-id="1194f-119">Especifica o nome do runbook exportado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1194f-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="1194f-120">O nome do runbook se torna o nome do arquivo de exportação.</span><span class="sxs-lookup"><span data-stu-id="1194f-120">The name of the runbook becomes the name of the export file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1194f-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="1194f-121">-OutputFolder</span></span>
<span data-ttu-id="1194f-122">Especifica o caminho de uma pasta na qual esse cmdlet cria o arquivo de exportação.</span><span class="sxs-lookup"><span data-stu-id="1194f-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1194f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1194f-123">-ResourceGroupName</span></span>
<span data-ttu-id="1194f-124">Especifica o nome do grupo de recursos para o qual esse cmdlet exporta um runbook.</span><span class="sxs-lookup"><span data-stu-id="1194f-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1194f-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="1194f-125">-Slot</span></span>
<span data-ttu-id="1194f-126">Especifica se esse cmdlet exporta o rascunho ou o conteúdo publicado do runbook.</span><span class="sxs-lookup"><span data-stu-id="1194f-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="1194f-127">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="1194f-127">Valid values are:</span></span> 
- <span data-ttu-id="1194f-128">Publish</span><span class="sxs-lookup"><span data-stu-id="1194f-128">Published</span></span> 
- <span data-ttu-id="1194f-129">Provisório</span><span class="sxs-lookup"><span data-stu-id="1194f-129">Draft</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1194f-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1194f-130">-Confirm</span></span>
<span data-ttu-id="1194f-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1194f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1194f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1194f-132">-WhatIf</span></span>
<span data-ttu-id="1194f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1194f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1194f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1194f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1194f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1194f-135">CommonParameters</span></span>
<span data-ttu-id="1194f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1194f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1194f-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1194f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1194f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1194f-138">INPUTS</span></span>

### <span data-ttu-id="1194f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1194f-139">System.String</span></span>

## <span data-ttu-id="1194f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1194f-140">OUTPUTS</span></span>

### <span data-ttu-id="1194f-141">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="1194f-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="1194f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1194f-142">NOTES</span></span>

## <span data-ttu-id="1194f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1194f-143">RELATED LINKS</span></span>

[<span data-ttu-id="1194f-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1194f-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="1194f-145">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1194f-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="1194f-146">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1194f-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1194f-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1194f-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1194f-148">Publicar-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1194f-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="1194f-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1194f-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="1194f-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1194f-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="1194f-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1194f-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


