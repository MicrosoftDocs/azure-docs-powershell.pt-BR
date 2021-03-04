---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: c4006c13130cecb27c35d466c43cfd75583644b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888335"
---
# <span data-ttu-id="a1dde-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="a1dde-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="a1dde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1dde-102">SYNOPSIS</span></span>
<span data-ttu-id="a1dde-103">Exporta o conteúdo bruto de um relatório DSC enviado de um nó DSC para Automação.</span><span class="sxs-lookup"><span data-stu-id="a1dde-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="a1dde-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a1dde-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1dde-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a1dde-105">DESCRIPTION</span></span>
<span data-ttu-id="a1dde-106">O cmdlet **Export-AzAutomationDscNodeReportContent** exporta o conteúdo bruto de um relatório de Configuração de Estado Desejado (DSC) do APS.</span><span class="sxs-lookup"><span data-stu-id="a1dde-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="a1dde-107">Um nó DSC envia um relatório DSC para a Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1dde-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="a1dde-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1dde-108">EXAMPLES</span></span>

### <span data-ttu-id="a1dde-109">Exemplo 1: Exportar um relatório de um nó DSC</span><span class="sxs-lookup"><span data-stu-id="a1dde-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="a1dde-110">Esse conjunto de comandos exporta o relatório mais recente do nó DSC chamado Computer14 para a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a1dde-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="a1dde-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a1dde-111">PARAMETERS</span></span>

### <span data-ttu-id="a1dde-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a1dde-112">-AutomationAccountName</span></span>
<span data-ttu-id="a1dde-113">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="a1dde-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="a1dde-114">Este cmdlet exporta conteúdo de relatório para um nó DSC que pertence à conta de Automação especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a1dde-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1dde-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1dde-115">-DefaultProfile</span></span>
<span data-ttu-id="a1dde-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a1dde-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1dde-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a1dde-117">-Force</span></span>
<span data-ttu-id="a1dde-118">Indica que esse cmdlet substitui um arquivo local existente por um novo arquivo com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="a1dde-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="a1dde-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="a1dde-119">-NodeId</span></span>
<span data-ttu-id="a1dde-120">Especifica a ID exclusiva do nó DSC para o qual este cmdlet exporta o conteúdo do relatório.</span><span class="sxs-lookup"><span data-stu-id="a1dde-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1dde-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="a1dde-121">-OutputFolder</span></span>
<span data-ttu-id="a1dde-122">Especifica a pasta de saída na qual esse cmdlet exporta o conteúdo do relatório.</span><span class="sxs-lookup"><span data-stu-id="a1dde-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="a1dde-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="a1dde-123">-ReportId</span></span>
<span data-ttu-id="a1dde-124">Especifica a ID exclusiva do relatório de nó DSC que esse cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="a1dde-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1dde-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1dde-125">-ResourceGroupName</span></span>
<span data-ttu-id="a1dde-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1dde-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a1dde-127">Este cmdlet exporta o conteúdo de um relatório para o nó DSC que pertence ao grupo de recursos especificado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1dde-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="a1dde-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1dde-128">-Confirm</span></span>
<span data-ttu-id="a1dde-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1dde-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1dde-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1dde-130">-WhatIf</span></span>
<span data-ttu-id="a1dde-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1dde-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1dde-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1dde-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1dde-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1dde-133">CommonParameters</span></span>
<span data-ttu-id="a1dde-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1dde-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1dde-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1dde-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1dde-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1dde-136">INPUTS</span></span>

### <span data-ttu-id="a1dde-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a1dde-137">System.Guid</span></span>

### <span data-ttu-id="a1dde-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a1dde-138">System.String</span></span>

## <span data-ttu-id="a1dde-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a1dde-139">OUTPUTS</span></span>

### <span data-ttu-id="a1dde-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="a1dde-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="a1dde-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="a1dde-141">NOTES</span></span>

## <span data-ttu-id="a1dde-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1dde-142">RELATED LINKS</span></span>

[<span data-ttu-id="a1dde-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="a1dde-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="a1dde-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a1dde-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="a1dde-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="a1dde-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


