---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
ms.openlocfilehash: 25690d1e125dbfe2a7588665ff4dbc71215e21d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944967"
---
# <span data-ttu-id="bea9c-101">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bea9c-101">New-AzAutomationRunbook</span></span>

## <span data-ttu-id="bea9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bea9c-102">SYNOPSIS</span></span>
<span data-ttu-id="bea9c-103">Cria um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="bea9c-103">Creates an Automation runbook.</span></span>

## <span data-ttu-id="bea9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bea9c-104">SYNTAX</span></span>

```
New-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bea9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bea9c-105">DESCRIPTION</span></span>
<span data-ttu-id="bea9c-106">O cmdlet **New-AzAutomationRunbook** cria um runbook de automação do Azure vazio usando APS.</span><span class="sxs-lookup"><span data-stu-id="bea9c-106">The **New-AzAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="bea9c-107">Especifique um nome para o runbook.</span><span class="sxs-lookup"><span data-stu-id="bea9c-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="bea9c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bea9c-108">EXAMPLES</span></span>

### <span data-ttu-id="bea9c-109">Exemplo 1: criar um runbook</span><span class="sxs-lookup"><span data-stu-id="bea9c-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bea9c-110">Esse comando cria um runbook chamado Runbook02 na conta de automação do Azure chamado Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bea9c-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="bea9c-111">OS</span><span class="sxs-lookup"><span data-stu-id="bea9c-111">PARAMETERS</span></span>

### <span data-ttu-id="bea9c-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bea9c-112">-AutomationAccountName</span></span>
<span data-ttu-id="bea9c-113">Especifica o nome da conta de automação na qual esse cmdlet cria um runbook.</span><span class="sxs-lookup"><span data-stu-id="bea9c-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="bea9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea9c-114">-DefaultProfile</span></span>
<span data-ttu-id="bea9c-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bea9c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bea9c-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="bea9c-116">-Description</span></span>
<span data-ttu-id="bea9c-117">Especifica uma descrição para o runbook.</span><span class="sxs-lookup"><span data-stu-id="bea9c-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="bea9c-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="bea9c-118">-LogProgress</span></span>
<span data-ttu-id="bea9c-119">Especifica se o runbook registra o progresso.</span><span class="sxs-lookup"><span data-stu-id="bea9c-119">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea9c-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="bea9c-120">-LogVerbose</span></span>
<span data-ttu-id="bea9c-121">Especifica se o registro em log inclui informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="bea9c-121">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea9c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bea9c-122">-Name</span></span>
<span data-ttu-id="bea9c-123">Especifica um nome para o runbook.</span><span class="sxs-lookup"><span data-stu-id="bea9c-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="bea9c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea9c-124">-ResourceGroupName</span></span>
<span data-ttu-id="bea9c-125">Especifica o nome do grupo de recursos para o qual esse cmdlet cria um runbook.</span><span class="sxs-lookup"><span data-stu-id="bea9c-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="bea9c-126">-Marcas</span><span class="sxs-lookup"><span data-stu-id="bea9c-126">-Tags</span></span>
<span data-ttu-id="bea9c-127">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bea9c-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bea9c-128">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="bea9c-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea9c-129">-Digite</span><span class="sxs-lookup"><span data-stu-id="bea9c-129">-Type</span></span>
<span data-ttu-id="bea9c-130">Especifica o tipo de runbook que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="bea9c-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="bea9c-131">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="bea9c-131">Valid values are:</span></span>
- <span data-ttu-id="bea9c-132">™</span><span class="sxs-lookup"><span data-stu-id="bea9c-132">PowerShell</span></span>
- <span data-ttu-id="bea9c-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="bea9c-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="bea9c-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="bea9c-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="bea9c-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="bea9c-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="bea9c-136">Representar</span><span class="sxs-lookup"><span data-stu-id="bea9c-136">Graph</span></span>
- <span data-ttu-id="bea9c-137">Python2 o gráfico de valor está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="bea9c-137">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="bea9c-138">É equivalente a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="bea9c-138">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea9c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea9c-139">CommonParameters</span></span>
<span data-ttu-id="bea9c-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea9c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea9c-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea9c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea9c-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bea9c-142">INPUTS</span></span>

### <span data-ttu-id="bea9c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bea9c-143">System.String</span></span>

### <span data-ttu-id="bea9c-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="bea9c-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="bea9c-145">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bea9c-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bea9c-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bea9c-146">OUTPUTS</span></span>

### <span data-ttu-id="bea9c-147">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="bea9c-147">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="bea9c-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bea9c-148">NOTES</span></span>

## <span data-ttu-id="bea9c-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bea9c-149">RELATED LINKS</span></span>

[<span data-ttu-id="bea9c-150">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bea9c-150">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="bea9c-151">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bea9c-151">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="bea9c-152">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bea9c-152">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="bea9c-153">Publicar-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bea9c-153">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="bea9c-154">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bea9c-154">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="bea9c-155">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bea9c-155">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="bea9c-156">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bea9c-156">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
