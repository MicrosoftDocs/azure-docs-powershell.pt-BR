---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 4dd1eee278adcced1dbace9a30e88b5767037746
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597733"
---
# <span data-ttu-id="a1e15-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1e15-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="a1e15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1e15-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e15-103">Modifica um runbook.</span><span class="sxs-lookup"><span data-stu-id="a1e15-103">Modifies a runbook.</span></span>

## <span data-ttu-id="a1e15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1e15-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1e15-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1e15-105">DESCRIPTION</span></span>
<span data-ttu-id="a1e15-106">O cmdlet **set-AzAutomationRunbook** modifica a configuração de um runbook de automação do Azure no APS.</span><span class="sxs-lookup"><span data-stu-id="a1e15-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="a1e15-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1e15-107">EXAMPLES</span></span>

### <span data-ttu-id="a1e15-108">Exemplo 1: habilitar o registro em log detalhado para um runbook</span><span class="sxs-lookup"><span data-stu-id="a1e15-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a1e15-109">Esse comando habilita o registro em log detalhado para os trabalhos do runbook especificado na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a1e15-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a1e15-110">OS</span><span class="sxs-lookup"><span data-stu-id="a1e15-110">PARAMETERS</span></span>

### <span data-ttu-id="a1e15-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a1e15-111">-AutomationAccountName</span></span>
<span data-ttu-id="a1e15-112">Especifica o nome da conta de automação na qual esse cmdlet modifica um runbook.</span><span class="sxs-lookup"><span data-stu-id="a1e15-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="a1e15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e15-113">-DefaultProfile</span></span>
<span data-ttu-id="a1e15-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a1e15-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1e15-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a1e15-115">-Description</span></span>
<span data-ttu-id="a1e15-116">Especifica uma descrição para o runbook.</span><span class="sxs-lookup"><span data-stu-id="a1e15-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="a1e15-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="a1e15-117">-LogProgress</span></span>
<span data-ttu-id="a1e15-118">Especifica se o runbook registra o progresso.</span><span class="sxs-lookup"><span data-stu-id="a1e15-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="a1e15-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="a1e15-119">-LogVerbose</span></span>
<span data-ttu-id="a1e15-120">Especifica se o registro em log inclui informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="a1e15-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="a1e15-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1e15-121">-Name</span></span>
<span data-ttu-id="a1e15-122">Especifica o nome do runbook que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a1e15-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a1e15-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e15-123">-ResourceGroupName</span></span>
<span data-ttu-id="a1e15-124">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica um runbook.</span><span class="sxs-lookup"><span data-stu-id="a1e15-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="a1e15-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="a1e15-125">-Tag</span></span>
<span data-ttu-id="a1e15-126">As marcas do runbook.</span><span class="sxs-lookup"><span data-stu-id="a1e15-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e15-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e15-127">CommonParameters</span></span>
<span data-ttu-id="a1e15-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e15-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e15-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1e15-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e15-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1e15-130">INPUTS</span></span>

### <span data-ttu-id="a1e15-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a1e15-131">System.String</span></span>

### <span data-ttu-id="a1e15-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="a1e15-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="a1e15-133">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a1e15-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a1e15-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1e15-134">OUTPUTS</span></span>

### <span data-ttu-id="a1e15-135">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="a1e15-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="a1e15-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1e15-136">NOTES</span></span>

## <span data-ttu-id="a1e15-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1e15-137">RELATED LINKS</span></span>

[<span data-ttu-id="a1e15-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1e15-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="a1e15-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1e15-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="a1e15-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1e15-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="a1e15-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1e15-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a1e15-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1e15-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a1e15-143">Publicar-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1e15-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="a1e15-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1e15-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="a1e15-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a1e15-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


