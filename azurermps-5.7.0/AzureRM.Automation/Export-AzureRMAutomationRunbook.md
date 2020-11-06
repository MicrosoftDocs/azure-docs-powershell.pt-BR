---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: 7bc8305c8b0d861398807f7eefae4a741f60cc52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610674"
---
# <span data-ttu-id="bbb7b-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bbb7b-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="bbb7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbb7b-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb7b-103">Exporta um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbb7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbb7b-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbb7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bbb7b-105">DESCRIPTION</span></span>
<span data-ttu-id="bbb7b-106">O cmdlet **Export-AzureRmAutomationRunbook** exporta um runbook de automação do Azure para um arquivo de script wps_2 (. ps1), para wps_2 ou wps_2 Runbooks de fluxo de trabalho, ou para um arquivo de runbook gráfico (. graphrunbook), para runbooks gráficos.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="bbb7b-107">O nome do runbook se torna o nome do arquivo exportado.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="bbb7b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbb7b-108">EXAMPLES</span></span>

### <span data-ttu-id="bbb7b-109">Exemplo 1: exportar um runbook</span><span class="sxs-lookup"><span data-stu-id="bbb7b-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="bbb7b-110">Esse comando exporta a versão publicada de um runbook de automação para uma área de trabalho do usuário.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="bbb7b-111">OS</span><span class="sxs-lookup"><span data-stu-id="bbb7b-111">PARAMETERS</span></span>

### <span data-ttu-id="bbb7b-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bbb7b-112">-AutomationAccountName</span></span>
<span data-ttu-id="bbb7b-113">Especifica o nome da conta de automação na qual esse cmdlet exporta um runbook.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb7b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb7b-114">-DefaultProfile</span></span>
<span data-ttu-id="bbb7b-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bbb7b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbb7b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bbb7b-116">-Force</span></span>
<span data-ttu-id="bbb7b-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="bbb7b-117">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb7b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbb7b-118">-Name</span></span>
<span data-ttu-id="bbb7b-119">Especifica o nome do runbook exportado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="bbb7b-120">O nome do runbook se torna o nome do arquivo de exportação.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-120">The name of the runbook becomes the name of the export file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb7b-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="bbb7b-121">-OutputFolder</span></span>
<span data-ttu-id="bbb7b-122">Especifica o caminho de uma pasta na qual esse cmdlet cria o arquivo de exportação.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="bbb7b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb7b-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbb7b-124">Especifica o nome do grupo de recursos para o qual esse cmdlet exporta um runbook.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb7b-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="bbb7b-125">-Slot</span></span>
<span data-ttu-id="bbb7b-126">Especifica se esse cmdlet exporta o rascunho ou o conteúdo publicado do runbook.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="bbb7b-127">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="bbb7b-127">Valid values are:</span></span> 

- <span data-ttu-id="bbb7b-128">Publish</span><span class="sxs-lookup"><span data-stu-id="bbb7b-128">Published</span></span> 
- <span data-ttu-id="bbb7b-129">Provisório</span><span class="sxs-lookup"><span data-stu-id="bbb7b-129">Draft</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb7b-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bbb7b-130">-Confirm</span></span>
<span data-ttu-id="bbb7b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbb7b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb7b-132">-WhatIf</span></span>
<span data-ttu-id="bbb7b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbb7b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbb7b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb7b-135">CommonParameters</span></span>
<span data-ttu-id="bbb7b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb7b-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbb7b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb7b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bbb7b-138">INPUTS</span></span>

### <span data-ttu-id="bbb7b-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bbb7b-139">None</span></span>
<span data-ttu-id="bbb7b-140">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="bbb7b-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bbb7b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bbb7b-141">OUTPUTS</span></span>

### <span data-ttu-id="bbb7b-142">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="bbb7b-142">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="bbb7b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bbb7b-143">NOTES</span></span>

## <span data-ttu-id="bbb7b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbb7b-144">RELATED LINKS</span></span>

[<span data-ttu-id="bbb7b-145">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bbb7b-145">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bbb7b-146">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bbb7b-146">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bbb7b-147">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bbb7b-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bbb7b-148">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bbb7b-148">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bbb7b-149">Publicar-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bbb7b-149">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bbb7b-150">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bbb7b-150">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bbb7b-151">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bbb7b-151">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="bbb7b-152">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bbb7b-152">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


