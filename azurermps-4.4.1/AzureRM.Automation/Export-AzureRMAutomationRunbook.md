---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: b78b992e74252f645faabcf284c817b1cb3c1d5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427007"
---
# <span data-ttu-id="b5b91-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5b91-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="b5b91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5b91-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b91-103">Exporta um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="b5b91-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5b91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5b91-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5b91-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5b91-105">DESCRIPTION</span></span>
<span data-ttu-id="b5b91-106">O cmdlet **Export-AzureRmAutomationRunbook** exporta um runbook de automação do Azure para um arquivo de script wps_2 (. ps1), para wps_2 ou wps_2 Runbooks de fluxo de trabalho, ou para um arquivo de runbook gráfico (. graphrunbook), para runbooks gráficos.</span><span class="sxs-lookup"><span data-stu-id="b5b91-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="b5b91-107">O nome do runbook se torna o nome do arquivo exportado.</span><span class="sxs-lookup"><span data-stu-id="b5b91-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="b5b91-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5b91-108">EXAMPLES</span></span>

### <span data-ttu-id="b5b91-109">Exemplo 1: exportar um runbook</span><span class="sxs-lookup"><span data-stu-id="b5b91-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="b5b91-110">Esse comando exporta a versão publicada de um runbook de automação para uma área de trabalho do usuário.</span><span class="sxs-lookup"><span data-stu-id="b5b91-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="b5b91-111">OS</span><span class="sxs-lookup"><span data-stu-id="b5b91-111">PARAMETERS</span></span>

### <span data-ttu-id="b5b91-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b5b91-112">-AutomationAccountName</span></span>
<span data-ttu-id="b5b91-113">Especifica o nome da conta de automação na qual esse cmdlet exporta um runbook.</span><span class="sxs-lookup"><span data-stu-id="b5b91-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="b5b91-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b5b91-114">-Force</span></span>
<span data-ttu-id="b5b91-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="b5b91-115">ps_force</span></span>

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

### <span data-ttu-id="b5b91-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5b91-116">-Name</span></span>
<span data-ttu-id="b5b91-117">Especifica o nome do runbook exportado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b91-117">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="b5b91-118">O nome do runbook se torna o nome do arquivo de exportação.</span><span class="sxs-lookup"><span data-stu-id="b5b91-118">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="b5b91-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="b5b91-119">-OutputFolder</span></span>
<span data-ttu-id="b5b91-120">Especifica o caminho de uma pasta na qual esse cmdlet cria o arquivo de exportação.</span><span class="sxs-lookup"><span data-stu-id="b5b91-120">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="b5b91-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5b91-121">-ResourceGroupName</span></span>
<span data-ttu-id="b5b91-122">Especifica o nome do grupo de recursos para o qual esse cmdlet exporta um runbook.</span><span class="sxs-lookup"><span data-stu-id="b5b91-122">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="b5b91-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="b5b91-123">-Slot</span></span>
<span data-ttu-id="b5b91-124">Especifica se esse cmdlet exporta o rascunho ou o conteúdo publicado do runbook.</span><span class="sxs-lookup"><span data-stu-id="b5b91-124">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="b5b91-125">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b5b91-125">Valid values are:</span></span> 

- <span data-ttu-id="b5b91-126">Publish</span><span class="sxs-lookup"><span data-stu-id="b5b91-126">Published</span></span> 
- <span data-ttu-id="b5b91-127">Provisório</span><span class="sxs-lookup"><span data-stu-id="b5b91-127">Draft</span></span>

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

### <span data-ttu-id="b5b91-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b5b91-128">-Confirm</span></span>
<span data-ttu-id="b5b91-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b91-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5b91-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5b91-130">-WhatIf</span></span>
<span data-ttu-id="b5b91-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b5b91-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5b91-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5b91-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5b91-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b91-133">-DefaultProfile</span></span>
<span data-ttu-id="b5b91-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b91-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5b91-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b91-135">CommonParameters</span></span>
<span data-ttu-id="b5b91-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b91-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b91-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b91-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b91-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5b91-138">INPUTS</span></span>

## <span data-ttu-id="b5b91-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5b91-139">OUTPUTS</span></span>

### <span data-ttu-id="b5b91-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="b5b91-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="b5b91-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5b91-141">NOTES</span></span>

## <span data-ttu-id="b5b91-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5b91-142">RELATED LINKS</span></span>

[<span data-ttu-id="b5b91-143">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5b91-143">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b5b91-144">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5b91-144">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b5b91-145">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5b91-145">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b5b91-146">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5b91-146">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b5b91-147">Publicar-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5b91-147">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b5b91-148">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5b91-148">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b5b91-149">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5b91-149">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b5b91-150">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b5b91-150">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


