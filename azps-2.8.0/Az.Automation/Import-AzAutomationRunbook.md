---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
ms.openlocfilehash: 9ec19ee8e1e6a74de83f77b8dca4e2536af8e425
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597808"
---
# <span data-ttu-id="3fa77-101">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3fa77-101">Import-AzAutomationRunbook</span></span>

## <span data-ttu-id="3fa77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fa77-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa77-103">Importa um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="3fa77-103">Imports an Automation runbook.</span></span>

## <span data-ttu-id="3fa77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fa77-104">SYNTAX</span></span>

```
Import-AzAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fa77-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3fa77-105">DESCRIPTION</span></span>
<span data-ttu-id="3fa77-106">O cmdlet **Import-AzAutomationRunbook** importa um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="3fa77-106">The **Import-AzAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="3fa77-107">Especifique o caminho para um arquivo de script wps_2 (. ps1) a ser importado para os runbooks de fluxo de trabalho wps_2 e wps_2, o arquivo (. graphrunbook) para runbooks gráficos ou o arquivo (. py) dos runbooks do Python 2.</span><span class="sxs-lookup"><span data-stu-id="3fa77-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="3fa77-108">Para wps_2 runbooks de fluxo de trabalho, o script deve conter uma única definição de fluxo de trabalho wps_2 que corresponda ao nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3fa77-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="3fa77-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fa77-109">EXAMPLES</span></span>

### <span data-ttu-id="3fa77-110">Exemplo 1: importar um runbook de um arquivo</span><span class="sxs-lookup"><span data-stu-id="3fa77-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="3fa77-111">O primeiro comando atribui dois pares de chave/valor à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="3fa77-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="3fa77-112">O segundo comando importa um runbook gráfico chamado GraphicalRunbook06 para a conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="3fa77-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="3fa77-113">O comando também atribui as marcas armazenadas em $Tags.</span><span class="sxs-lookup"><span data-stu-id="3fa77-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="3fa77-114">OS</span><span class="sxs-lookup"><span data-stu-id="3fa77-114">PARAMETERS</span></span>

### <span data-ttu-id="3fa77-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3fa77-115">-AutomationAccountName</span></span>
<span data-ttu-id="3fa77-116">Especifica o nome da conta de automação na qual esse cmdlet importa um runbook.</span><span class="sxs-lookup"><span data-stu-id="3fa77-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="3fa77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa77-117">-DefaultProfile</span></span>
<span data-ttu-id="3fa77-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3fa77-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fa77-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3fa77-119">-Description</span></span>
<span data-ttu-id="3fa77-120">Especifica uma descrição do runbook importado.</span><span class="sxs-lookup"><span data-stu-id="3fa77-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="3fa77-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3fa77-121">-Force</span></span>
<span data-ttu-id="3fa77-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="3fa77-122">ps_force</span></span>

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

### <span data-ttu-id="3fa77-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="3fa77-123">-LogProgress</span></span>
<span data-ttu-id="3fa77-124">Especifica se o runbook registra informações de progresso.</span><span class="sxs-lookup"><span data-stu-id="3fa77-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="3fa77-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="3fa77-125">-LogVerbose</span></span>
<span data-ttu-id="3fa77-126">Especifica se o runbook registra informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="3fa77-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="3fa77-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="3fa77-127">-Name</span></span>
<span data-ttu-id="3fa77-128">Especifica o nome do runbook importado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fa77-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa77-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="3fa77-129">-Path</span></span>
<span data-ttu-id="3fa77-130">Especifica o caminho de um arquivo. ps1 ou. graphrunbook que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="3fa77-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa77-131">-Publicado</span><span class="sxs-lookup"><span data-stu-id="3fa77-131">-Published</span></span>
<span data-ttu-id="3fa77-132">Indica que esse cmdlet publica o runbook que ele importa.</span><span class="sxs-lookup"><span data-stu-id="3fa77-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="3fa77-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa77-133">-ResourceGroupName</span></span>
<span data-ttu-id="3fa77-134">Especifica o nome do grupo de recursos para o qual esse cmdlet importa um runbook.</span><span class="sxs-lookup"><span data-stu-id="3fa77-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="3fa77-135">-Marcas</span><span class="sxs-lookup"><span data-stu-id="3fa77-135">-Tags</span></span>
<span data-ttu-id="3fa77-136">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3fa77-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3fa77-137">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3fa77-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3fa77-138">-Digite</span><span class="sxs-lookup"><span data-stu-id="3fa77-138">-Type</span></span>
<span data-ttu-id="3fa77-139">Especifica o tipo de runbook que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="3fa77-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="3fa77-140">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="3fa77-140">Valid values are:</span></span>
- <span data-ttu-id="3fa77-141">™</span><span class="sxs-lookup"><span data-stu-id="3fa77-141">PowerShell</span></span>
- <span data-ttu-id="3fa77-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="3fa77-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="3fa77-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="3fa77-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="3fa77-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="3fa77-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="3fa77-145">Representar</span><span class="sxs-lookup"><span data-stu-id="3fa77-145">Graph</span></span>
- <span data-ttu-id="3fa77-146">Python2 o gráfico de valor está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="3fa77-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="3fa77-147">É equivalente a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="3fa77-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="3fa77-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3fa77-148">-Confirm</span></span>
<span data-ttu-id="3fa77-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fa77-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fa77-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa77-150">-WhatIf</span></span>
<span data-ttu-id="3fa77-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3fa77-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fa77-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fa77-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fa77-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa77-153">CommonParameters</span></span>
<span data-ttu-id="3fa77-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fa77-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa77-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fa77-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa77-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3fa77-156">INPUTS</span></span>

### <span data-ttu-id="3fa77-157">System. String</span><span class="sxs-lookup"><span data-stu-id="3fa77-157">System.String</span></span>

### <span data-ttu-id="3fa77-158">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="3fa77-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="3fa77-159">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3fa77-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3fa77-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3fa77-160">OUTPUTS</span></span>

### <span data-ttu-id="3fa77-161">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="3fa77-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="3fa77-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3fa77-162">NOTES</span></span>

## <span data-ttu-id="3fa77-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fa77-163">RELATED LINKS</span></span>

[<span data-ttu-id="3fa77-164">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3fa77-164">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="3fa77-165">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3fa77-165">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="3fa77-166">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3fa77-166">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="3fa77-167">Publicar-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3fa77-167">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="3fa77-168">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3fa77-168">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="3fa77-169">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3fa77-169">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="3fa77-170">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3fa77-170">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
