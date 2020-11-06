---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: d28166ec0a9a339017aa11bc30c0c5f0394afe94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431187"
---
# <span data-ttu-id="232e3-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232e3-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="232e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="232e3-102">SYNOPSIS</span></span>
<span data-ttu-id="232e3-103">Importa um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="232e3-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="232e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="232e3-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="232e3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="232e3-105">DESCRIPTION</span></span>
<span data-ttu-id="232e3-106">O cmdlet **Import-AzureRmAutomationRunbook** importa um runbook de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="232e3-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="232e3-107">Especifique o caminho para um arquivo de script wps_2 (. ps1) a ser importado para wps_2 e wps_2 runbooks de fluxo de trabalho ou para um arquivo de runbook gráfico (. graphrunbook) para runbooks gráficos.</span><span class="sxs-lookup"><span data-stu-id="232e3-107">Specify the path to a wps_2 script (.ps1 ) file to import for wps_2 and wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file for graphical runbooks.</span></span> <span data-ttu-id="232e3-108">O nome do arquivo se torna o nome do runbook.</span><span class="sxs-lookup"><span data-stu-id="232e3-108">The name of the file becomes the name of the runbook.</span></span> <span data-ttu-id="232e3-109">Para wps_2 runbooks de fluxo de trabalho, o script deve conter uma única definição de fluxo de trabalho wps_2 que corresponda ao nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="232e3-109">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="232e3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="232e3-110">EXAMPLES</span></span>

### <span data-ttu-id="232e3-111">Exemplo 1: importar um runbook de um arquivo</span><span class="sxs-lookup"><span data-stu-id="232e3-111">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="232e3-112">O primeiro comando atribui dois pares de chave/valor à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="232e3-112">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="232e3-113">O segundo comando importa um runbook gráfico chamado GraphicalRunbook06 para a conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="232e3-113">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="232e3-114">O comando também atribui as marcas armazenadas em $Tags.</span><span class="sxs-lookup"><span data-stu-id="232e3-114">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="232e3-115">OS</span><span class="sxs-lookup"><span data-stu-id="232e3-115">PARAMETERS</span></span>

### <span data-ttu-id="232e3-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="232e3-116">-AutomationAccountName</span></span>
<span data-ttu-id="232e3-117">Especifica o nome da conta de automação na qual esse cmdlet importa um runbook.</span><span class="sxs-lookup"><span data-stu-id="232e3-117">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="232e3-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="232e3-118">-Description</span></span>
<span data-ttu-id="232e3-119">Especifica uma descrição do runbook importado.</span><span class="sxs-lookup"><span data-stu-id="232e3-119">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="232e3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="232e3-120">-Force</span></span>
<span data-ttu-id="232e3-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="232e3-121">ps_force</span></span>

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

### <span data-ttu-id="232e3-122">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="232e3-122">-LogProgress</span></span>
<span data-ttu-id="232e3-123">Especifica se o runbook registra informações de progresso.</span><span class="sxs-lookup"><span data-stu-id="232e3-123">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="232e3-124">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="232e3-124">-LogVerbose</span></span>
<span data-ttu-id="232e3-125">Especifica se o runbook registra informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="232e3-125">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="232e3-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="232e3-126">-Name</span></span>
<span data-ttu-id="232e3-127">Especifica o nome do runbook importado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232e3-127">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="232e3-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="232e3-128">-Path</span></span>
<span data-ttu-id="232e3-129">Especifica o caminho de um arquivo. ps1 ou. graphrunbook que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="232e3-129">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="232e3-130">-Publicado</span><span class="sxs-lookup"><span data-stu-id="232e3-130">-Published</span></span>
<span data-ttu-id="232e3-131">Indica que esse cmdlet publica o runbook que ele importa.</span><span class="sxs-lookup"><span data-stu-id="232e3-131">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="232e3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="232e3-132">-ResourceGroupName</span></span>
<span data-ttu-id="232e3-133">Especifica o nome do grupo de recursos para o qual esse cmdlet importa um runbook.</span><span class="sxs-lookup"><span data-stu-id="232e3-133">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="232e3-134">-Marcas</span><span class="sxs-lookup"><span data-stu-id="232e3-134">-Tags</span></span>
<span data-ttu-id="232e3-135">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="232e3-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="232e3-136">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="232e3-136">For example:</span></span>

<span data-ttu-id="232e3-137">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="232e3-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="232e3-138">-Digite</span><span class="sxs-lookup"><span data-stu-id="232e3-138">-Type</span></span>
<span data-ttu-id="232e3-139">Especifica o tipo de runbook que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="232e3-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="232e3-140">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="232e3-140">Valid values are:</span></span>

- <span data-ttu-id="232e3-141">™</span><span class="sxs-lookup"><span data-stu-id="232e3-141">PowerShell</span></span>
- <span data-ttu-id="232e3-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="232e3-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="232e3-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="232e3-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="232e3-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="232e3-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="232e3-145">Representar</span><span class="sxs-lookup"><span data-stu-id="232e3-145">Graph</span></span>

<span data-ttu-id="232e3-146">O gráfico de valor é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="232e3-146">The value Graph is obsolete.</span></span>
<span data-ttu-id="232e3-147">É equivalente a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="232e3-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232e3-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="232e3-148">-Confirm</span></span>
<span data-ttu-id="232e3-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232e3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="232e3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="232e3-150">-WhatIf</span></span>
<span data-ttu-id="232e3-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="232e3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="232e3-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="232e3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="232e3-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232e3-153">-DefaultProfile</span></span>
<span data-ttu-id="232e3-154">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="232e3-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="232e3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232e3-155">CommonParameters</span></span>
<span data-ttu-id="232e3-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="232e3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232e3-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="232e3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232e3-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="232e3-158">INPUTS</span></span>

## <span data-ttu-id="232e3-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="232e3-159">OUTPUTS</span></span>

### <span data-ttu-id="232e3-160">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="232e3-160">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="232e3-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="232e3-161">NOTES</span></span>

## <span data-ttu-id="232e3-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="232e3-162">RELATED LINKS</span></span>

[<span data-ttu-id="232e3-163">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232e3-163">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232e3-164">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232e3-164">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232e3-165">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232e3-165">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232e3-166">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232e3-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232e3-167">Publicar-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232e3-167">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232e3-168">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232e3-168">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232e3-169">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232e3-169">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232e3-170">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232e3-170">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
