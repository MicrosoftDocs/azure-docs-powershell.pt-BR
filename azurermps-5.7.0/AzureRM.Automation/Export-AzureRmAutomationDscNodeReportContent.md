---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
ms.openlocfilehash: aba2a95492a72f1b88aec4f38a037b315ede17a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431086"
---
# <span data-ttu-id="1f998-101">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="1f998-101">Export-AzureRmAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="1f998-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f998-102">SYNOPSIS</span></span>
<span data-ttu-id="1f998-103">Exporta o conteúdo bruto de um relatório DSC enviado de um nó DSC para automação.</span><span class="sxs-lookup"><span data-stu-id="1f998-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f998-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f998-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f998-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f998-105">DESCRIPTION</span></span>
<span data-ttu-id="1f998-106">O cmdlet **Export-AzureRmAutomationDscNodeReportContent** exporta o conteúdo bruto de um relatório DSC (configuração de estado desejado APS).</span><span class="sxs-lookup"><span data-stu-id="1f998-106">The **Export-AzureRmAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="1f998-107">Um nó DSC envia um relatório DSC para a automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="1f998-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="1f998-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f998-108">EXAMPLES</span></span>

### <span data-ttu-id="1f998-109">Exemplo 1: exportar um relatório de um nó DSC</span><span class="sxs-lookup"><span data-stu-id="1f998-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzureRmAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="1f998-110">Esse conjunto de comandos exporta o relatório mais recente do nó DSC chamado Computer14 para a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1f998-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="1f998-111">OS</span><span class="sxs-lookup"><span data-stu-id="1f998-111">PARAMETERS</span></span>

### <span data-ttu-id="1f998-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1f998-112">-AutomationAccountName</span></span>
<span data-ttu-id="1f998-113">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="1f998-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="1f998-114">Esse cmdlet exporta o conteúdo do relatório para um nó DSC que pertence à conta de automação que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1f998-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="1f998-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f998-115">-DefaultProfile</span></span>
<span data-ttu-id="1f998-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1f998-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f998-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1f998-117">-Force</span></span>
<span data-ttu-id="1f998-118">Indica que esse cmdlet substitui um arquivo local existente por um novo arquivo que tem o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="1f998-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="1f998-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="1f998-119">-NodeId</span></span>
<span data-ttu-id="1f998-120">Especifica a ID exclusiva do nó DSC para o qual esse cmdlet exporta conteúdo do relatório.</span><span class="sxs-lookup"><span data-stu-id="1f998-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f998-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="1f998-121">-OutputFolder</span></span>
<span data-ttu-id="1f998-122">Especifica a pasta de saída na qual esse cmdlet exporta o conteúdo do relatório.</span><span class="sxs-lookup"><span data-stu-id="1f998-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="1f998-123">-ReportID</span><span class="sxs-lookup"><span data-stu-id="1f998-123">-ReportId</span></span>
<span data-ttu-id="1f998-124">Especifica a ID exclusiva do relatório de nó DSC que este cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="1f998-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f998-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f998-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f998-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f998-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1f998-127">Esse cmdlet exporta o conteúdo de um relatório para o nó DSC que pertence ao grupo de recursos especificado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f998-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="1f998-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f998-128">-Confirm</span></span>
<span data-ttu-id="1f998-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f998-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f998-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f998-130">-WhatIf</span></span>
<span data-ttu-id="1f998-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f998-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f998-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f998-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f998-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f998-133">CommonParameters</span></span>
<span data-ttu-id="1f998-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f998-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f998-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f998-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f998-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f998-136">INPUTS</span></span>

### <span data-ttu-id="1f998-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1f998-137">None</span></span>
<span data-ttu-id="1f998-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1f998-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f998-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f998-139">OUTPUTS</span></span>

### <span data-ttu-id="1f998-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="1f998-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="1f998-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f998-141">NOTES</span></span>

## <span data-ttu-id="1f998-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f998-142">RELATED LINKS</span></span>

[<span data-ttu-id="1f998-143">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="1f998-143">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

[<span data-ttu-id="1f998-144">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="1f998-144">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="1f998-145">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="1f998-145">Get-AzureRmAutomationDscNodeReport</span></span>](./Get-AzureRmAutomationDscNodeReport.md)


