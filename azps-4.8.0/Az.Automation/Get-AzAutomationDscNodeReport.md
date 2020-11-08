---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: 81a50a8c805d05b47b934b899eff708031ac6beb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110640"
---
# <span data-ttu-id="646b4-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="646b4-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="646b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="646b4-102">SYNOPSIS</span></span>
<span data-ttu-id="646b4-103">Obtém relatórios enviados de um nó DSC para automação.</span><span class="sxs-lookup"><span data-stu-id="646b4-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="646b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="646b4-104">SYNTAX</span></span>

### <span data-ttu-id="646b4-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="646b4-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="646b4-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="646b4-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="646b4-107">ById</span><span class="sxs-lookup"><span data-stu-id="646b4-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="646b4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="646b4-108">DESCRIPTION</span></span>
<span data-ttu-id="646b4-109">O cmdlet **Get-AzAutomationDscNodeReport** Obtém relatórios enviados de um nó DSC (configuração de estado desejado) do APS para a automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="646b4-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="646b4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="646b4-110">EXAMPLES</span></span>

### <span data-ttu-id="646b4-111">Exemplo 1: obter todos os relatórios para um nó DSC</span><span class="sxs-lookup"><span data-stu-id="646b4-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="646b4-112">O primeiro comando obtém o nó DSC do computador chamado Computer14 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="646b4-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="646b4-113">O comando armazena esse objeto na variável $Node.</span><span class="sxs-lookup"><span data-stu-id="646b4-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="646b4-114">O segundo comando obtém metadados para todos os relatórios enviados do nó DSC chamado Computer14 para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="646b4-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="646b4-115">O comando especifica o nó usando a propriedade **ID** do objeto $node.</span><span class="sxs-lookup"><span data-stu-id="646b4-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="646b4-116">Exemplo 2: obter um relatório para um nó DSC por ID do relatório</span><span class="sxs-lookup"><span data-stu-id="646b4-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="646b4-117">O primeiro comando obtém o nó DSC do computador chamado Computer14 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="646b4-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="646b4-118">O comando armazena esse objeto na variável $Node.</span><span class="sxs-lookup"><span data-stu-id="646b4-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="646b4-119">O segundo comando obtém metadados para o relatório identificado pela ID especificada enviada do nó DSC chamado Computer14 para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="646b4-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="646b4-120">Exemplo 3: obter o relatório mais recente para um nó DSC</span><span class="sxs-lookup"><span data-stu-id="646b4-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="646b4-121">O primeiro comando obtém o nó DSC do computador chamado Computer14 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="646b4-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="646b4-122">O comando armazena esse objeto na variável $Node.</span><span class="sxs-lookup"><span data-stu-id="646b4-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="646b4-123">O segundo comando obtém metadados para o relatório mais recente enviado do nó DSC chamado Computer14 para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="646b4-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="646b4-124">OS</span><span class="sxs-lookup"><span data-stu-id="646b4-124">PARAMETERS</span></span>

### <span data-ttu-id="646b4-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="646b4-125">-AutomationAccountName</span></span>
<span data-ttu-id="646b4-126">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="646b4-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="646b4-127">Esse cmdlet exporta relatórios para um nó DSC que pertence à conta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="646b4-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="646b4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="646b4-128">-DefaultProfile</span></span>
<span data-ttu-id="646b4-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="646b4-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="646b4-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="646b4-130">-EndTime</span></span>
<span data-ttu-id="646b4-131">Especifica uma hora de término.</span><span class="sxs-lookup"><span data-stu-id="646b4-131">Specifies an end time.</span></span>
<span data-ttu-id="646b4-132">Esse cmdlet obtém relatórios que a automação recebeu antes desta hora.</span><span class="sxs-lookup"><span data-stu-id="646b4-132">This cmdlet gets reports that Automation received before this time.</span></span>

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

### <span data-ttu-id="646b4-133">-ID</span><span class="sxs-lookup"><span data-stu-id="646b4-133">-Id</span></span>
<span data-ttu-id="646b4-134">Especifica a ID exclusiva do relatório de nó DSC para obter esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="646b4-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

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

### <span data-ttu-id="646b4-135">-Mais recente</span><span class="sxs-lookup"><span data-stu-id="646b4-135">-Latest</span></span>
<span data-ttu-id="646b4-136">Indica que esse cmdlet obtém o relatório DSC mais recente somente para o nó especificado.</span><span class="sxs-lookup"><span data-stu-id="646b4-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

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

### <span data-ttu-id="646b4-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="646b4-137">-NodeId</span></span>
<span data-ttu-id="646b4-138">Especifica a ID exclusiva do nó DSC para o qual esse cmdlet recebe relatórios.</span><span class="sxs-lookup"><span data-stu-id="646b4-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="646b4-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="646b4-139">-ResourceGroupName</span></span>
<span data-ttu-id="646b4-140">Especifica o nome de um grupo de recursos que contém o nó DSC para o qual esse cmdlet recebe relatórios.</span><span class="sxs-lookup"><span data-stu-id="646b4-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="646b4-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="646b4-141">-StartTime</span></span>
<span data-ttu-id="646b4-142">Especifica uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="646b4-142">Specifies a start time.</span></span>
<span data-ttu-id="646b4-143">Esse cmdlet obtém relatórios que a automação recebeu após esse período.</span><span class="sxs-lookup"><span data-stu-id="646b4-143">This cmdlet gets reports that Automation received after this time.</span></span>

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

### <span data-ttu-id="646b4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646b4-144">CommonParameters</span></span>
<span data-ttu-id="646b4-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="646b4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646b4-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="646b4-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646b4-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="646b4-147">INPUTS</span></span>

### <span data-ttu-id="646b4-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="646b4-148">System.Guid</span></span>

### <span data-ttu-id="646b4-149">System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="646b4-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="646b4-150">System. String</span><span class="sxs-lookup"><span data-stu-id="646b4-150">System.String</span></span>

## <span data-ttu-id="646b4-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="646b4-151">OUTPUTS</span></span>

### <span data-ttu-id="646b4-152">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="646b4-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="646b4-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="646b4-153">NOTES</span></span>

## <span data-ttu-id="646b4-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="646b4-154">RELATED LINKS</span></span>

[<span data-ttu-id="646b4-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="646b4-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="646b4-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="646b4-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


