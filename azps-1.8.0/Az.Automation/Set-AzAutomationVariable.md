---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: bc0fb96ace958761f4d6b12b73ac46b93d9a0143
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601495"
---
# <span data-ttu-id="ce785-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ce785-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="ce785-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce785-102">SYNOPSIS</span></span>
<span data-ttu-id="ce785-103">Modifica uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="ce785-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="ce785-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce785-104">SYNTAX</span></span>

### <span data-ttu-id="ce785-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="ce785-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce785-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="ce785-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce785-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce785-107">DESCRIPTION</span></span>
<span data-ttu-id="ce785-108">O cmdlet **set-AzAutomationVariable** modifica o valor ou a descrição de uma variável na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ce785-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="ce785-109">Para criptografar a variável, especifique o parâmetro *Encrypted* .</span><span class="sxs-lookup"><span data-stu-id="ce785-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="ce785-110">Não é possível modificar o estado criptografado de uma variável após a criação.</span><span class="sxs-lookup"><span data-stu-id="ce785-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="ce785-111">A especificação *criptografada* para uma variável existente, não criptografada falha.</span><span class="sxs-lookup"><span data-stu-id="ce785-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="ce785-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce785-112">EXAMPLES</span></span>

### <span data-ttu-id="ce785-113">Exemplo 1: definir o valor de uma variável</span><span class="sxs-lookup"><span data-stu-id="ce785-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="ce785-114">Esse comando define um novo valor para a variável chamada StringVariable22 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ce785-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ce785-115">OS</span><span class="sxs-lookup"><span data-stu-id="ce785-115">PARAMETERS</span></span>

### <span data-ttu-id="ce785-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ce785-116">-AutomationAccountName</span></span>
<span data-ttu-id="ce785-117">Especifica o nome da conta de automação na qual a variável está armazenada.</span><span class="sxs-lookup"><span data-stu-id="ce785-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="ce785-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce785-118">-DefaultProfile</span></span>
<span data-ttu-id="ce785-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ce785-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce785-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ce785-120">-Description</span></span>
<span data-ttu-id="ce785-121">Especifica uma descrição para a variável.</span><span class="sxs-lookup"><span data-stu-id="ce785-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="ce785-122">-Criptografado</span><span class="sxs-lookup"><span data-stu-id="ce785-122">-Encrypted</span></span>
<span data-ttu-id="ce785-123">Especifica se o cmdlet criptografa o valor da variável para armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ce785-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="ce785-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce785-124">-Name</span></span>
<span data-ttu-id="ce785-125">Especifica o nome da variável que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="ce785-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ce785-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce785-126">-ResourceGroupName</span></span>
<span data-ttu-id="ce785-127">Especifica o grupo de recursos para o qual esse cmdlet modifica uma variável.</span><span class="sxs-lookup"><span data-stu-id="ce785-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="ce785-128">-Valor</span><span class="sxs-lookup"><span data-stu-id="ce785-128">-Value</span></span>
<span data-ttu-id="ce785-129">Especifica um valor para a variável.</span><span class="sxs-lookup"><span data-stu-id="ce785-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="ce785-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce785-130">CommonParameters</span></span>
<span data-ttu-id="ce785-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce785-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce785-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce785-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce785-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce785-133">INPUTS</span></span>

### <span data-ttu-id="ce785-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ce785-134">System.String</span></span>

### <span data-ttu-id="ce785-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce785-135">System.Boolean</span></span>

### <span data-ttu-id="ce785-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="ce785-136">System.Object</span></span>

## <span data-ttu-id="ce785-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce785-137">OUTPUTS</span></span>

### <span data-ttu-id="ce785-138">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="ce785-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="ce785-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce785-139">NOTES</span></span>

## <span data-ttu-id="ce785-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce785-140">RELATED LINKS</span></span>

[<span data-ttu-id="ce785-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ce785-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="ce785-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ce785-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="ce785-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="ce785-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


