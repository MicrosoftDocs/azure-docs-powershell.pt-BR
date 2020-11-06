---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: ea07e0d0b0c60b35186224d7ea0284df17d1e27b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597783"
---
# <span data-ttu-id="58012-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="58012-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="58012-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58012-102">SYNOPSIS</span></span>
<span data-ttu-id="58012-103">Cria uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="58012-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="58012-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58012-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58012-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58012-105">DESCRIPTION</span></span>
<span data-ttu-id="58012-106">O cmdlet **New-AzAutomationVariable** cria uma variável na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="58012-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="58012-107">Para criptografar a variável, especifique o parâmetro *Encrypted* .</span><span class="sxs-lookup"><span data-stu-id="58012-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="58012-108">Não é possível modificar o estado criptografado de uma variável após a criação.</span><span class="sxs-lookup"><span data-stu-id="58012-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="58012-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58012-109">EXAMPLES</span></span>

### <span data-ttu-id="58012-110">Exemplo 1: criar uma variável com um valor simples</span><span class="sxs-lookup"><span data-stu-id="58012-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="58012-111">Esse comando cria uma variável chamada StringVariable22 com um valor de cadeia de caracteres na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="58012-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="58012-112">Exemplo 2: criar uma variável com um valor complexo</span><span class="sxs-lookup"><span data-stu-id="58012-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="58012-113">O primeiro comando obtém uma máquina virtual usando o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="58012-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="58012-114">O comando o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="58012-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="58012-115">O segundo comando cria uma variável chamada ComplexVariable01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="58012-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="58012-116">Esse comando usa um objeto complexo para seu valor, nesse caso, a máquina virtual no $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="58012-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="58012-117">OS</span><span class="sxs-lookup"><span data-stu-id="58012-117">PARAMETERS</span></span>

### <span data-ttu-id="58012-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="58012-118">-AutomationAccountName</span></span>
<span data-ttu-id="58012-119">Especifica o nome da conta de automação na qual armazenar a variável.</span><span class="sxs-lookup"><span data-stu-id="58012-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="58012-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58012-120">-DefaultProfile</span></span>
<span data-ttu-id="58012-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="58012-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58012-122">-Descrição</span><span class="sxs-lookup"><span data-stu-id="58012-122">-Description</span></span>
<span data-ttu-id="58012-123">Especifica uma descrição para a variável.</span><span class="sxs-lookup"><span data-stu-id="58012-123">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="58012-124">-Criptografado</span><span class="sxs-lookup"><span data-stu-id="58012-124">-Encrypted</span></span>
<span data-ttu-id="58012-125">Especifica se esse cmdlet criptografa o valor da variável para armazenamento.</span><span class="sxs-lookup"><span data-stu-id="58012-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58012-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="58012-126">-Name</span></span>
<span data-ttu-id="58012-127">Especifica um nome para a variável.</span><span class="sxs-lookup"><span data-stu-id="58012-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="58012-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58012-128">-ResourceGroupName</span></span>
<span data-ttu-id="58012-129">Especifica o grupo de recursos para o qual esse cmdlet cria uma variável.</span><span class="sxs-lookup"><span data-stu-id="58012-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="58012-130">-Valor</span><span class="sxs-lookup"><span data-stu-id="58012-130">-Value</span></span>
<span data-ttu-id="58012-131">Especifica um valor para a variável.</span><span class="sxs-lookup"><span data-stu-id="58012-131">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58012-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58012-132">CommonParameters</span></span>
<span data-ttu-id="58012-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58012-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58012-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58012-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58012-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58012-135">INPUTS</span></span>

### <span data-ttu-id="58012-136">System. String</span><span class="sxs-lookup"><span data-stu-id="58012-136">System.String</span></span>

### <span data-ttu-id="58012-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58012-137">System.Boolean</span></span>

### <span data-ttu-id="58012-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="58012-138">System.Object</span></span>

## <span data-ttu-id="58012-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58012-139">OUTPUTS</span></span>

### <span data-ttu-id="58012-140">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="58012-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="58012-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58012-141">NOTES</span></span>

## <span data-ttu-id="58012-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58012-142">RELATED LINKS</span></span>

[<span data-ttu-id="58012-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="58012-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="58012-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="58012-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="58012-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="58012-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


