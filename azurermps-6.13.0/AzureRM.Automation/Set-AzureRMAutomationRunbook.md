---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 26f3214cf98e43a805aab99eb3ad1b92f289b2bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429601"
---
# <span data-ttu-id="95598-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="95598-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="95598-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95598-102">SYNOPSIS</span></span>
<span data-ttu-id="95598-103">Modifica um runbook.</span><span class="sxs-lookup"><span data-stu-id="95598-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95598-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95598-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95598-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95598-105">DESCRIPTION</span></span>
<span data-ttu-id="95598-106">O cmdlet **set-AzureRmAutomationRunbook** modifica a configuração de um runbook de automação do Azure no APS.</span><span class="sxs-lookup"><span data-stu-id="95598-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="95598-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95598-107">EXAMPLES</span></span>

### <span data-ttu-id="95598-108">Exemplo 1: habilitar o registro em log detalhado para um runbook</span><span class="sxs-lookup"><span data-stu-id="95598-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="95598-109">Esse comando habilita o registro em log detalhado para os trabalhos do runbook especificado na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="95598-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="95598-110">OS</span><span class="sxs-lookup"><span data-stu-id="95598-110">PARAMETERS</span></span>

### <span data-ttu-id="95598-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="95598-111">-AutomationAccountName</span></span>
<span data-ttu-id="95598-112">Especifica o nome da conta de automação na qual esse cmdlet modifica um runbook.</span><span class="sxs-lookup"><span data-stu-id="95598-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="95598-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95598-113">-DefaultProfile</span></span>
<span data-ttu-id="95598-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="95598-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95598-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="95598-115">-Description</span></span>
<span data-ttu-id="95598-116">Especifica uma descrição para o runbook.</span><span class="sxs-lookup"><span data-stu-id="95598-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="95598-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="95598-117">-LogProgress</span></span>
<span data-ttu-id="95598-118">Especifica se o runbook registra o progresso.</span><span class="sxs-lookup"><span data-stu-id="95598-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="95598-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="95598-119">-LogVerbose</span></span>
<span data-ttu-id="95598-120">Especifica se o registro em log inclui informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="95598-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="95598-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="95598-121">-Name</span></span>
<span data-ttu-id="95598-122">Especifica o nome do runbook que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="95598-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="95598-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95598-123">-ResourceGroupName</span></span>
<span data-ttu-id="95598-124">Especifica o nome do grupo de recursos para o qual esse cmdlet modifica um runbook.</span><span class="sxs-lookup"><span data-stu-id="95598-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="95598-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="95598-125">-Tag</span></span>
<span data-ttu-id="95598-126">As marcas do runbook.</span><span class="sxs-lookup"><span data-stu-id="95598-126">The runbook tags.</span></span>

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

### <span data-ttu-id="95598-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95598-127">CommonParameters</span></span>
<span data-ttu-id="95598-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95598-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95598-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95598-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95598-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95598-130">INPUTS</span></span>

### <span data-ttu-id="95598-131">System. String</span><span class="sxs-lookup"><span data-stu-id="95598-131">System.String</span></span>

### <span data-ttu-id="95598-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="95598-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="95598-133">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="95598-133">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="95598-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95598-134">OUTPUTS</span></span>

### <span data-ttu-id="95598-135">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="95598-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="95598-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95598-136">NOTES</span></span>

## <span data-ttu-id="95598-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95598-137">RELATED LINKS</span></span>

[<span data-ttu-id="95598-138">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="95598-138">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="95598-139">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="95598-139">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="95598-140">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="95598-140">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="95598-141">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="95598-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="95598-142">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="95598-142">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="95598-143">Publicar-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="95598-143">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="95598-144">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="95598-144">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="95598-145">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="95598-145">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


