---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: c2e03cae02c776b69c424ea3ff685a4118ed94bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431828"
---
# <span data-ttu-id="f88c5-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f88c5-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="f88c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f88c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f88c5-103">Cria uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="f88c5-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f88c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f88c5-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f88c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f88c5-105">DESCRIPTION</span></span>
<span data-ttu-id="f88c5-106">O cmdlet **New-AzureRmAutomationVariable** cria uma variável na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="f88c5-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="f88c5-107">Para criptografar a variável, especifique o parâmetro *Encrypted* .</span><span class="sxs-lookup"><span data-stu-id="f88c5-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="f88c5-108">Não é possível modificar o estado criptografado de uma variável após a criação.</span><span class="sxs-lookup"><span data-stu-id="f88c5-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="f88c5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f88c5-109">EXAMPLES</span></span>

### <span data-ttu-id="f88c5-110">Exemplo 1: criar uma variável com um valor simples</span><span class="sxs-lookup"><span data-stu-id="f88c5-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f88c5-111">Esse comando cria uma variável chamada StringVariable22 com um valor de cadeia de caracteres na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f88c5-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f88c5-112">Exemplo 2: criar uma variável com um valor complexo</span><span class="sxs-lookup"><span data-stu-id="f88c5-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f88c5-113">O primeiro comando obtém uma máquina virtual usando o cmdlet Get-AzureVM.</span><span class="sxs-lookup"><span data-stu-id="f88c5-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="f88c5-114">O comando o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f88c5-114">The command stores it in the $VirtualMachine variable.</span></span>

<span data-ttu-id="f88c5-115">O segundo comando cria uma variável chamada ComplexVariable01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f88c5-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f88c5-116">Esse comando usa um objeto complexo para seu valor, nesse caso, a máquina virtual no $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f88c5-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="f88c5-117">OS</span><span class="sxs-lookup"><span data-stu-id="f88c5-117">PARAMETERS</span></span>

### <span data-ttu-id="f88c5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f88c5-118">-AutomationAccountName</span></span>
<span data-ttu-id="f88c5-119">Especifica o nome da conta de automação na qual armazenar a variável.</span><span class="sxs-lookup"><span data-stu-id="f88c5-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="f88c5-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f88c5-120">-Description</span></span>
<span data-ttu-id="f88c5-121">Especifica uma descrição para a variável.</span><span class="sxs-lookup"><span data-stu-id="f88c5-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="f88c5-122">-Criptografado</span><span class="sxs-lookup"><span data-stu-id="f88c5-122">-Encrypted</span></span>
<span data-ttu-id="f88c5-123">Especifica se esse cmdlet criptografa o valor da variável para armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f88c5-123">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="f88c5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f88c5-124">-Name</span></span>
<span data-ttu-id="f88c5-125">Especifica um nome para a variável.</span><span class="sxs-lookup"><span data-stu-id="f88c5-125">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="f88c5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f88c5-126">-ResourceGroupName</span></span>
<span data-ttu-id="f88c5-127">Especifica o grupo de recursos para o qual esse cmdlet cria uma variável.</span><span class="sxs-lookup"><span data-stu-id="f88c5-127">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="f88c5-128">-Valor</span><span class="sxs-lookup"><span data-stu-id="f88c5-128">-Value</span></span>
<span data-ttu-id="f88c5-129">Especifica um valor para a variável.</span><span class="sxs-lookup"><span data-stu-id="f88c5-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="f88c5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88c5-130">-DefaultProfile</span></span>
<span data-ttu-id="f88c5-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f88c5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f88c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88c5-132">CommonParameters</span></span>
<span data-ttu-id="f88c5-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f88c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88c5-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f88c5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88c5-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f88c5-135">INPUTS</span></span>

## <span data-ttu-id="f88c5-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f88c5-136">OUTPUTS</span></span>

### <span data-ttu-id="f88c5-137">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="f88c5-137">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="f88c5-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f88c5-138">NOTES</span></span>

## <span data-ttu-id="f88c5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f88c5-139">RELATED LINKS</span></span>

[<span data-ttu-id="f88c5-140">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f88c5-140">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="f88c5-141">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f88c5-141">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="f88c5-142">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f88c5-142">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


