---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: bb88bc38f6102f18b4d45b3b80902886975e2628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889815"
---
# <span data-ttu-id="c02cf-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="c02cf-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="c02cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c02cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c02cf-103">Obtém relatórios enviados de um nó DSC para Automação.</span><span class="sxs-lookup"><span data-stu-id="c02cf-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="c02cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c02cf-104">SYNTAX</span></span>

### <span data-ttu-id="c02cf-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c02cf-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c02cf-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="c02cf-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c02cf-107">ById</span><span class="sxs-lookup"><span data-stu-id="c02cf-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c02cf-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c02cf-108">DESCRIPTION</span></span>
<span data-ttu-id="c02cf-109">O cmdlet **Get-AzAutomationDscNodeReport** obtém relatórios enviados de um nó DSC (Configuração de Estado Desejado) do APS para a Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="c02cf-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="c02cf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c02cf-110">EXAMPLES</span></span>

### <span data-ttu-id="c02cf-111">Exemplo 1: Obter todos os relatórios para um nó DSC</span><span class="sxs-lookup"><span data-stu-id="c02cf-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="c02cf-112">O primeiro comando obtém o nó DSC do computador chamado Computer14 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c02cf-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="c02cf-113">O comando armazena esse objeto na variável $Node.</span><span class="sxs-lookup"><span data-stu-id="c02cf-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="c02cf-114">O segundo comando obtém metadados para todos os relatórios enviados do nó DSC chamado Computer14 para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c02cf-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="c02cf-115">O comando especifica o nó usando a **propriedade Id** do objeto $Node.</span><span class="sxs-lookup"><span data-stu-id="c02cf-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="c02cf-116">Exemplo 2: Obter um relatório para um nó DSC por ID do relatório</span><span class="sxs-lookup"><span data-stu-id="c02cf-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="c02cf-117">O primeiro comando obtém o nó DSC do computador chamado Computer14 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c02cf-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="c02cf-118">O comando armazena esse objeto na variável $Node.</span><span class="sxs-lookup"><span data-stu-id="c02cf-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="c02cf-119">O segundo comando obtém metadados para o relatório identificado pela ID especificada enviada do nó DSC chamado Computer14 para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c02cf-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c02cf-120">Exemplo 3: Obter o relatório mais recente para um nó DSC</span><span class="sxs-lookup"><span data-stu-id="c02cf-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="c02cf-121">O primeiro comando obtém o nó DSC do computador chamado Computer14 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c02cf-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="c02cf-122">O comando armazena esse objeto na variável $Node.</span><span class="sxs-lookup"><span data-stu-id="c02cf-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="c02cf-123">O segundo comando obtém metadados para o relatório mais recente enviado do nó DSC chamado Computer14 para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c02cf-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c02cf-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c02cf-124">PARAMETERS</span></span>

### <span data-ttu-id="c02cf-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c02cf-125">-AutomationAccountName</span></span>
<span data-ttu-id="c02cf-126">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="c02cf-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="c02cf-127">Este cmdlet exporta relatórios para um nó DSC que pertence à conta especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c02cf-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="c02cf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c02cf-128">-DefaultProfile</span></span>
<span data-ttu-id="c02cf-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c02cf-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c02cf-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c02cf-130">-EndTime</span></span>
<span data-ttu-id="c02cf-131">Especifica uma hora de término.</span><span class="sxs-lookup"><span data-stu-id="c02cf-131">Specifies an end time.</span></span>
<span data-ttu-id="c02cf-132">Este cmdlet obtém relatórios que a Automação recebeu antes dessa hora.</span><span class="sxs-lookup"><span data-stu-id="c02cf-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02cf-133">-Id</span><span class="sxs-lookup"><span data-stu-id="c02cf-133">-Id</span></span>
<span data-ttu-id="c02cf-134">Especifica a ID exclusiva do relatório de nó DSC para este cmdlet obter.</span><span class="sxs-lookup"><span data-stu-id="c02cf-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02cf-135">-Latest</span><span class="sxs-lookup"><span data-stu-id="c02cf-135">-Latest</span></span>
<span data-ttu-id="c02cf-136">Indica que esse cmdlet obtém o relatório DSC mais recente apenas para o nó especificado.</span><span class="sxs-lookup"><span data-stu-id="c02cf-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02cf-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="c02cf-137">-NodeId</span></span>
<span data-ttu-id="c02cf-138">Especifica a ID exclusiva do nó DSC para o qual este cmdlet obtém relatórios.</span><span class="sxs-lookup"><span data-stu-id="c02cf-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="c02cf-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c02cf-139">-ResourceGroupName</span></span>
<span data-ttu-id="c02cf-140">Especifica o nome de um grupo de recursos que contém o nó DSC para o qual este cmdlet obtém relatórios.</span><span class="sxs-lookup"><span data-stu-id="c02cf-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="c02cf-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c02cf-141">-StartTime</span></span>
<span data-ttu-id="c02cf-142">Especifica uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="c02cf-142">Specifies a start time.</span></span>
<span data-ttu-id="c02cf-143">Este cmdlet recebe relatórios que a Automação recebeu após esse tempo.</span><span class="sxs-lookup"><span data-stu-id="c02cf-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02cf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02cf-144">CommonParameters</span></span>
<span data-ttu-id="c02cf-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c02cf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c02cf-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c02cf-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02cf-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c02cf-147">INPUTS</span></span>

### <span data-ttu-id="c02cf-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c02cf-148">System.Guid</span></span>

### <span data-ttu-id="c02cf-149">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c02cf-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c02cf-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c02cf-150">System.String</span></span>

## <span data-ttu-id="c02cf-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c02cf-151">OUTPUTS</span></span>

### <span data-ttu-id="c02cf-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="c02cf-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="c02cf-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="c02cf-153">NOTES</span></span>

## <span data-ttu-id="c02cf-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c02cf-154">RELATED LINKS</span></span>

[<span data-ttu-id="c02cf-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="c02cf-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="c02cf-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="c02cf-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


