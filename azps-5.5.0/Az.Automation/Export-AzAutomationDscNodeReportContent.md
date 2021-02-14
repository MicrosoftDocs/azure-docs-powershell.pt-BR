---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: dd29a092ec0ca3b24614b363147d4c50bf14dcbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116636"
---
# <span data-ttu-id="44caa-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="44caa-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="44caa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44caa-102">SYNOPSIS</span></span>
<span data-ttu-id="44caa-103">Exporta o conteúdo bruto de um relatório DSC enviado de um nó DSC para Automação.</span><span class="sxs-lookup"><span data-stu-id="44caa-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="44caa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44caa-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44caa-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="44caa-105">DESCRIPTION</span></span>
<span data-ttu-id="44caa-106">O cmdlet **Export-AzAutomationDscNodeReportContent** exporta o conteúdo bruto de um relatório DSC (Configuração de Estado Desejado) APS.</span><span class="sxs-lookup"><span data-stu-id="44caa-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="44caa-107">Um nó DSC envia um relatório DSC para a Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="44caa-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="44caa-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="44caa-108">EXAMPLES</span></span>

### <span data-ttu-id="44caa-109">Exemplo 1: Exportar um relatório de um nó DSC</span><span class="sxs-lookup"><span data-stu-id="44caa-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="44caa-110">Esse conjunto de comandos exporta o relatório mais recente do nó DSC chamado Computador14 para a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="44caa-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="44caa-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44caa-111">PARAMETERS</span></span>

### <span data-ttu-id="44caa-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="44caa-112">-AutomationAccountName</span></span>
<span data-ttu-id="44caa-113">Especifica o nome de uma conta de Automação.</span><span class="sxs-lookup"><span data-stu-id="44caa-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="44caa-114">Esse cmdlet exporta o conteúdo do relatório para um nó DSC que pertence à conta automação especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="44caa-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="44caa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44caa-115">-DefaultProfile</span></span>
<span data-ttu-id="44caa-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="44caa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44caa-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="44caa-117">-Force</span></span>
<span data-ttu-id="44caa-118">Indica que esse cmdlet substitui um arquivo local existente por um novo arquivo com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="44caa-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="44caa-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="44caa-119">-NodeId</span></span>
<span data-ttu-id="44caa-120">Especifica a ID exclusiva do nó DSC para o qual este cmdlet exporta o conteúdo do relatório.</span><span class="sxs-lookup"><span data-stu-id="44caa-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="44caa-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="44caa-121">-OutputFolder</span></span>
<span data-ttu-id="44caa-122">Especifica a pasta de saída onde este cmdlet exporta o conteúdo do relatório.</span><span class="sxs-lookup"><span data-stu-id="44caa-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="44caa-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="44caa-123">-ReportId</span></span>
<span data-ttu-id="44caa-124">Especifica a ID exclusiva do relatório de nó DSC que esse cmdlet exporta.</span><span class="sxs-lookup"><span data-stu-id="44caa-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="44caa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44caa-125">-ResourceGroupName</span></span>
<span data-ttu-id="44caa-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44caa-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="44caa-127">Esse cmdlet exporta o conteúdo de um relatório para o nó DSC que pertence ao grupo de recursos especificado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44caa-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="44caa-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="44caa-128">-Confirm</span></span>
<span data-ttu-id="44caa-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44caa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44caa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44caa-130">-WhatIf</span></span>
<span data-ttu-id="44caa-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="44caa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44caa-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44caa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44caa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44caa-133">CommonParameters</span></span>
<span data-ttu-id="44caa-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44caa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44caa-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44caa-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44caa-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="44caa-136">INPUTS</span></span>

### <span data-ttu-id="44caa-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="44caa-137">System.Guid</span></span>

### <span data-ttu-id="44caa-138">System.String</span><span class="sxs-lookup"><span data-stu-id="44caa-138">System.String</span></span>

## <span data-ttu-id="44caa-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="44caa-139">OUTPUTS</span></span>

### <span data-ttu-id="44caa-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="44caa-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="44caa-141">Notas</span><span class="sxs-lookup"><span data-stu-id="44caa-141">NOTES</span></span>

## <span data-ttu-id="44caa-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44caa-142">RELATED LINKS</span></span>

[<span data-ttu-id="44caa-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="44caa-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="44caa-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="44caa-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="44caa-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="44caa-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


