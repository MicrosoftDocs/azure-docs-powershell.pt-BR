---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778397"
---
# <span data-ttu-id="aaa01-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="aaa01-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="aaa01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aaa01-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa01-103">Modifica uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="aaa01-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="aaa01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aaa01-104">SYNTAX</span></span>

### <span data-ttu-id="aaa01-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="aaa01-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaa01-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="aaa01-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaa01-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aaa01-107">DESCRIPTION</span></span>
<span data-ttu-id="aaa01-108">O cmdlet **set-AzAutomationVariable** modifica o valor ou a descrição de uma variável na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="aaa01-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="aaa01-109">Para criptografar a variável, especifique o parâmetro *Encrypted* .</span><span class="sxs-lookup"><span data-stu-id="aaa01-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="aaa01-110">Não é possível modificar o estado criptografado de uma variável após a criação.</span><span class="sxs-lookup"><span data-stu-id="aaa01-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="aaa01-111">A especificação *criptografada* para uma variável existente, não criptografada falha.</span><span class="sxs-lookup"><span data-stu-id="aaa01-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="aaa01-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aaa01-112">EXAMPLES</span></span>

### <span data-ttu-id="aaa01-113">Exemplo 1: definir o valor de uma variável</span><span class="sxs-lookup"><span data-stu-id="aaa01-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="aaa01-114">Esse comando define um novo valor para a variável chamada StringVariable22 na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="aaa01-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="aaa01-115">OS</span><span class="sxs-lookup"><span data-stu-id="aaa01-115">PARAMETERS</span></span>

### <span data-ttu-id="aaa01-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aaa01-116">-AutomationAccountName</span></span>
<span data-ttu-id="aaa01-117">Especifica o nome da conta de automação na qual a variável está armazenada.</span><span class="sxs-lookup"><span data-stu-id="aaa01-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="aaa01-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa01-118">-DefaultProfile</span></span>
<span data-ttu-id="aaa01-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="aaa01-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaa01-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="aaa01-120">-Description</span></span>
<span data-ttu-id="aaa01-121">Especifica uma descrição para a variável.</span><span class="sxs-lookup"><span data-stu-id="aaa01-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="aaa01-122">-Criptografado</span><span class="sxs-lookup"><span data-stu-id="aaa01-122">-Encrypted</span></span>
<span data-ttu-id="aaa01-123">Especifica se o cmdlet criptografa o valor da variável para armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aaa01-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="aaa01-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="aaa01-124">-Name</span></span>
<span data-ttu-id="aaa01-125">Especifica o nome da variável que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="aaa01-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="aaa01-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaa01-126">-ResourceGroupName</span></span>
<span data-ttu-id="aaa01-127">Especifica o grupo de recursos para o qual esse cmdlet modifica uma variável.</span><span class="sxs-lookup"><span data-stu-id="aaa01-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="aaa01-128">-Valor</span><span class="sxs-lookup"><span data-stu-id="aaa01-128">-Value</span></span>
<span data-ttu-id="aaa01-129">Especifica um valor para a variável.</span><span class="sxs-lookup"><span data-stu-id="aaa01-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="aaa01-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa01-130">CommonParameters</span></span>
<span data-ttu-id="aaa01-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa01-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa01-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaa01-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa01-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aaa01-133">INPUTS</span></span>

### <span data-ttu-id="aaa01-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aaa01-134">System.String</span></span>

### <span data-ttu-id="aaa01-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aaa01-135">System.Boolean</span></span>

### <span data-ttu-id="aaa01-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="aaa01-136">System.Object</span></span>

## <span data-ttu-id="aaa01-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aaa01-137">OUTPUTS</span></span>

### <span data-ttu-id="aaa01-138">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="aaa01-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="aaa01-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aaa01-139">NOTES</span></span>

## <span data-ttu-id="aaa01-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aaa01-140">RELATED LINKS</span></span>

[<span data-ttu-id="aaa01-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="aaa01-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="aaa01-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="aaa01-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="aaa01-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="aaa01-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


