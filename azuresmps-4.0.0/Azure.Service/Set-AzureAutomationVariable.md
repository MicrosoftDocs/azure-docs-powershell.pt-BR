---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 47664B13-5D63-4012-80E1-7982C8FE22E1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20edd29629cb5dbbfa6f3f538d1530e9c0692e6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946068"
---
# <span data-ttu-id="7a7fe-101">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7a7fe-101">Set-AzureAutomationVariable</span></span>

## <span data-ttu-id="7a7fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a7fe-102">SYNOPSIS</span></span>

<span data-ttu-id="7a7fe-103">Modifica uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="7a7fe-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="7a7fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a7fe-104">SYNTAX</span></span>

### <span data-ttu-id="7a7fe-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="7a7fe-105">UpdateVariableValue</span></span>
```
Set-AzureAutomationVariable -Name <String> -Encrypted <Boolean> -Value <Object> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7a7fe-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="7a7fe-106">UpdateVariableDescription</span></span>
```
Set-AzureAutomationVariable -Name <String> -Description <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7a7fe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a7fe-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7a7fe-108">O cmdlet **set-AzureAutomationVariable** modifica o valor ou a descrição de uma variável na automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7a7fe-108">The **Set-AzureAutomationVariable** cmdlet modifies the value or description of a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="7a7fe-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a7fe-109">EXAMPLES</span></span>

### <span data-ttu-id="7a7fe-110">Exemplo 1: definir o valor de uma variável</span><span class="sxs-lookup"><span data-stu-id="7a7fe-110">Example 1: Set the value of a variable</span></span>
```
PS C:\> Set-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="7a7fe-111">Esse comando define um novo valor para a variável chamada MyStringVariable na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7a7fe-111">This command sets a new value for the variable named MyStringVariable in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="7a7fe-112">OS</span><span class="sxs-lookup"><span data-stu-id="7a7fe-112">PARAMETERS</span></span>

### <span data-ttu-id="7a7fe-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7a7fe-113">-AutomationAccountName</span></span>
<span data-ttu-id="7a7fe-114">Especifica o nome da conta de automação com a variável.</span><span class="sxs-lookup"><span data-stu-id="7a7fe-114">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="7a7fe-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="7a7fe-115">-Description</span></span>
<span data-ttu-id="7a7fe-116">Especifica uma descrição para a variável.</span><span class="sxs-lookup"><span data-stu-id="7a7fe-116">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7fe-117">-Criptografado</span><span class="sxs-lookup"><span data-stu-id="7a7fe-117">-Encrypted</span></span>
<span data-ttu-id="7a7fe-118">Indica se a variável deve ser criptografada.</span><span class="sxs-lookup"><span data-stu-id="7a7fe-118">Indicates whether to encrypt the variable.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7fe-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a7fe-119">-Name</span></span>
<span data-ttu-id="7a7fe-120">Especifica o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="7a7fe-120">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="7a7fe-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7a7fe-121">-Profile</span></span>
<span data-ttu-id="7a7fe-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7a7fe-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7a7fe-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7a7fe-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7a7fe-124">-Valor</span><span class="sxs-lookup"><span data-stu-id="7a7fe-124">-Value</span></span>
<span data-ttu-id="7a7fe-125">Especifica um valor para a variável.</span><span class="sxs-lookup"><span data-stu-id="7a7fe-125">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7fe-126">CommonParameters</span></span>
<span data-ttu-id="7a7fe-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a7fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7fe-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a7fe-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7fe-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a7fe-129">INPUTS</span></span>

## <span data-ttu-id="7a7fe-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a7fe-130">OUTPUTS</span></span>

### <span data-ttu-id="7a7fe-131">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="7a7fe-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="7a7fe-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a7fe-132">NOTES</span></span>

## <span data-ttu-id="7a7fe-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a7fe-133">RELATED LINKS</span></span>

[<span data-ttu-id="7a7fe-134">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7a7fe-134">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="7a7fe-135">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7a7fe-135">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="7a7fe-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7a7fe-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)


