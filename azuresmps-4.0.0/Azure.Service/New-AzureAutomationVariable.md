---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D88C6B17-5D0E-4E23-9C5C-DB38DED9061C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1518c351a67c84e6dacafd1fa8a394051f3bfeac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945931"
---
# <span data-ttu-id="82a51-101">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="82a51-101">New-AzureAutomationVariable</span></span>

## <span data-ttu-id="82a51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82a51-102">SYNOPSIS</span></span>

<span data-ttu-id="82a51-103">Cria uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="82a51-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="82a51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82a51-104">SYNTAX</span></span>

```
New-AzureAutomationVariable -Name <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82a51-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82a51-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="82a51-106">O cmdlet **New-AzureAutomationVariable** cria uma variável na automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="82a51-106">The **New-AzureAutomationVariable** cmdlet creates a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="82a51-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82a51-107">EXAMPLES</span></span>

### <span data-ttu-id="82a51-108">Exemplo 1: criar uma nova variável com um valor simples</span><span class="sxs-lookup"><span data-stu-id="82a51-108">Example 1: Create a new variable with a simple value</span></span>
```
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Encrypted $False -Value "My String"
```

<span data-ttu-id="82a51-109">Esse comando cria uma nova variável chamada MyStringVariable com um valor de cadeia de caracteres na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82a51-109">This command creates a new variable named MyStringVariable with a string value in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="82a51-110">Exemplo 2: criar uma nova variável com um valor complexo</span><span class="sxs-lookup"><span data-stu-id="82a51-110">Example 2: Create a new variable with a complex value</span></span>
```
PS C:\> $vm = Get-AzureVM -ServiceName "MyVM" -Name "MyVM"
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyComplexVariable" -Encrypted $False -Value $vm
```

<span data-ttu-id="82a51-111">Esses comandos criam uma nova variável chamada MyComplexVariable na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="82a51-111">These commands create a new variable called MyComplexVariable in the Automation account named Contoso17.</span></span>
<span data-ttu-id="82a51-112">Um objeto complexo é usado para seu valor, nesse caso um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="82a51-112">A complex object is used for its value, in this case a virtual machine object.</span></span>

## <span data-ttu-id="82a51-113">OS</span><span class="sxs-lookup"><span data-stu-id="82a51-113">PARAMETERS</span></span>

### <span data-ttu-id="82a51-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="82a51-114">-AutomationAccountName</span></span>
<span data-ttu-id="82a51-115">Especifica o nome da conta de automação na qual a variável será armazenada.</span><span class="sxs-lookup"><span data-stu-id="82a51-115">Specifies the name of the Automation account the variable will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82a51-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="82a51-116">-Description</span></span>
<span data-ttu-id="82a51-117">Especifica uma descrição para a variável.</span><span class="sxs-lookup"><span data-stu-id="82a51-117">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="82a51-118">-Criptografado</span><span class="sxs-lookup"><span data-stu-id="82a51-118">-Encrypted</span></span>
<span data-ttu-id="82a51-119">Indica se o valor da variável deve ser armazenado criptografado.</span><span class="sxs-lookup"><span data-stu-id="82a51-119">Indicates whether the value of the variable should be stored encrypted.</span></span>

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

### <span data-ttu-id="82a51-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="82a51-120">-Name</span></span>
<span data-ttu-id="82a51-121">Especifica um nome para a variável.</span><span class="sxs-lookup"><span data-stu-id="82a51-121">Specifies a name for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82a51-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="82a51-122">-Profile</span></span>
<span data-ttu-id="82a51-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="82a51-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82a51-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="82a51-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a51-125">-Valor</span><span class="sxs-lookup"><span data-stu-id="82a51-125">-Value</span></span>
<span data-ttu-id="82a51-126">Especifica um valor a ser armazenado na variável.</span><span class="sxs-lookup"><span data-stu-id="82a51-126">Specifies a value to store in the variable.</span></span>

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

### <span data-ttu-id="82a51-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a51-127">CommonParameters</span></span>
<span data-ttu-id="82a51-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82a51-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a51-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a51-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a51-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82a51-130">INPUTS</span></span>

## <span data-ttu-id="82a51-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82a51-131">OUTPUTS</span></span>

### <span data-ttu-id="82a51-132">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="82a51-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="82a51-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82a51-133">NOTES</span></span>

## <span data-ttu-id="82a51-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82a51-134">RELATED LINKS</span></span>

[<span data-ttu-id="82a51-135">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="82a51-135">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="82a51-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="82a51-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="82a51-137">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="82a51-137">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


