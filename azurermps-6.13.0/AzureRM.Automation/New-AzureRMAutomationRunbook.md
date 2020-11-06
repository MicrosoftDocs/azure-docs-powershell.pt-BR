---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 73945c02c5c5802e169e0868908874374080b344
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431452"
---
# <span data-ttu-id="7e82d-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e82d-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="7e82d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e82d-102">SYNOPSIS</span></span>
<span data-ttu-id="7e82d-103">Cria um runbook de automação.</span><span class="sxs-lookup"><span data-stu-id="7e82d-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e82d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e82d-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e82d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e82d-105">DESCRIPTION</span></span>
<span data-ttu-id="7e82d-106">O cmdlet **New-AzureRmAutomationRunbook** cria um runbook de automação do Azure vazio usando APS.</span><span class="sxs-lookup"><span data-stu-id="7e82d-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="7e82d-107">Especifique um nome para o runbook.</span><span class="sxs-lookup"><span data-stu-id="7e82d-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="7e82d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e82d-108">EXAMPLES</span></span>

### <span data-ttu-id="7e82d-109">Exemplo 1: criar um runbook</span><span class="sxs-lookup"><span data-stu-id="7e82d-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7e82d-110">Esse comando cria um runbook chamado Runbook02 na conta de automação do Azure chamado Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7e82d-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="7e82d-111">OS</span><span class="sxs-lookup"><span data-stu-id="7e82d-111">PARAMETERS</span></span>

### <span data-ttu-id="7e82d-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7e82d-112">-AutomationAccountName</span></span>
<span data-ttu-id="7e82d-113">Especifica o nome da conta de automação na qual esse cmdlet cria um runbook.</span><span class="sxs-lookup"><span data-stu-id="7e82d-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="7e82d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e82d-114">-DefaultProfile</span></span>
<span data-ttu-id="7e82d-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7e82d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e82d-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="7e82d-116">-Description</span></span>
<span data-ttu-id="7e82d-117">Especifica uma descrição para o runbook.</span><span class="sxs-lookup"><span data-stu-id="7e82d-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="7e82d-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="7e82d-118">-LogProgress</span></span>
<span data-ttu-id="7e82d-119">Especifica se o runbook registra o progresso.</span><span class="sxs-lookup"><span data-stu-id="7e82d-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="7e82d-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="7e82d-120">-LogVerbose</span></span>
<span data-ttu-id="7e82d-121">Especifica se o registro em log inclui informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="7e82d-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="7e82d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e82d-122">-Name</span></span>
<span data-ttu-id="7e82d-123">Especifica um nome para o runbook.</span><span class="sxs-lookup"><span data-stu-id="7e82d-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="7e82d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e82d-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e82d-125">Especifica o nome do grupo de recursos para o qual esse cmdlet cria um runbook.</span><span class="sxs-lookup"><span data-stu-id="7e82d-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="7e82d-126">-Marcas</span><span class="sxs-lookup"><span data-stu-id="7e82d-126">-Tags</span></span>
<span data-ttu-id="7e82d-127">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7e82d-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7e82d-128">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7e82d-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7e82d-129">-Digite</span><span class="sxs-lookup"><span data-stu-id="7e82d-129">-Type</span></span>
<span data-ttu-id="7e82d-130">Especifica o tipo de runbook que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="7e82d-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="7e82d-131">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="7e82d-131">Valid values are:</span></span>
- <span data-ttu-id="7e82d-132">™</span><span class="sxs-lookup"><span data-stu-id="7e82d-132">PowerShell</span></span>
- <span data-ttu-id="7e82d-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="7e82d-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="7e82d-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="7e82d-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="7e82d-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="7e82d-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="7e82d-136">O gráfico de valor é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7e82d-136">Graph The value Graph is obsolete.</span></span>
<span data-ttu-id="7e82d-137">É equivalente a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="7e82d-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="7e82d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e82d-138">CommonParameters</span></span>
<span data-ttu-id="7e82d-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e82d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e82d-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e82d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e82d-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e82d-141">INPUTS</span></span>

### <span data-ttu-id="7e82d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7e82d-142">System.String</span></span>

### <span data-ttu-id="7e82d-143">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="7e82d-143">System.Collections.IDictionary</span></span>

### <span data-ttu-id="7e82d-144">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7e82d-144">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7e82d-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e82d-145">OUTPUTS</span></span>

### <span data-ttu-id="7e82d-146">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="7e82d-146">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="7e82d-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e82d-147">NOTES</span></span>

## <span data-ttu-id="7e82d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e82d-148">RELATED LINKS</span></span>

[<span data-ttu-id="7e82d-149">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e82d-149">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e82d-150">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e82d-150">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e82d-151">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e82d-151">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e82d-152">Publicar-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e82d-152">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e82d-153">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e82d-153">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e82d-154">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e82d-154">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e82d-155">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e82d-155">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
