---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1f7c50f0f5b11c80fce203b0c44128e380834bdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426827"
---
# <span data-ttu-id="481dd-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="481dd-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="481dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="481dd-102">SYNOPSIS</span></span>
<span data-ttu-id="481dd-103">Importa um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="481dd-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="481dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="481dd-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="481dd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="481dd-105">DESCRIPTION</span></span>
<span data-ttu-id="481dd-106">O cmdlet **Import-AzureRmAutomationRunbook** importa um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="481dd-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="481dd-107">Especifique o caminho para um arquivo de script wps_2 (. ps1) a ser importado para os runbooks de fluxo de trabalho wps_2 e wps_2, o arquivo (. graphrunbook) para runbooks gráficos ou o arquivo (. py) dos runbooks do Python 2.</span><span class="sxs-lookup"><span data-stu-id="481dd-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="481dd-108">Para wps_2 runbooks de fluxo de trabalho, o script deve conter uma única definição de fluxo de trabalho wps_2 que corresponda ao nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="481dd-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="481dd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="481dd-109">EXAMPLES</span></span>

### <span data-ttu-id="481dd-110">Exemplo 1: importar um runbook de um arquivo</span><span class="sxs-lookup"><span data-stu-id="481dd-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="481dd-111">O primeiro comando atribui dois pares de chave/valor à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="481dd-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="481dd-112">O segundo comando importa um runbook gráfico chamado GraphicalRunbook06 para a conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="481dd-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="481dd-113">O comando também atribui as marcas armazenadas em $Tags.</span><span class="sxs-lookup"><span data-stu-id="481dd-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="481dd-114">OS</span><span class="sxs-lookup"><span data-stu-id="481dd-114">PARAMETERS</span></span>

### <span data-ttu-id="481dd-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="481dd-115">-AutomationAccountName</span></span>
<span data-ttu-id="481dd-116">Especifica o nome da conta de automação na qual esse cmdlet importa um runbook.</span><span class="sxs-lookup"><span data-stu-id="481dd-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="481dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="481dd-117">-DefaultProfile</span></span>
<span data-ttu-id="481dd-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="481dd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="481dd-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="481dd-119">-Description</span></span>
<span data-ttu-id="481dd-120">Especifica uma descrição do runbook importado.</span><span class="sxs-lookup"><span data-stu-id="481dd-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="481dd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="481dd-121">-Force</span></span>
<span data-ttu-id="481dd-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="481dd-122">ps_force</span></span>

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

### <span data-ttu-id="481dd-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="481dd-123">-LogProgress</span></span>
<span data-ttu-id="481dd-124">Especifica se o runbook registra informações de progresso.</span><span class="sxs-lookup"><span data-stu-id="481dd-124">Specifies whether the runbook logs progress information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481dd-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="481dd-125">-LogVerbose</span></span>
<span data-ttu-id="481dd-126">Especifica se o runbook registra informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="481dd-126">Specifies whether the runbook logs detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481dd-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="481dd-127">-Name</span></span>
<span data-ttu-id="481dd-128">Especifica o nome do runbook importado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="481dd-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481dd-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="481dd-129">-Path</span></span>
<span data-ttu-id="481dd-130">Especifica o caminho de um arquivo. ps1 ou. graphrunbook que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="481dd-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481dd-131">-Publicado</span><span class="sxs-lookup"><span data-stu-id="481dd-131">-Published</span></span>
<span data-ttu-id="481dd-132">Indica que esse cmdlet publica o runbook que ele importa.</span><span class="sxs-lookup"><span data-stu-id="481dd-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="481dd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="481dd-133">-ResourceGroupName</span></span>
<span data-ttu-id="481dd-134">Especifica o nome do grupo de recursos para o qual esse cmdlet importa um runbook.</span><span class="sxs-lookup"><span data-stu-id="481dd-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="481dd-135">-Marcas</span><span class="sxs-lookup"><span data-stu-id="481dd-135">-Tags</span></span>
<span data-ttu-id="481dd-136">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="481dd-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="481dd-137">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="481dd-137">For example:</span></span>

<span data-ttu-id="481dd-138">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="481dd-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481dd-139">-Digite</span><span class="sxs-lookup"><span data-stu-id="481dd-139">-Type</span></span>
<span data-ttu-id="481dd-140">Especifica o tipo de runbook que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="481dd-140">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="481dd-141">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="481dd-141">Valid values are:</span></span>

- <span data-ttu-id="481dd-142">™</span><span class="sxs-lookup"><span data-stu-id="481dd-142">PowerShell</span></span>
- <span data-ttu-id="481dd-143">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="481dd-143">GraphicalPowerShell</span></span>
- <span data-ttu-id="481dd-144">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="481dd-144">PowerShellWorkflow</span></span>
- <span data-ttu-id="481dd-145">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="481dd-145">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="481dd-146">Representar</span><span class="sxs-lookup"><span data-stu-id="481dd-146">Graph</span></span>
- <span data-ttu-id="481dd-147">Python2</span><span class="sxs-lookup"><span data-stu-id="481dd-147">Python2</span></span>

<span data-ttu-id="481dd-148">O gráfico de valor é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="481dd-148">The value Graph is obsolete.</span></span>
<span data-ttu-id="481dd-149">É equivalente a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="481dd-149">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481dd-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="481dd-150">-Confirm</span></span>
<span data-ttu-id="481dd-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="481dd-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="481dd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="481dd-152">-WhatIf</span></span>
<span data-ttu-id="481dd-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="481dd-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="481dd-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="481dd-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="481dd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="481dd-155">CommonParameters</span></span>
<span data-ttu-id="481dd-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="481dd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="481dd-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="481dd-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="481dd-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="481dd-158">INPUTS</span></span>

### <span data-ttu-id="481dd-159">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="481dd-159">None</span></span>
<span data-ttu-id="481dd-160">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="481dd-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="481dd-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="481dd-161">OUTPUTS</span></span>

### <span data-ttu-id="481dd-162">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="481dd-162">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="481dd-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="481dd-163">NOTES</span></span>

## <span data-ttu-id="481dd-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="481dd-164">RELATED LINKS</span></span>

[<span data-ttu-id="481dd-165">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="481dd-165">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="481dd-166">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="481dd-166">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="481dd-167">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="481dd-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="481dd-168">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="481dd-168">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="481dd-169">Publicar-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="481dd-169">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="481dd-170">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="481dd-170">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="481dd-171">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="481dd-171">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="481dd-172">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="481dd-172">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
