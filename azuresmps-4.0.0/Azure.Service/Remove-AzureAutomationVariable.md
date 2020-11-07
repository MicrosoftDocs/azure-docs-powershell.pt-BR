---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2D89557B-4B8B-43EE-8453-D55FCE0C2CE0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fdd9dd886e4056f2cb7e547098e5d3ab75a547
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946169"
---
# <span data-ttu-id="b2321-101">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b2321-101">Remove-AzureAutomationVariable</span></span>

## <span data-ttu-id="b2321-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2321-102">SYNOPSIS</span></span>

<span data-ttu-id="b2321-103">Remove uma variável de automação.</span><span class="sxs-lookup"><span data-stu-id="b2321-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="b2321-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2321-104">SYNTAX</span></span>

```
Remove-AzureAutomationVariable -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b2321-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2321-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b2321-106">O cmdlet **Remove-AzureAutomationVariable** remove uma variável da automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b2321-106">The **Remove-AzureAutomationVariable** cmdlet removes a variable from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="b2321-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2321-107">EXAMPLES</span></span>

### <span data-ttu-id="b2321-108">Exemplo 1: remover uma variável</span><span class="sxs-lookup"><span data-stu-id="b2321-108">Example 1: Remove a variable</span></span>
```
PS C:\> Remove-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Force
```

<span data-ttu-id="b2321-109">Esse comando Remove uma variável chamada MyStringVariable na conta de automação chamada Contoso17 sem solicitar a validação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b2321-109">This command removes a variable named MyStringVariable in the Automation account named Contoso17 without prompting for user validation.</span></span>

## <span data-ttu-id="b2321-110">OS</span><span class="sxs-lookup"><span data-stu-id="b2321-110">PARAMETERS</span></span>

### <span data-ttu-id="b2321-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b2321-111">-AutomationAccountName</span></span>
<span data-ttu-id="b2321-112">Especifica o nome da conta de automação com a variável.</span><span class="sxs-lookup"><span data-stu-id="b2321-112">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="b2321-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b2321-113">-Force</span></span>
<span data-ttu-id="b2321-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b2321-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2321-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2321-115">-Name</span></span>
<span data-ttu-id="b2321-116">Especifica o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="b2321-116">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="b2321-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b2321-117">-Profile</span></span>
<span data-ttu-id="b2321-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b2321-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2321-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b2321-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2321-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2321-120">CommonParameters</span></span>
<span data-ttu-id="b2321-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2321-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2321-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2321-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2321-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2321-123">INPUTS</span></span>

## <span data-ttu-id="b2321-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2321-124">OUTPUTS</span></span>

## <span data-ttu-id="b2321-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2321-125">NOTES</span></span>

## <span data-ttu-id="b2321-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2321-126">RELATED LINKS</span></span>

[<span data-ttu-id="b2321-127">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b2321-127">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="b2321-128">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b2321-128">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="b2321-129">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b2321-129">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


