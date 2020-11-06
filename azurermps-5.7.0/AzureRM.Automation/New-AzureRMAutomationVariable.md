---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: 217a6553a21871e79998dcad0630f4c0e1b6aec4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440133"
---
# <span data-ttu-id="a62fd-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a62fd-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="a62fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a62fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a62fd-103">Cria uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="a62fd-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a62fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a62fd-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a62fd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a62fd-105">DESCRIPTION</span></span>
<span data-ttu-id="a62fd-106">O cmdlet **New-AzureRmAutomationVariable** cria uma variável na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="a62fd-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="a62fd-107">Para criptografar a variável, especifique o parâmetro *Encrypted* .</span><span class="sxs-lookup"><span data-stu-id="a62fd-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="a62fd-108">Não é possível modificar o estado criptografado de uma variável após a criação.</span><span class="sxs-lookup"><span data-stu-id="a62fd-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="a62fd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a62fd-109">EXAMPLES</span></span>

### <span data-ttu-id="a62fd-110">Exemplo 1: criar uma variável com um valor simples</span><span class="sxs-lookup"><span data-stu-id="a62fd-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a62fd-111">Esse comando cria uma variável chamada StringVariable22 com um valor de cadeia de caracteres na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a62fd-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a62fd-112">Exemplo 2: criar uma variável com um valor complexo</span><span class="sxs-lookup"><span data-stu-id="a62fd-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a62fd-113">O primeiro comando obtém uma máquina virtual usando o cmdlet Get-AzureVM.</span><span class="sxs-lookup"><span data-stu-id="a62fd-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="a62fd-114">O comando o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a62fd-114">The command stores it in the $VirtualMachine variable.</span></span>

<span data-ttu-id="a62fd-115">O segundo comando cria uma variável chamada ComplexVariable01 na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a62fd-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="a62fd-116">Esse comando usa um objeto complexo para seu valor, nesse caso, a máquina virtual no $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a62fd-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="a62fd-117">OS</span><span class="sxs-lookup"><span data-stu-id="a62fd-117">PARAMETERS</span></span>

### <span data-ttu-id="a62fd-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a62fd-118">-AutomationAccountName</span></span>
<span data-ttu-id="a62fd-119">Especifica o nome da conta de automação na qual armazenar a variável.</span><span class="sxs-lookup"><span data-stu-id="a62fd-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="a62fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a62fd-120">-DefaultProfile</span></span>
<span data-ttu-id="a62fd-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a62fd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a62fd-122">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a62fd-122">-Description</span></span>
<span data-ttu-id="a62fd-123">Especifica uma descrição para a variável.</span><span class="sxs-lookup"><span data-stu-id="a62fd-123">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="a62fd-124">-Criptografado</span><span class="sxs-lookup"><span data-stu-id="a62fd-124">-Encrypted</span></span>
<span data-ttu-id="a62fd-125">Especifica se esse cmdlet criptografa o valor da variável para armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a62fd-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62fd-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a62fd-126">-Name</span></span>
<span data-ttu-id="a62fd-127">Especifica um nome para a variável.</span><span class="sxs-lookup"><span data-stu-id="a62fd-127">Specifies a name for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62fd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a62fd-128">-ResourceGroupName</span></span>
<span data-ttu-id="a62fd-129">Especifica o grupo de recursos para o qual esse cmdlet cria uma variável.</span><span class="sxs-lookup"><span data-stu-id="a62fd-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="a62fd-130">-Valor</span><span class="sxs-lookup"><span data-stu-id="a62fd-130">-Value</span></span>
<span data-ttu-id="a62fd-131">Especifica um valor para a variável.</span><span class="sxs-lookup"><span data-stu-id="a62fd-131">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62fd-132">CommonParameters</span></span>
<span data-ttu-id="a62fd-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a62fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62fd-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a62fd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62fd-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a62fd-135">INPUTS</span></span>

### <span data-ttu-id="a62fd-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a62fd-136">None</span></span>
<span data-ttu-id="a62fd-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a62fd-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a62fd-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a62fd-138">OUTPUTS</span></span>

### <span data-ttu-id="a62fd-139">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="a62fd-139">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="a62fd-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a62fd-140">NOTES</span></span>

## <span data-ttu-id="a62fd-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a62fd-141">RELATED LINKS</span></span>

[<span data-ttu-id="a62fd-142">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a62fd-142">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="a62fd-143">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a62fd-143">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="a62fd-144">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a62fd-144">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


