---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: ff83049e6afec5b0a6712aef2622bd9cbe0110c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892237"
---
# <span data-ttu-id="2e2cc-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2e2cc-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="2e2cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e2cc-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2cc-103">Modifica uma variável automation.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="2e2cc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2e2cc-104">SYNTAX</span></span>

### <span data-ttu-id="2e2cc-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="2e2cc-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e2cc-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="2e2cc-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e2cc-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2e2cc-107">DESCRIPTION</span></span>
<span data-ttu-id="2e2cc-108">O cmdlet **Set-AzAutomationVariable** modifica o valor ou a descrição de uma variável no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="2e2cc-109">Para criptografar a variável, especifique o *parâmetro Encrypted.*</span><span class="sxs-lookup"><span data-stu-id="2e2cc-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="2e2cc-110">Não é possível modificar o estado criptografado de uma variável após a criação.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="2e2cc-111">A *especificação criptografada* para uma variável existente, não criptografada, falha.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="2e2cc-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e2cc-112">EXAMPLES</span></span>

### <span data-ttu-id="2e2cc-113">Exemplo 1: definir o valor de uma variável</span><span class="sxs-lookup"><span data-stu-id="2e2cc-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="2e2cc-114">Este comando define um novo valor para a variável chamada StringVariable22 na conta de Automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="2e2cc-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2e2cc-115">PARAMETERS</span></span>

### <span data-ttu-id="2e2cc-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2e2cc-116">-AutomationAccountName</span></span>
<span data-ttu-id="2e2cc-117">Especifica o nome da conta de automação na qual a variável é armazenada.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="2e2cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e2cc-118">-DefaultProfile</span></span>
<span data-ttu-id="2e2cc-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2e2cc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e2cc-120">-Description</span><span class="sxs-lookup"><span data-stu-id="2e2cc-120">-Description</span></span>
<span data-ttu-id="2e2cc-121">Especifica uma descrição para a variável.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e2cc-122">-Encrypted</span><span class="sxs-lookup"><span data-stu-id="2e2cc-122">-Encrypted</span></span>
<span data-ttu-id="2e2cc-123">Especifica se o cmdlet criptografa o valor da variável para armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e2cc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2e2cc-124">-Name</span></span>
<span data-ttu-id="2e2cc-125">Especifica o nome da variável que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e2cc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e2cc-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e2cc-127">Especifica o grupo de recursos para o qual este cmdlet modifica uma variável.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="2e2cc-128">-Value</span><span class="sxs-lookup"><span data-stu-id="2e2cc-128">-Value</span></span>
<span data-ttu-id="2e2cc-129">Especifica um valor para a variável.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e2cc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2cc-130">CommonParameters</span></span>
<span data-ttu-id="2e2cc-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e2cc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2cc-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e2cc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2cc-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e2cc-133">INPUTS</span></span>

### <span data-ttu-id="2e2cc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2e2cc-134">System.String</span></span>

### <span data-ttu-id="2e2cc-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e2cc-135">System.Boolean</span></span>

### <span data-ttu-id="2e2cc-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="2e2cc-136">System.Object</span></span>

## <span data-ttu-id="2e2cc-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2e2cc-137">OUTPUTS</span></span>

### <span data-ttu-id="2e2cc-138">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="2e2cc-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="2e2cc-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="2e2cc-139">NOTES</span></span>

## <span data-ttu-id="2e2cc-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e2cc-140">RELATED LINKS</span></span>

[<span data-ttu-id="2e2cc-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2e2cc-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="2e2cc-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2e2cc-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="2e2cc-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2e2cc-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


