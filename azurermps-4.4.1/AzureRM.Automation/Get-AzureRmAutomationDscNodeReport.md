---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: c3ae9da7959d606ec8ab92ed7a05e502d03b12a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431201"
---
# <span data-ttu-id="efbf4-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="efbf4-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="efbf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efbf4-102">SYNOPSIS</span></span>
<span data-ttu-id="efbf4-103">Obtém relatórios enviados de um nó DSC para automação.</span><span class="sxs-lookup"><span data-stu-id="efbf4-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efbf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efbf4-104">SYNTAX</span></span>

### <span data-ttu-id="efbf4-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="efbf4-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efbf4-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="efbf4-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efbf4-107">ById</span><span class="sxs-lookup"><span data-stu-id="efbf4-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efbf4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="efbf4-108">DESCRIPTION</span></span>
<span data-ttu-id="efbf4-109">O cmdlet **Get-AzureRmAutomationDscNodeReport** Obtém relatórios enviados de um nó DSC (configuração de estado desejado) do APS para a automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="efbf4-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="efbf4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="efbf4-110">EXAMPLES</span></span>

### <span data-ttu-id="efbf4-111">Exemplo 1: obter todos os relatórios para um nó DSC</span><span class="sxs-lookup"><span data-stu-id="efbf4-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="efbf4-112">O primeiro comando obtém o nó DSC do computador chamado Computer14 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="efbf4-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="efbf4-113">O comando armazena esse objeto na variável $Node.</span><span class="sxs-lookup"><span data-stu-id="efbf4-113">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="efbf4-114">O segundo comando obtém metadados para todos os relatórios enviados do nó DSC chamado Computer14 para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="efbf4-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="efbf4-115">O comando especifica o nó usando a propriedade **ID** do objeto $node.</span><span class="sxs-lookup"><span data-stu-id="efbf4-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="efbf4-116">Exemplo 2: obter um relatório para um nó DSC por ID do relatório</span><span class="sxs-lookup"><span data-stu-id="efbf4-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="efbf4-117">O primeiro comando obtém o nó DSC do computador chamado Computer14 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="efbf4-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="efbf4-118">O comando armazena esse objeto na variável $Node.</span><span class="sxs-lookup"><span data-stu-id="efbf4-118">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="efbf4-119">O segundo comando obtém metadados para o relatório identificado pela ID especificada enviada do nó DSC chamado Computer14 para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="efbf4-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="efbf4-120">Exemplo 3: obter o relatório mais recente para um nó DSC</span><span class="sxs-lookup"><span data-stu-id="efbf4-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="efbf4-121">O primeiro comando obtém o nó DSC do computador chamado Computer14 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="efbf4-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="efbf4-122">O comando armazena esse objeto na variável $Node.</span><span class="sxs-lookup"><span data-stu-id="efbf4-122">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="efbf4-123">O segundo comando obtém metadados para o relatório mais recente enviado do nó DSC chamado Computer14 para a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="efbf4-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="efbf4-124">OS</span><span class="sxs-lookup"><span data-stu-id="efbf4-124">PARAMETERS</span></span>

### <span data-ttu-id="efbf4-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="efbf4-125">-AutomationAccountName</span></span>
<span data-ttu-id="efbf4-126">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="efbf4-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="efbf4-127">Esse cmdlet exporta relatórios para um nó DSC que pertence à conta que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="efbf4-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="efbf4-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="efbf4-128">-EndTime</span></span>
<span data-ttu-id="efbf4-129">Especifica uma hora de término.</span><span class="sxs-lookup"><span data-stu-id="efbf4-129">Specifies an end time.</span></span>
<span data-ttu-id="efbf4-130">Esse cmdlet obtém relatórios que a automação recebeu antes desta hora.</span><span class="sxs-lookup"><span data-stu-id="efbf4-130">This cmdlet gets reports that Automation received before this time.</span></span>

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

### <span data-ttu-id="efbf4-131">-ID</span><span class="sxs-lookup"><span data-stu-id="efbf4-131">-Id</span></span>
<span data-ttu-id="efbf4-132">Especifica a ID exclusiva do relatório de nó DSC para obter esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efbf4-132">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

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

### <span data-ttu-id="efbf4-133">-Mais recente</span><span class="sxs-lookup"><span data-stu-id="efbf4-133">-Latest</span></span>
<span data-ttu-id="efbf4-134">Indica que esse cmdlet obtém o relatório DSC mais recente somente para o nó especificado.</span><span class="sxs-lookup"><span data-stu-id="efbf4-134">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

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

### <span data-ttu-id="efbf4-135">-NodeId</span><span class="sxs-lookup"><span data-stu-id="efbf4-135">-NodeId</span></span>
<span data-ttu-id="efbf4-136">Especifica a ID exclusiva do nó DSC para o qual esse cmdlet recebe relatórios.</span><span class="sxs-lookup"><span data-stu-id="efbf4-136">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="efbf4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efbf4-137">-ResourceGroupName</span></span>
<span data-ttu-id="efbf4-138">Especifica o nome de um grupo de recursos que contém o nó DSC para o qual esse cmdlet recebe relatórios.</span><span class="sxs-lookup"><span data-stu-id="efbf4-138">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="efbf4-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="efbf4-139">-StartTime</span></span>
<span data-ttu-id="efbf4-140">Especifica uma hora de início.</span><span class="sxs-lookup"><span data-stu-id="efbf4-140">Specifies a start time.</span></span>
<span data-ttu-id="efbf4-141">Esse cmdlet obtém relatórios que a automação recebeu após esse período.</span><span class="sxs-lookup"><span data-stu-id="efbf4-141">This cmdlet gets reports that Automation received after this time.</span></span>

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

### <span data-ttu-id="efbf4-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efbf4-142">-DefaultProfile</span></span>
<span data-ttu-id="efbf4-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="efbf4-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efbf4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efbf4-144">CommonParameters</span></span>
<span data-ttu-id="efbf4-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efbf4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efbf4-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efbf4-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efbf4-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="efbf4-147">INPUTS</span></span>

## <span data-ttu-id="efbf4-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="efbf4-148">OUTPUTS</span></span>

### <span data-ttu-id="efbf4-149">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="efbf4-149">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="efbf4-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="efbf4-150">NOTES</span></span>

## <span data-ttu-id="efbf4-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efbf4-151">RELATED LINKS</span></span>

[<span data-ttu-id="efbf4-152">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="efbf4-152">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="efbf4-153">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="efbf4-153">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)


