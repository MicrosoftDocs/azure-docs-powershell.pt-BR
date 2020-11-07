---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CC6AF515-2F43-4E1B-BCBB-8DA23F3C6CBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8687cc00e9ba83c427666e08d0ad46c9aab45e02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945653"
---
# <span data-ttu-id="a0a4a-101">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a0a4a-101">Get-AzureAutomationVariable</span></span>

## <span data-ttu-id="a0a4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0a4a-102">SYNOPSIS</span></span>

<span data-ttu-id="a0a4a-103">Obtém uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="a0a4a-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="a0a4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0a4a-104">SYNTAX</span></span>

### <span data-ttu-id="a0a4a-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0a4a-105">ByAll (Default)</span></span>
```
Get-AzureAutomationVariable -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a0a4a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a0a4a-106">ByName</span></span>
```
Get-AzureAutomationVariable -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0a4a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0a4a-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a0a4a-108">O cmdlet **Get-AzureAutomationVariable** Obtém uma ou mais variáveis de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a4a-108">The **Get-AzureAutomationVariable** cmdlet gets one or more Microsoft Azure Automation variables.</span></span>
<span data-ttu-id="a0a4a-109">Por padrão, todas as variáveis são retornadas.</span><span class="sxs-lookup"><span data-stu-id="a0a4a-109">By default, all variables are returned.</span></span>
<span data-ttu-id="a0a4a-110">Para obter uma variável específica, especifique o nome dela.</span><span class="sxs-lookup"><span data-stu-id="a0a4a-110">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="a0a4a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0a4a-111">EXAMPLES</span></span>

### <span data-ttu-id="a0a4a-112">Exemplo 1: obter uma variável</span><span class="sxs-lookup"><span data-stu-id="a0a4a-112">Example 1: Get a variable</span></span>
```
PS C:\> $variable = Get-AzureAutomationVariable -AutomationAccountName
PS C:\> "Contoso17" -Name "MyVariable"
PS C:\> $value = $variable.value
```

<span data-ttu-id="a0a4a-113">Esses comandos obtêm uma variável de automação chamada myVariable e atribui seu valor a uma variável chamada $value.</span><span class="sxs-lookup"><span data-stu-id="a0a4a-113">These commands get an Automation variable called MyVariable and assign its value to a variable called $value.</span></span>

## <span data-ttu-id="a0a4a-114">OS</span><span class="sxs-lookup"><span data-stu-id="a0a4a-114">PARAMETERS</span></span>

### <span data-ttu-id="a0a4a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a0a4a-115">-AutomationAccountName</span></span>
<span data-ttu-id="a0a4a-116">Especifica o nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="a0a4a-116">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="a0a4a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0a4a-117">-Name</span></span>
<span data-ttu-id="a0a4a-118">Especifica o nome de uma variável.</span><span class="sxs-lookup"><span data-stu-id="a0a4a-118">Specifies the name of a variable.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a4a-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a0a4a-119">-Profile</span></span>
<span data-ttu-id="a0a4a-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a0a4a-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a0a4a-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a0a4a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a0a4a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a4a-122">CommonParameters</span></span>
<span data-ttu-id="a0a4a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a4a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a4a-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0a4a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a4a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0a4a-125">INPUTS</span></span>

## <span data-ttu-id="a0a4a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0a4a-126">OUTPUTS</span></span>

### <span data-ttu-id="a0a4a-127">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="a0a4a-127">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="a0a4a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0a4a-128">NOTES</span></span>

## <span data-ttu-id="a0a4a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0a4a-129">RELATED LINKS</span></span>

[<span data-ttu-id="a0a4a-130">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a0a4a-130">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="a0a4a-131">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a0a4a-131">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="a0a4a-132">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a0a4a-132">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


